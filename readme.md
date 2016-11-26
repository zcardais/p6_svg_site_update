# Project Instructions
There are 9 steps to this project:

1. Replace the background pattern PNG with the matching SVG (background.svg). Use CSS to resize the SVG to match the original design. *Complete.*

2. Replace rasterized PNG logo with the SVG logo image of the same size (logo.svg): use the inline SVG method to add it (you'll use CSS to modify the image). *Complete.*

3. At a page width of less than 420 pixels remove the text from the logo and add an H1 tag that contains the logo text. *Complete.*

4. Replace dogs with SVG images of the same size using the <img> tag. *Complete.*

5. Change icons in the menu from rasterized images to inline SVGs keeping the original image size the same. *Complete.*

6. When a user hovers over a nav menu item, use CSS to change the color of both the text and the inline SVG. *Complete.*

7. When submitting your project be sure to make a note in the comments which browsers and versions you have tested with. *Complete.* NOTE: Testing completed on Chrome version 54.0.2840.98 (64-bit), Safari version 10.0.1 (12602.2.14.0.7), and Firefox version 47.0.

8. And remember you can only use an 'ID' once so double check the SVG images when adding them. *Complete.*

9. Make sure to check your code is valid by running it through an HTML and CSS validator. *Complete.*

  - Links to the validators can be found in the Project Resources. This will help you spot any errors that might be in your code.

  - *There are a few exceptions that you don’t need to fix:*

    - Don’t worry about any warnings, we just need you to check any errors that might be there.

    - If CSS validator flags use of calc, vendor prefixes or pseudo-elements/pseudo-classes these errors should be ignored.

    - If HTML validator flags use of pipe (‘|’) in Google font links/URLs this error can also be ignored.

    - The CSS Validator does not recognize the SVG attributes like fill as valid attributes. Take a look at the [SVG Attribute](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute) Reference for SVG attributes that are acceptable even if they do not pass the validator.

## Notes from SVG Courses

### Creating an Animated Line Drawing
  - Add a `stroke` to the `path`
  - Set `stroke-dasharray` equal to path's total length
  - Set `stroke-dashoffset` the same as `stroke-dasharray`
  - Animate `stroke-dasharray` to 0

### Example
    /* --------------------------
      Keyframes
    --------------------------- */

    @keyframes offset {
      100% {
        stroke-dashoffset: 0;
      }
    }

    @keyframes fill-it {
      100% {
        fill: #6fbc6d;
      }
    }

    /* --------------------------
      SVG Styles
      --------------------------- */

    svg {
      display: block;
      margin: 2em auto 0;
      width: 40%;
    }

    .logo {
      stroke: #6FBC6D;
      stroke-width: 2;
      stroke-dasharray: 810;
      stroke-dashoffset: 810;

      animation: offset 5s linear forwards, fill-it .8s 5s forwards;
    }
`
