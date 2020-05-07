# FreeCAD_macros
My and collected macros for FreeCAD - directly from ~/.FreeCAD/Macro

Some macros are not written by me, but copied from other sources. Please inspect the licence of those files individually!

Most of my macros are designed to work with a Python3/QT5 build of FreeCAD!
Please use a modern version like 0.18 which supports both!

# Add the Macros to your toolbar:

Follow the instructions in the FreeCAD wiki regaring [Toolbar Customization](https://wiki.freecadweb.org/Customize_Toolbars).
Do not forget to add the `icons` folder in order to use the provided icons for
the macros.

## TDCustomFormat.FCMacro

This macro is intended to be used in the TechDraw Workbench.
It allows you to set the FormatSpec of a dimension enhanced with some common CAD
symbols.

To use the macro, select one or more dimensions you want to change the
FormatSpec.
Execute the macro and click on the symbols you want to enhance the format string
with. Symbols are inserted at the current cursor position, which is the
beginning by default.
Then click OK to set the format string.

Note on the `g` format string: In my opinion the `g` format has an advantage
over `f` as it removes trailing zeros from the string. One disadvantage is, that
you can only specify the total number of decimal places and that it will switch
to exponential format if the value is too large.


## TDChainDistances.FCMacro

With this macro you can properly align dimensions to be used as chain measures.
It also aligns the dimension value to the center of the line, if it was moved
before.

Select at least one dimension line which shall be aligned.
Only DistanceX and DistanceY are supported.


## TDEdgeIntersection.FCMacro

This macro is intended to be used in the TechDraw Workbench.

Select two Edges of a DrawViewPart to compute the intersection point.
A cosmetic vertex is created at the point of intersection.

You will get an error message if:

* a different number than two edges is selected
* the lines are parallel


## TDTangentialMeasure.FCMacro

This macro is intended to be used in the TechDraw Workbench.

The idea is to be able to create dimensions between tangents of two arcs.
A third axis has to be chosen as the perpendicular axis for the tangents.

As TechDraw can not create dimensions along an arbitrary axis (yet), the macro creates four cosmetic
vertices in order to use the normal distance dimension tool.



# Licence

All my macros are released under MIT Licence.


Work based on other projects:

* `EdgeIntersection.svg`: Based on [techdraw-2linecenterline.svg](https://github.com/FreeCAD/FreeCAD/blob/941968b37cd45505a5668a1df17ba9b8d6f9a66b/src/Mod/TechDraw/Gui/Resources/icons/actions/techdraw-2linecenterline.svg)
* `TDChainDistances.svg`: Based on [techdraw_dimension_horizontal.svg](https://github.com/FreeCAD/FreeCAD/blob/291bad6cba925cb2a69033ce0d9f748814348398/src/Mod/TechDraw/Gui/Resources/icons/TechDraw_Dimension_Horizontal.svg)
