# Sprite

## Size

`Size` simply determines the dimensions of a graphic. As **Sprite Objects** are two-dimensional, the `Z` **Value** doesn't actually have any effect.

If you want to display the graphic with the precise pixel resolution, you should ensure that `Size` matches the file's pixel dimensions, and that the **Object's** `Position` **Transformation** place it on the same plane as the **Scene's** **Camera**.

The dimensions should be correct by default when you create a new **Sprite** **Object**, by dragging a graphic from the **Asset Manager**.

## Alpha

`Alpha` determines the opacity of a **Sprite** with 0 being completely transparent and 1 being completely opaque.

![](../../../.gitbook/assets/sprite-alpha.gif)

## Flip U / Flip V

The horizontal and vertical coordinates in most *2D* graphics programs are referred to as XY-coordinates. In *3D* applications, though, it is conventional to call these UV-coordinates to differentiate between *3D* _mesh_ transformation coordinates and *2D* _texture_ transformation coordinates.

The `Flip U` and `Flip V` **Attributes** simply invert the direction of the corresponding axis, meaning that `Flip U` flips a **Sprite** _horizontally_, while `Flip V` will flip it _vertically_.

![](../../../.gitbook/assets/sprite-uv.gif)

## Sort Index

Because **Incari** works in _3D_, it has no way of automatically discerning the layering order of different elements that occupy the same area in _3D_ space. It is therefore necessary to manually define the _sort order_ of **Sprites** to ensure that they are layered correctly.

This is done by manipulating the `Sort Index`. **Sprites** with higher values will be rendered above lower values. If **Sprites** have the same `Sort Index` **Value**, then there is no guarantee that they will be shown correctly, and it is therefore recommended that you assign a unique **Value** to each **Sprite** unless you are certain that they will never overlap one another.

![](../../../.gitbook/assets/sprite-sort-index.gif)

## File

This is an [**Asset / Object Attribute**](../attribute-types/asset-object-attribute.md) that links the **Object** to an imported **Asset**. This should be assigned by default, when you use the drag-and-drop method to create the **Sprite Object**, but you can assign it manually by dragging a graphic from the **Asset Manager** onto the `File` slot.

