# 3DViewer-v1.0

![3DViewer-v1.0](https://github.com/Garjelin/3DViewer-v1.0/blob/main/Animation_3.gif)

## Implementation of 3DViewer v1.0

The example of .obj file format:
```
  # List of geometric vertices, with (x, y, z [,w]) coordinates, w is optional and defaults to 1.0.
  v 0.123 0.234 0.345 1.0
  v ...
  ...
  # Texture coordinates (u, [,v ,w]), w is optional and default to 0.
  vt 0.500 -1.352 [0.234]
  vt ...
  ...
  # Normals (x,y,z)
  vn 0.707 0.000 0.707
  vn ...
  ...
  # Parameter space vertices (u [,v] [,w])
  vn 0.707 0.000 0.707
  vn ...
  ...
  # Polygonal face element
  f v1 v2 v3
  f ...
  ...
  # Group
  g Group1
  ...
  # Object
  o Object1
```
### Requirements:
* The program must be developed in C language of C11 standard using gcc compiler. You can use any additional QT libraries and modules;
* The program code must be located in the src folder;
* The program must be built with Makefile which contains standard set of targets for GNU-programs: all, install, uninstall, clean, dvi, dist, tests, gcov. Installation directory could be arbitrary, except the building one;
* The program must be developed according to the principles of structured programming;
* When writing code it is necessary to follow the Google style;
* Prepare full coverage of modules related to model loading and affine transformations with unit-tests;
* There should be only one model on the screen at a time;
* The program must provide the ability to:
  * Load a wireframe model from an obj file (vertices and surfaces list support only);
  * Translate the model by a given distance in relation to the X, Y, Z axes;
  * Rotate the model by a given angle relative to its X, Y, Z axes;
  * Scale the model by a given value;
* GUI implementation, based on any GUI library with API for C89/C99/C11
  * For Linix: GTK+, CEF, Qt
  * For Mac: GTK+, Nuklear, raygui, microui, libagar, libui, IUP, LCUI, CEF, Qt;
* The graphical user interface must contain:
  * A button to select the model file and a field to output its name;
  * A visualisation area for the wireframe model;
  * Button/buttons and input fields for translating the model;
  * Button/buttons and input fields for rotating the model;
  * Button/buttons and input fields for scaling the model;
  * Information about the uploaded model - file name, number of vertices and edges;
* The program must correctly process and allow user to view models with details up to 100, 1000, 10,000, 100,000, 1,000,000 vertices without freezing (a freeze is an interface inactivity of more than 0.5 seconds).
