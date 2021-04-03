# Read: 05 - HTML Images; CSS Color & Text  

## From the Duckett HTML book:  
### Chapter 5: Images (pp.94-125)  
- You might need insert these types of image in the website (logo, photograph, illustration, diagram, or chart.)
-  `<img>` used to add image and this is an **empty element**(has no closing tag).
- suntax `<img src="URL" alt="alternate text" title="title" />`
- `<img>` element attributes:
1. `src` -> image source.
2. `alt` -> a text description of the image that describes the image it not seen.
3. `title`
4. `height`
5. `width`

- Three rules to remember when you are creating images:
1. Save images in the right format (whether jpg,gif and png).
2. Save images at the right size(if it is smaller than intended-> might be distorted and stretched./ larger than intended -> will take longer to display on the page.)
3. Use the correct resolution.

- Tools to Edit & Save Images -> ensure that the images are the right size, format, and resolution. *ex: * Adobe photoshop.
- JPEGs -> best for Photographs.
- Gif -> best for illustrations or logos.
- Vector images -> are used for creating logos, illustrations and print layouts.
- Animated GIFs -> show several frames of an image in sequence.

- `<figure>` -> we can use it to insert img element and caption.
- `<figcaption>` ->  for figure caprion, can be inside `<figure>`.

### Chapter 11: Color (pp.246-263)  
-  Three ways to specify colors in CSS:
1. RGB Values.
2. Hex Codes.
3. a color name.

- **color pickers** enables us to find any color.
-  A contrast between background and foreground colors; important for readability.
1. With (Low Contrast) -> text is harder to read. 
2. (high Contrast) -> becomes easier to read. 
3. (Medium Contrast) -> For long spans of text, we can improve readability by reducing the contrast a little.

- **Opacity** -> rgba(alpha value-> between 0.0 and 1.0 ): just like RGB value, but the fourth value is alpha value that indicates opacity; .5 = 5%.

- HSL Colors:
1. Hue -> a degree on the color circle from 0 to 360.
2. saturation -> is the amount of gray in a color; 100% full saturation & 0% shade to gray.
3. lightness -> "is the amount of white (lightness) or black (darkness) in a color." -0% lightness is black, 100% lightness is white-

- an opacity value for HSL is HSLA.

---
### Chapter 12: Text (pp.264-299)
- Typeface Terminology :
1. Serif -> extra details on the ends of the main strokes of the letters.
2. Sans-Serif -> s have straight ends to letters.
3. Monospace ->   font is the fixed width.
4. `Weight` -> has a values of Light, Medium, Bold, and Black.
5. `Style` values -> Normal, Italic, and Oblique. 
6. `Stretch` values -> Condensed, Regular, and Extended.

-Specifying Typefaces:
1. `The font` -family property.
2. `font-size` -> insert a number with (px or % or em or pt)
3. `@font-face` -> for more font choice; specify inside it a `font-family` and `src` to use a font not install in a person's computer.
4. `text-transform` -> uppercase, lowercase, and capitalize.
5. `text-decoration` -> none, underline, overline, line-through, and blink.
6. `line-height` -> "Leading (pronounced ledding) " which define a vertical space between lines. *ex* line-height:3px;
7. `letter-spacing` -> Kerning: a space between each letter.
8. `word-spacing` -> space between each word.
9. `text-align` -> left, right, center, and justify.
10. `vertical-align` -> baseline, sub, super, top, text-top, middle, bottom, and text-bottom.
11. `text-indent` -> indent first line of the text. *ex:* text-indent:15px;
12. `text-shadow` -> create a drop shadow. *ex:* text-shadow: 1px 1px 0px #000000;
**first value:** " length indicates how far to the left or right the shadow should fall", **second value:** "indicates the distance to the top or bottom that the shadow should fall. **third value:** (optional)- for amount of blur. **last value:** the color of the drop shadow.
13. `:first-letter`, `:first-line` -> specify  different values for the first letter or first line. *example from book:* p.intro:first-letter {font-size: 200%;}
14. `:link`, `:visited` -> for link styling.
15. `:hover`, `:active`, `:focus` -> "specify appearance of elements when a user is interacting with them."

<!-- go to table page 299-->

## From Blog Post
### JPEG vs PNG vs GIF  
- JPEG, PNG and GIF format comprise more than 95% of all images loaded on websites.
#### TL;DR (Too Long; Didn't Read)
1. JPEG format -> for all images that contain a natural scene or photograph.
2. PNG format->  for images that needs transparency or for images with text & objects with sharp contrast edges *ex*: logos.
3. GIF format -> for images that contain animations.

#### Compression types :
1. Lossless compression -> when image compressed image,  there is no information loss during compression; so with decompression an image will appear like before a compression.
2. Lossy compression ->  compression ratio comes at a cost of reduced quality(some of the data from the original file is lost).

- JPEG is a lossy compression.
- PNG is a lossless image format using DEFLATE compression.
- GIF is also a lossless image format that uses LZW compression algorithm. 

#### Transparency
like when we need a transparent background in logos.
- JPEG images don’t support transparency.
- PNG images support transparency in two ways — inserting an alpha channel that allows partial transparency(ideal with images with transparent background ) or by declaring a single colour as transparent (index transparency).
- GIF images support transparency by declaring a single colour in the colour palette as transparent (index transparency) so not ideal in all cases.

#### Colours
- JPEG images can support around 16 million colours. 
- PNG images mainly have two modes:
1. PNG8 -> can support up to 256 colours. (used for simple shapes with fewer colours)
2. PNG24 can support up to 16 million colours. Use PNG8  and PNG24 (used for high quality, complex logos and shapes with rounded corners on a transparent background).
3. GIF images ->  256 colours. If index transparency is used.

#### Animation
"Animation: is Any change or movement in the image. It doesn’t necessarily have to have frame rates like an animated video"
- only GIF supports animation.



