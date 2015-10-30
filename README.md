cLEDSprites Instructions
========================


Overview
--------
This class allows you to define sprite shapes using 1, 3, 7 or 15 colour palettes.
The drawing order can be controlled and each sprite can be given its own automatic
motion with options to allow the sprite to be kept in the display area.
Collisions between sprites and display edge detection have also been implemented.
Also multiple images can be set for each sprite with automatic change controls
allowing easy animation.



Initialise
----------
In order to use the class you must have the following header files included in your program:-

	#include <FastLED.h>
	#include <LEDMatrix.h>
	#include <LEDSprites.h>

You must declare an instance of the cLEDMatrix class as this is used to modify the
LED data according to the matrix dimensions and layout.

	cLEDMatrix<32, 16, HORIZONTAL_ZIGZAG_MATRIX> leds;

The LED array is allocated in the matrix class but the address of the array can be obtained by
using '[0]' after the matrix variable name and '.Size()' to obtain the number of LED's:-

	FastLED.addLeds<CHIPSET, LED_PIN, COLOR_ORDER>(leds[0], leds.Size());

Then finally you can declare the cLEDSprites class variable:-

	cLEDSprites Sprites(&leds);

This class is the control class for the Sprites whereas cSprite is the class for defining
individual sprites that can then be registered and used using the cLEDSprites class.

	cSprite Shape(SHAPE_WIDTH, SHAPE_HEIGHT, ShapeData, 1, _1BIT, ColTable, ShapeData);

THERE IS FAR MORE TO BE WRITTEN HERE, BUT FOR NOW HAVE A LOOK AT THE EXAMPLES PROVIDED ;-)
