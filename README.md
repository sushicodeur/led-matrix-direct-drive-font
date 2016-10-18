# Font for Arduino's Direct Drive LED Matrix tutorial

This is an pretty complete font to use with 8x8 Led Matrix as proposed here : http://playground.arduino.cc/Main/DirectDriveLEDMatrix

The font is based on Neale Davidson's "[Emulator Normal](http://www.urbanfonts.com/fonts/Emulator.htm)" font.

All alpha-numerics characters are presents as well as the main special characters.

## What's included

In `EmulatorFont.h` :

* `SPACE`
* `A` to `Z` : Take care of `F` letter (see bellow)
* `0` to `9` : `NUM_0` ... `NUM_9`

In `EmulatorFontSpecialChars.h` :

* `EXCLAM`, `DBL_QUOTE`, `SHARP`, `DOLLAR`, `PERCENT`, `AND`, `QUOTE`, `OPEN_PARENTHESIS`, `CLOSE_PARENTHESIS`, `ASTERISK`, `PLUS`, `COMA`, `MINUS`, `DOT`, `SLASH`, `COLON`, `SEMICOLON`, `LESS`, `EQUAL`, `MORE`, `QUESTION`, `AROBASE`, `OPEN_BRACKET`, `BACKSLASH`, `CLOSE_BRACKET`, `TILDE`, `UNDERSCORE`, `OPEN_CURLY`, `PIPE`, `CLOSE_CURLY`

## How to use

Follow this link http://playground.arduino.cc/Main/DirectDriveLEDMatrix this code is to use with the example `"Show messages on an 8x8 led matrix, scrolling from right to left."`

Just include the file you want to use in your Arduino sketch :

```
#include "EmulatorFont.h"
#include "EmulatorFontSpecialChars.h"
```

Delete the #define SPACE ... O from the sample.

Then you can use any letter in your pattern,

```
byte patterns[numPatterns][8][8] = {
  E, M, U, L, A, T, O, R, SPACE, _F, O, N, T
};
```

> Note : as `F` was already defined in Arduino, I renamed the Object `_F`
