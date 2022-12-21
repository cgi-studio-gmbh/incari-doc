---
description: Methods PUT, DELETE, and HEAD available since 2022.1.2
---

# HTTP Client

## Overview

The **HTTP Client Node** allows the user to send *HTTP* requests to a selected *HTTP* server. All configurations are made in the **Node** or in the **Attributes** section. There are several methods that the user can select from to perform different *HTTP* requests. These are: [**GET**](httpclient.md#get), [**POST**](httpclient.md#post), [**PUT**](httpclient.md#put), [**HEAD**](httpclient.md#head), and [**DELETE**](httpclient.md#delete).

[**Scope**](../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

![HTTP Client Methods.](../../../.gitbook/assets/httpclientmethod.png)

## Common Attributes, Inputs, and Outputs

Depending on the `Method` selected, the **Attributes** and **Inputs** might change. However, there are several common [**Attributes**](httpclient.md#common-attributes), [**Inputs**](httpclient.md#common-inputs), and [**Outputs**](httpclient.md#common-outputs) between the many **HTTP** `Methods`.
### Common Attributes

![HTTP Shared Attributes.](../../../.gitbook/assets/httpclientattributes.png)
 

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Remote IP` | **User Input** | The _HTTP_ endpoint \(either a URL or IP address\). |
| `Remote Port` | **Int** | The port value. For _HTTP_, the standard is 80 and for *HTTPS*, the standard is 443. |
| `Method` | **Drop-down** | Either **GET**, **POST**, **PUT**, **HEAD**, or **DELETE**.|
| `Path` | **User Input** | A specific path from the call being referenced in `Remote IP`. Usually, this is the text after the main root URL but before the `?` character. |
| `Authentication` | **Drop-down** | The user selects `Basic` when a username and password are required to access the information, otherwise `None` is chosen. |
| `Default Headers` | **Add Elements** | _HTTP_ headers in the form of key/value pairs. |
| `Request Query` | **Add Elements** | Parameters of the call in the form of key/value pairs. |
| `Is Response Body Binary` | **Bool** | The user chooses true or false depending on whether they wish for the `Response Body` output to remain a **String** or be converted into *binary*.  Currently, the **Node** only supports **Strings**. |

### Common Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| _Pulse Input_ \(►\) | **Pulse** | A standard **Input Pulse**, to trigger the execution of the **Node**. |
| `Remote IP` | **String** | The _HTTP_ endpoint \(either a URL or IP address\). |
| `Remote Port` | **Int** | The port value. For _HTTP_, the standard is 80 and for *HTTPS*, the standard is 443. |
| `Path` | **String** | A specific path from the call being referenced in `Remote IP`. Usually, this is the text after the main root URL but before the `?` character. |
| `Headers` | **Dictionary** | _HTTP_ headers in the form of key/value pairs. |
| `Query` | **Dictionary** | Parameters of the call in the form of key/value pairs. |

### Common Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |
| `OnResponse` \(►\) | **Pulse** | Flows to additional actions when there is a response. |
| `Status Code` | **Int** | A standard status code within the _HTTP_ protocol. For example, 404 is when a page is not found. |
| `Headers` | **Dictionary** |  _HTTP_ headers in the form of key/value pairs. |
| `Body` | **String** | The body of the response, usually including _HTML_ text. |


## Methods
### GET

![The HTTP Client Node using Method GET.](../../../.gitbook/assets/httpgetupdatedimage.png)

**GET** creates a request and returns the response as per the _HTTP_ protocol. This is very useful when dealing with web APIs. A more detailed explanation involving web APIs can be found in the **See Also** section. Additional information on the different *HTTP* methods can be found in the **External Links** section.

### POST

![The HTTP Client Node using Method POST.](../../../.gitbook/assets/httppostupdatedimage.png)

**POST** sends data, in this case the information from the `Request Body`, to the desired server as per the _HTTP_ protocol. More information on the different *HTTP* methods can be found in the **External Links** section. All **Attributes** and **Inputs** are the same as the common **Attributes**, except for the addition of the following:

#### Attributes

![The HTTP Client Node Attributes using Method POST.](../../../.gitbook/assets/httppostattributesreal.png)

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Default Body` | **String** | The body of the _HTTP_ request, if none is provided in the **Input Socket**. |

#### Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| `Body` | **String** | The body of the _HTTP_ request. |



### PUT

![The HTTP Client Node using Method PUT.](../../../.gitbook/assets/httpputupdatedimage.png)

**PUT** updates already existing data on the desired server per the *HTTP* protocol. More information on the different *HTTP* methods can be found in the **External Links** section. All **Attributes** and **Inputs** are the same as the common **Attributes**, except for the addition of the following:

#### Attributes

![The HTTP Client Node Attributes using Method PUT.](../../../.gitbook/assets/httppostattributesreal.png)

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Default Body` | **String** | The body of the _HTTP_ request, if none is provided in the **Input Socket**. |

#### Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| `Body` | **String** | The body of the _HTTP_ request. |

### HEAD

![The HTTP Client Node using Method HEAD.](../../../.gitbook/assets/httpheadupdatedimage.png)

**HEAD** requests the headers on the desired server in order to gather information about the data, but not the content of the data itself. More information on the different *HTTP* methods can be found in the **External Links** section. All **Attributes** and **Inputs** are the same as the common **Attributes**. 

### DELETE

![The HTTP Client Node using Method DELETE.](../../../.gitbook/assets/httpdeleteupdatedimage.png)

**DELETE** deletes data on the desired server per the *HTTP* protocol. More information on the different *HTTP* methods can be found in the **External Links** section. All **Attributes** and **Inputs** are the same as the common **Attributes**, except for the addition of the following:

#### Attributes

![The HTTP Client Node Attributes using Method DELETE.](../../../.gitbook/assets/httppostattributesreal.png)

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Default Body` | **String** | The body of the _HTTP_ request, if none is provided in the **Input Socket**. |

#### Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| `Body` | **String** | The body of the _HTTP_ request. |

## See Also

* [**Using APIs to Pull Dynamic Data**](../../../demo-projects/using-apis-to-pull-dynamic-data.md)

## External Links

* [Different *HTTP* Methods](https://www.w3schools.com/tags/ref_httpmethods.asp) on W3Schools.