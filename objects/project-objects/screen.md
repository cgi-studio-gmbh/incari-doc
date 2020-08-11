# Screen

![](../../.gitbook/assets/iconscreen.png)

The **Screen Object** in Incari contains the technical specifications of the physical display that is used to render a **Scene**. Also, it has **Attributes** relating to the virtual **Camera**, the **Simulation Window** and post-processing effects during rendering.

Note: **Screen Objects** pass on **Attributes** to [**Scene Objects**](scene.md) that are created from them.  

## Attributes

A **Screen's Attributes** can be edited by selecting it in the **Project Outliner** and adjusting them in its **Attribute Editor**.

### Transformation

Each **Scene** has the standard **Transformation Attributes**, however it is worth noting that, in order to have two-dimensional **Objects**, such as **Text** and **Sprites**, be displayed correctly, they should have the same **Transformation** as the **Screen** and sit on the same plane.

### Camera

Each **Screen** has a built-in **Camera Object**, with its accompanying **Attributes**. For more information, take a look at the [**Camera**](../scene-objects/camera.md) documentation.

### Simulation Window

`Position` defines the offset position, in pixels, that the **Simulation WIndow** will be displayed on your monitor. This means that when you are working on a multi-display system, you can preview **Screens** on separate parts of your monitor.

By default, the **Simulation Window** will be shown in the left-hand corner of your monitor \(0, 0\), with `x` representing the number of pixels between the left-hand side of the **Simulation Window** and the left-hand side of your monitor, and `y` representing the amount between the top of the window and top of your monitor.

`Scale factor` is a *percent* value that is used to adjust the size of the **Simulation Window**. The default value is *100%* and this ensures that the size of the **Simulation Window** corresponds to the **Screen** size. The **Screen** size can be found in the **Attribute** section of the **Screen**'s **Camera** **Attribute**. Other options for adjusting the size of the **Simulation Window** includes \(75%, 50%, 25%\) of the **Screen** size. 

### Background

The `Color` **Attribute** defines the background color of the **Simulation** and its default value is *solid black*.

### FXAA

**Fast Approximate Anti-Aliasing** \(**FXAA**\) is a post-processing effect, that seeks to smoothen out jagged edges that appear in rendered **Objects**. This helps improve how 2D and 3D **Objects** are displayed. _After_ each frame has been rendered, the effect is applied per-pixel and doesn't consider 3D geometry or know what should be smoothed and what shouldn't. As a result, it may unintentionally smoothen the wrong parts of the image and may not be the best option. It is often a trade-off between improved smoothness of jagged areas of geometry at the loss of some crispness of textures.

In terms of options, `Mode` changes the way the effect is calculated, with `fast` being quicker than `accurate`, which may give better results at the expense of some calculation speed.

`Enabled` enables/disables the effect entirely. Turning the effect off is of course the quickest option, and should be considered if it isn't necessary or you are having performance issues. Another point worth noting is that **FXAA** doesn't consider movement at all, and may produce undesirable results in cases where you have fast-moving objects.

![](../../.gitbook/assets/fxaa.gif)

### SSAO

**Screen Space Ambient Occlusion** \(**SSAO**\) is a post-processing effect, which takes both the _depth_, and _normal_ information of 3D geometry within a **Scene**, to approximate areas of occlusion and exposure to ambient light. What this means is that areas such as corners and cavities are darker, creating a more realistic representation of the way light behaves in the real world.

Like **FXAA**, the effect can be disabled/enabled by toggling the `Enabled` option, but it also has a few extra **Attributes** to consider.

`Radius` defines the spread of darkened areas, with a lower value resulting in smaller, crisper occluded areas, and bigger values producing a darker, but softer result.

`Samples` defines the number of samples to be used in the calculation, with lower values being cheaper in terms of processing time required, at the expense of quality. Higher samples invariably give a better result, but you also sacrifice performance. It often comes down to tweaking the `Radius` and `Samples` values to find the sweet spot between quality and performance.

![](../../.gitbook/assets/ssao.gif)

# See Also
- [**Scene**](scene.md)
- [**Camera**](../scene-objects/camera.md)

# External Links

- [**FXAA**](https://en.wikipedia.org/wiki/Fast_approximate_anti-aliasing) on wikipedia
- [**SSAO**](https://en.wikipedia.org/wiki/Screen_space_ambient_occlusion) on wikipedia.

