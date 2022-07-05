# Lights

**Incari** has three types of **Light Objects**: the **Spot Light**, the **Point Light**, and the **Directional Light**.

The **Point** **Light** is _omnidirectional_, meaning that light is emitted equally in all directions; the **Spot Light** is _directional_ and will only light the area that it is rotated towards; and when a **Directional Light** is used, the rays of light are parallel to each other, illuminating as if from a far off distance and lighting objects equally, like the sun. Additionally, **Spot Light** and **Directional Light** support shadow mapping and have an extra set of **Attributes** for that purpose. On the other hand, this is not possible for **Point Light**.

| Attribute | Spot Light | Point Light | Directional Light |
| :--- | :--- | :--- | :--- |
| `Color` | ✔ | ✔ | ✔ |
| `Brightness` | ✔ | ✔ | ✔ |
| `Attenuation` | ✔ | ✔ | ✘ |
| `Radial Falloff` | ✔ | ✘ | ✘ |
| `Shadow Mapping` | ✔ | ✘ | ✔ |

### Color

`Color` determines the color of the light being emitted.

Please note that the `Color` **Attribute's** _brightness_ level will affect the brightness of the light itself. It is recommended that you always have the brightness level set to 1 and use the actual `Brightness` **Attribute** to alter the intensity of the light.

`Color's` _alpha_ level has no effect.

### Brightness

`Brightness` governs the intensity of the light, with lower values giving less intense light emission and vice versa.

![](../../.gitbook/assets/brightness.gif)

### Attenuation

`Attenuation` relates to the spread, or reach, of the light. Lower levels only illuminate close **Objects**, whereas high levels allow the light to reach **Objects** that are further away.

![](../../.gitbook/assets/attenuation.gif)

### Radial Falloff

`Radial Falloff` is used to change the smoothness of the light falloff. Lower levels will give a smoother transition between light and dark areas, but will be darker overall. Higher levels give a more contrasting light-to-dark transition and will appear comparatively brighter.

This **Attribute** is only available on the **Spot Light Object**.

![](../../.gitbook/assets/radialfalloff.gif)

## Shadow Mapping

**Shadow Mapping** is a method of approximating shadows in real-time. **Shadow Mapping** takes the depth and normal passes of the **Scene** from the perspective of the **Spot Light** or **Directional Light**, calculates which areas are occluded, and projects the shadow map onto the **Scene**.

There is no 'one size fits all' setup for **Shadow Mapping**. It is invariably a matter of tweaking and adjusting to achieve the desired visual result for your **Scene**, as well as meeting the _performance_ requirements of your **Project**.

### Enable

**Shadow Mapping** can be turned off/on using the `Enable` switch. Whether or not you use this effect often comes down to performance. If you are having performance issues, then you should consider removing the effect, or adjusting the other settings.

### Resolution

`Resolution` alters the size of the shadow map. Just like with normal *2D* textures, higher resolutions produce better quality, at the cost of increasing processing time and file size.

![](../../.gitbook/assets/resolution.gif)

### Kernel Size

`Kernel Size` relates to the size of each sampled area during the calculation. It affects the smoothness of the shadow map. Lower levels give crisp, but jagged, shadows; higher levels give smoother, but less defined results.

Increased `Kernel Size` may help improve results that suffer from _shadow acne_ or reduce artifacts in cases where the shadow map `Resolution` is low.

![](../../.gitbook/assets/kernel-size.gif)

### Clip Near

As stated above, **Shadow Mapping** takes passes from the **Light's** perspective. Like the `Clip Near` **Attribute** of **Camera**, everything within the defined distance isn't rendered and is therefore excluded from those passes and the **Shadow Mapping** algorithm.

![](../../.gitbook/assets/clip-near.gif)

### Offset

`Offset` offsets the depth of the shadow map and can improve its appearance by reducing _shadow acne_. It is recommended that you increase this value by very small increments \(0.0001\), until you get an acceptable reduction in artifacts.

Due to the effect `Offset` has on the **Shadow Mapping** algorithm, higher values can cause shadows to appear to become disconnected from the geometry that casts them.

![](../../.gitbook/assets/offset.gif)

