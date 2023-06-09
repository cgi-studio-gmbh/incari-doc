# Using APIs to Pull Dynamic Data

### Introduction

_Application programming interfaces_ (APIs) allow developers to retrieve data from various services, based on some queries and parameters. The API providor decides _what_ and _how_ data can be accessed, and this information is usually made available in the form of documentation.

There are thousands of paid and free API services that exist on the Internet, ranging from sources as diverse as ["facts" about Chuck Norris](https://api.chucknorris.io/) to retrieving detailed information about what the weather is like... [on Mars](https://api.nasa.gov/)!

For our latest demo, we will be looking at the weather much closer to home and the basic workflow of working with APIs.

#### OpenWeatherMap

[_OpenWeatherMap_](https://openweathermap.org/) provides a free API, capable of getting detailed weather information from over 200,000 cities. To use the service in our **Incari** demo, you will first need to [create an account](https://home.openweathermap.org/users/sign\_up) and [generate an API Key](https://home.openweathermap.org/api\_keys). An API Key is a 32-character code, unique to your account, which will be used every time you make an API request.

#### Getting the Demo

As an example of how to use an API and how the data retrieved can be used in **Incari**, we have created a fully-functional weather application, which you can download from the _Remote Projects_ section of **Incari Hub**. There, you will see a project called **'WeatherWidget'**, which you can download to your local machine by pressing the download icon.

### Project Overview

![](../.gitbook/assets/demoweatherapp\_overview.png)

If you open up the **Project** and look inside the **Logic Editor**, under the **'Root'** **Scene** tab, you will see the top-level **Logic** for the demo. To get things working, you will first need to change a few variables, which can be seen in the **Variables** tab of the **Logic Editor**. The **Variables** are:

1. `apiKey` - The 32-character API key, unique to your OpenWeatherMap account.
2. `locationsList` - A list of four locations for which you want to retrieve the weather. To avoid ambiguity issues with location names, it is preferred to use both the city name _and_ country. "San Francisco" could be 1 of 5 locations, but "San Francisco, US" yields only one result. To see the search results beforehand, you can check them [here](https://openweathermap.org/find).
3. `isMetric` - Whether the temperature should be in metric (°C) or imperial (°F) units.

![](../.gitbook/assets/demoweatherapp\_differentLocations.gif)

Once these **Variables** are changed you can press play to start the simulation. You should now be able to see current weather information for the locations listed in `locationsList`.

### HTTP GET

**Incari's** **HTTP GET Node** is what makes this kind of functionality possible. It takes some information, based on the documentation of the API provider, constructs and calls an API request, and asynchronously returns the response as a string.

If you take a look at the documentation at [_OpenWeatherMaps's API documentation_](https://openweathermap.org/current), you will see that one of the examples of an API call that it provides is the following:

```
http://api.openweathermap.org/data/2.5/weather?q=London&appid={API key}
```

#### The Connection Attributes

* `Remote IP` - The first section of this request is `http://api.openweathermap.org`, which is our endpoint. This is the value we put inside the `Remote IP` **Attribute**. A couple of notes regarding this **Attribute**:
  1. An IP address can also be used, instead of a URL.
  2. The **HTTP GET Node**, like all other **HTTP** **Nodes**, supports both the _HTTP_ and _HTTPS_ protocols. However this **Project** will focus on _HTTP_.
* `Remote Port` - For the `Remote Port` **Attribute**, this should be set to 80, which is the standard port for _HTTP_ usage.

#### The Request Header Attributes

* `Method` - Because we want to _get_ data, the `Method` **Attribute** should be set to "GET".
* `Path` - This is the specific path defined by the API provider. Usually, this is the text after the main root URL but before the`?`character. In the case above, the path is `/data/2.5/weather`.
* `Authentication` - This is used if the API requires a username and password, however OpenWeatherMap doesn't require this, so we set it to "None".
* `Default Headers` - This allows us to add additional information in the form of key-value pairs, using [_HTTP headers_](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers). For our example, though, we don't need to add any.

#### The Request Query Attributes

![](<../.gitbook/assets/untitled (1).png>)

A query is a selection of key-value pairs, which form the parameters of the API call. One of these pairs almost always relates to the API key. In the case of OpenWeatherMap, this parameter is called `appid` and needs to be used whenever attempting to retrieve data.

In the example call above, you will see that part of the string says `q=London`. By looking at the [documentation](https://openweathermap.org/current), you will see that the parameter `q` is the "City name, state code and country code divided by comma".

Also, for localization purposes, there is one more query which determines the temperature format. By default, the SI unit Kelvin is used when making API calls on OpenWeatherMap. To change this to degrees Celsius (°C) or degrees Fahrenheit (°F), the `units` parameter should be set to "metric" or "imperial".

If we were to put this information directly into the **Attributes** of the **Node**, it would look something like the image here:

#### The Request Query as a Variable

![](../.gitbook/assets/demoweatherapi\_queryinitial.png)

Although building the query directly in the **Attribute Editor** may work correctly, it is much better practice to break this up into **Variables**, so that all settings of our application can be changed in one place (the **Variable** tab of the **Logic Editor**) and can be dynamically adjusted on-the-fly. If you look at the initialization **Logic** above, we are using the variables `isMetric`, `apiKey`, and `city` to build a **Dictionary**, which will form a query for each location in the `locationsList` **Array** and put it into the `queryList` **Array**.

![](../.gitbook/assets/demoweatherapi\_inputSetResponse1png.png)

Each element of the `queryList` **Array** is then used as a `Query` input parameter for the `SetResponse` **Function**.

![](../.gitbook/assets/demoweatherapi\_setresponsefunction.png)

This parameter is passed into the `HTTP GET` **Node** `Query` **Input Socket**, overriding any information in the **Node's** `Request Query` **Attribute**. The `SetResponse` **Function** outputs a `Response` parameter that is used to set different `WeatherScreen` **Attributes**

### JSON

JavaScript Object Notation (JSON) is a data-interchange format, commonly used by APIs. Some APIs may require the format of the response to be defined explicitly, however, OpenWeatherMap returns JSON-formatted data by default.

Because **HTTP GET** returns the JSON as one big **String**, we need to convert this into a format that we can use. The **Dictionary** data type is the perfect option for this, as it is made up of [key-value pairs](https://www.techopedia.com/definition/13645/key-value-pair-kvp), which can be accessed by name in other parts of our **Logic**.

![](../.gitbook/assets/image.png)

To convert the `Body` output (the response) into a **Dictionary**, we can use the new **JSON Parse Node** to convert the **String**. Because JSON can also be parsed as an **Array**, we need to tell **Incari** that we are expecting a **Dictionary**, not an **Array**. We do this by using the **Conversion** **Node** to _cast_ the **Any**-type output of the **JSON Parse Node** to a **Dictionary**.

### Dictionaries

**Dictionaries** are a common data structure, used in many programming languages. The term "dictionary" stems from the fact that, like a dictionary, you look up a string of characters (a word in the case of a physical dictionary) to get the information or definition associated with that particular string.

**Dictionaries** share _some_ similarities with **Arrays**, namely that they are both _collections_ of data. Where they differ, though, is that **Dictionaries** are _unordered_ (can't be iterated over using loops) and their values can only be accessed via their _key_. Conversely, **Arrays** are _ordered_ and the values are accessed by their _index_.

The reason why **Dictionaries** are advantageous when dealing with APIs is that once the JSON has been parsed we can access what we need by a _key_ name that relates to the information we need. **Dictionaries** can even contain other **Dictionaries**.

![](../.gitbook/assets/dictionaries.png)

For example, if you look at the image above, you will see that from the main `Response` variable, we are getting another **Dictionary** called `main`. From this, we are then able to get the temperature (`temp`) as a **Float**. This structure (`main` > `temp`) corresponds to the [OpenWeatherMap documentation](https://openweathermap.org/current#parameter), which shows an example of the hierarchy of the API response.

### On Set

For each location, after generating a `Response` **Dictionary**-type **Variable** with the `SetResponse` **Function**, this output is passed to the `SetWeatherScreenValues` **Function** and fed into a number of custom **Functions** to get the relevant _key-value pairs_ and process them.

![](../.gitbook/assets/demoweatherapp\_setWeatherScreenValues.png)

![](../.gitbook/assets/demoweatherapp\_setWeatherScreenValuesLogic.png)

This **Function** outputs a set of **Strings** and **Int** values which is then passed to the `WeatherScreen` **Prefab** **Node**.

![](../.gitbook/assets/demoweatherapp\_prefabLogic\_01.png)

Inside the **Prefab** **Logic**, every input parameter is passed on to a local **Variable**.

In [Part 8 of our Tutorial for Beginners](https://www.youtube.com/watch?v=odtn4941x4Q\&ab\_channel=IncariHMIDevelopmentPlatform), we discussed the advantages of _decoupling_ **Logic**.

![](../.gitbook/assets/demoweatherapp\_prefabLogic\_02.png)

![](../.gitbook/assets/demoweatherapp\_prefabLogic\_03.png)

By putting input parameters into local **Variables**, it is possible to trigger a **Logic Branch** only in the case that a **Variable** is changed at runtime.

### Conclusion

Although we have focused primarily on weather information in this example, there are thousands of different APIs which can be applied in infinite ways. The core functionality in **Incari**, however, will remain the same:

1. You use the **HTTP Get Node** to make an API call, parse the data into a **Dictionary** using the **JSON Parse Node**
2. You then use that data to change aspects of your application.

Whether you want to get [playlists from Spotify](https://developer.spotify.com/documentation/web-api/quick-start/), [navigation information from Mapbox](https://docs.mapbox.com/api/), or [financial market data from Finnhub](https://finnhub.io/), APIs open a whole world of possibilities when it comes to creating engaging HMI experiences.

### Links

* [_Understanding And Using REST APIs - Smashing Magazine_](https://www.smashingmagazine.com/2018/01/understanding-using-rest-api/)
* [_HTTP request methods_](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
* [_Weather API_](https://openweathermap.org/api)
