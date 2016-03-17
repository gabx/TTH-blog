# TTH-blog
Back and front end for blog.thetradinghall.com.

## FRONT-END

Files `TTH-blog_basic.html` and `css/TTH-blog_basic.css` are the basis for TTH blog
page. Most important elements have been framed with color to highlight them. You can see
this template in action at this link.


### Template

The template used for the blog is [material design lite](https://www.getmdl.io/), written by GOOGLE. Some more ideas come from [w3schools](http://www.w3schools.com/w3css/demo_template_blog.htm) blog template and [callmenick](http://callmenick.com/) blog and tutorials.

### Guiding rules
#### Style
* Mobile first: it’s easier to add to a design than to take away. By starting
with a minimum configuration, you can then add in more as you gain more space from larger screens
and resolutions.

* Fluid grids: Fluid grid article published in [Alispart](http://alistapart.com/article/fluidgrids)

* Responsive pattern: [__Off-Canvas Left__](http://codepen.io/bradfrost/full/sjiCv) layout tucks a left sidebar away for small screens but exposes it once enough space becomes available. Off canvas multi-device layouts use the space outside a browser’s viewport to hide secondary elements until people need them.

* Holly grail: the [holy grail layout](https://philipwalton.github.io/solved-by-flexbox/demos/holy-grail/) is a page with a header, footer and three columns. The center column contains the main content, and the left and right columns contain supplemental content like ads or navigation.

#### CSS

CSS sheets have been writen following the [__BEM__](https://en.bem.info/method/)(Block Element Modifier) methodology. The overall syntax is:
```
.block {}
.block__element {}
.block__element--modifier {}
```

* Block: a logically and functionally independent page component, the equivalent of a component in Web Components. A block encapsulates behavior (JavaScript), templates, styles (CSS), and other implementation technologies.
Blocks can be nested inside any other blocks.
Blocks can be moved around on a page, moved between pages or projects. The implementation of blocks as independent entities makes it possible to change their position on the page and ensures their proper functioning and appearance.

* Element: a constituent part of a block that can't be used outside of it.

* Modifier: a BEM entity that defines the appearance and behavior of a block or an element.


#### Performance

TO WRITE: with HTTP2, best practice is to split CSS files and load them in sequence.

#### HTML

TO WRITE : header meta data, [Google Webmasters](https://www.google.com/webmasters/#?modal_active=none)


#### Fonts

It is widely advised to stick to the use of no more than two-three fonts. One *serif* can be used for titles and subtitles and one *sans serif* for core text. Usual size is __16px__.


#### Images
SVG is an image format for vector graphics. It literally means Scalable Vector Graphics.

Benefits are:
  1. Small file sizes that compress well
  2. Scales to any size without losing clarity (except very tiny)
  3. Looks great on retina displays
  4. Design control like interactivity and filters


* Drawing: images have been draw using [Inkscape](https://inkscape.org/en/). Inkscape is a free professional quality vector graphics software which runs on Windows, Mac OS X and GNU/Linux.

* Optimization: it's highly recommended to optimize the file first in a [__SVGO__](https://sarasoueidan.com/blog/svgo-tools/) (SVG Optimization) format. Most graphics softwares output SVG with a bunch of unnecessary hoo-ha's that add weight and overall excess baggage. Below is a non exhaustive list of tools:
  - on line: [svgomg](https://jakearchibald.github.io/svgomg/)
  - Linux: [Nodejs-based tool](https://github.com/svg/svgo)
  - Inkscape: save as > `optimized with svgo`

* Color: best practice for mono color pictures is to use the black color when drawing.
Then, use a CSS style to color the text.

* SVG image size can be controlled by the `height` and `width` CSS properties. More informations can be found on this [CSS-Tricks post](https://css-tricks.com/scale-svg/).

* [Grunticon](https://github.com/filamentgroup/grunticon) is a Grunt.js task that makes it easy to manage icons and background images for all devices. grunticon takes a folder of SVG/PNG files (typically, icons that you've drawn in an application like Adobe Illustrator), and outputs them to CSS in 3 formats: svg data urls, png data urls, and a third fallback CSS file with references to regular png images, which are also automatically generated and placed in a folder.

* Fav icon: The browser/webpage looks for favicon.ico in the root directory by default. Best is thus to place it at the root, and declare like this:
`<link rel="icon" href="favicon.ico" type="image/x-icon" />`. [This article](https://css-tricks.com/favicon-quiz/) details all needed formats for the various browsers and devices.
Best is to use online [Favicon Generator](http://realfavicongenerator.net/) to get all of them in an easy and quick manner.
