# SASS Mixin

This is a small selection of some SASS mixins I haven't been able to find anywhere else. The collection of mixins will be expanded upon over time.
For examples of the different mixins, check the `example` folder.

## Mixins

### text-close-shade( `depth`, `color`, `printer-shade` )

`text-close-shade` creates closed shades on text. The idea came from [Tim Brown's excellent article on TypeKit's blog](http://blog.typekit.com/2011/07/19/shading-with-css-text-shadows/).

| Parameters     | Accepted Data Types | Required? |
|----------------|---------------------|-----------|
| depth          | `int`               | Yes       |
| color          | `string`, `list`    | Yes       |
| printer-shade  | `boolean`           | No        |

### underline( `color`, `baseline`, `thickness`, `background` )

`underline` creates a "smart" underline on your text, that will clear descenders using a mix of a linear gradient background and a text shadow. This can only be used on solid colored backgrounds and can be very resource intensive on longer paragraphs of text.

| Parameters     | Accepted Data Types | Required? |
|----------------|---------------------|-----------|
| color          | `string`            | Yes       |
| baseline       | `int`               | Yes       |
| thickness      | `int`               | No        |
| background     | `string`            | No        |

## Instructions

    // Import the mixin file
    @import "mixins";

    // Use the mixins
    @include text-close-shade(6, #8E432B);

## License

Copyright (c) 2016 Briix

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
