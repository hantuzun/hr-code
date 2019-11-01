<img src="github_url_hr_code.png" width="120">
  
# HR code
**Human Response Code**: Designed to be recognized by humans and OCR. Encodes all valid URL characters to images.

## Specification

### Overview

 * HR Codes a rectangle images.
 * HR Codes are sorrounded by a border.
 * HR code is read from left to right and from top to bottom, just as English.
 * There must be an rightwards arrow on the top left.
 * Each character occupies the same square size.
 * Characters are separated by a constant size padding, which creates an uniform grid.

### Characters

 * All valid characters for URLs are also valid HR code characters.
 * The complete list of characters is: `A-Z`, `a-z`, `0-9`, `-`, `.`, `_`, `~`, `:`, `/`, `?`, `#`, `[`, `]`, `@`, `!`, `$`, `&`, `'`, `(`, `)`, `*`, `+`, `,`, `;`, `%`, and `=`.
 * Updates in [RFC 3986 (Uniform Resource Identifier (URI): Generic Syntax)](https://www.ietf.org/rfc/rfc3986.txt) could require HR code to support additional characters.

### Colors

 * Black for character strokes, the borders, the initial arrow background, and the padding between the initial arrow and the borders.
 * White for character backgrounds and the initial arrow stroke.
 * Light gray (`#aaa`) for the padding between character backgrounds, which creates a gray grid.
 * Trailing empty character spaces, if any, are filled with light gray, not white.

### Layout

 * A text of `n` characters should be placed into a square HR code with the following number of rows and columns: `√(n+1)` rounded up to the smallest integer.
   * For example, 100 chracters should be placed into a square of 11x11 characters. since `10 < √101 <= 11`.
 * Borders and grid paddings are 1 unit.
 * Character backgrounds are 7 x 7 units.
  


## Examples

### Some characters

The following characters generate the HR code below them:

```
➡️ABC
DE01
%?#@
$&.;
```

<img src="example_hr_code.png" width="175">

### This url `https://github.com/hantuzun/hr-code`

The HR code above is the rendering of this url in the format below:

```
➡️https
://git
hub.co
m/hant
uzun/h
r-code
```

<img src="github_url_hr_code.png" width="255">
