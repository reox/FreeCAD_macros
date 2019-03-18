# FreeCAD_macros
My and collected macros for FreeCAD - directly from ~/.FreeCAD/Macro

Some macros are not written by me, but copied from other sources. Please inspect the licence of those files individually!

Most of my macros are designed to work with a Python3/QT5 build of FreeCAD!
Please use a modern version like 0.18 which supports both!


## CustomFormat.FCMacro

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

