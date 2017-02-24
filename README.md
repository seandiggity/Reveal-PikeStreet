# 'Creative' Theme for Reveal.js
This is a fancy theme for Reveal.js, based heavily upon 'Pike Street' by Felix Rieseberg, and including some [Creative Commons](https://creativecommons.org) flair.

The theme uses EB Garamond and Muli, falling back to well-known serif and sans-serif fonts (respectively) if these aren't available.

![Screenshot](https://github.com/seandiggity/reveal-creative/raw/master/screenshot-example.png)

**To get started, just open up `index.html` and edit the slides. Every `<section>` is a slide.**

* [Markdown](#markdown)
* [Graphics](#graphics)
* [Code Highlighter & Editor](#codeedit)
* [Speaker Notes](#speaker-notes)
* [Disabling the Controls](#disabling-the-controls)

## Features and Hints

### Markdown
Reveal.js is capable of creating a presentation directly from Markdown, either from an external file or by writing your slide directly in Markdown. 

```
<section data-markdown>
    <script type="text/template">
        ## Page title

        A paragraph with some text and a [link](http://hakim.se).
    </script>
</section>
```

#### External Markdown
The files `index_markdown.html` and `presentation.md` showcase how to do use an external file. There is one limitation: External markdown files are only supported if served from any kind of web server. If you install all development dependencies for this project, `grunt serve` will be one of those servers - alternatively, you should know that Python enables you to always start a small http server in any directory by calling `python -m SimpleHTTPServer` (Python 2.7) or `python -m http.server` (Python 3+). 

### Graphics
I recommend the following sites for some nice photos. All of them are Creative Commons zero-licensed (CC0), meaning that you can do whatever you want with them (including using them in a presentation). Patterns are a bit more difficult to find, but I recommend [The Pattern Library](http://thepatternlibrary.com/).

* [Little Visuals](http://littlevisuals.co/)
* [Unsplash](http://unsplash.com/)
* [Death to the Stock Photo](http://join.deathtothestockphoto.com/)
* [New Old Stock](http://nos.twnsnd.co/)
* [Picjumbo](http://picjumbo.com/)
* [Gratisography](http://www.gratisography.com/)
* [Getrefe](http://getrefe.tumblr.com/)
* [Jay Mantri](http://jaymantri.com/)
* [Magdeleine](http://magdeleine.co/)
* [Picography](http://picography.co/)
* [Raumrot](http://www.raumrot.com/10/)
* [ISO Republic](http://isorepublic.com/)

### Code Highlighter & Editor <a name="codeedit"></a>
Highlighting is provided by Highlight.js. Included are three popular color schemes (Visual Studio, Zenburn, and GitHub), [but more styles are available online](https://highlightjs.org/static/demo/). To change the used CSS file, open up `index.html` and change the stylesheet in line 21 from `github.css` to `visualstudio.css`, `zenburn.css` or whatever Hightlight.js theme you put into `/lib/css`.

### Make Code Editable
You know what's really cool? Casually clicking into your code and changing a few things. By default, adding the attribute `contenteditable` to your code block makes it automatically editable.

```
<pre>
    <code data-trim contenteditable>
var hi = "I'm some code!";
    </code>
</pre>
```

If you want to be really cool and run the code you just entered, you can either go with a custom solution - alternatively, you can use online code editors. A normal `iframe` will work, but so will embedded components. For example, this slide shows how to code and run TypeScript from within the presentation.

### Speaker Notes
reveal.js comes with a speaker notes plugin which can be used to present per-slide notes in a separate browser window. The notes window also gives you a preview of the next upcoming slide so it may be helpful even if you haven't written any notes. Press the 's' key on your keyboard to open the notes window.

Notes are defined by appending an `<aside>` element to a slide as seen below. You can add the data-markdown attribute to the aside element if you prefer writing notes using Markdown. When used locally, this feature requires that reveal.js runs from a local web server.

```
<section>
    <h2>Some Slide</h2>

    <aside class="notes">
        Oh hey, these are some notes. They'll be hidden in your presentation, but you can see them if you open the speaker notes window (hit 's' on your keyboard).
    </aside>
</section>
```

If you're using the external Markdown feature, you can add notes by just writing `Note:`.

```
# Title
## Sub-title

Here is some content...

Note:
This will only display in the notes window.
```

### Disabling the Controls
Go into `js/creative.js` and set `controls` to `false` (line 5).

## Development
On Unix systems, simply calling `npm install` installs all required development dependencies to mess with the code (more information can be found at [reveal.js](https://github.com/hakimel/reveal.js/#installation). On Windows, installation is made a bit more difficult - one of the required modules, `node-sass`, requires compilation with Visual Studio 2013. Install Visual Studio 2013 and run `npm install --msvs_version=2013`.

## Licensing
'Pike Street' theme by [Felix Rieseberg](http://www.felixrieseberg.com) was released under the [MIT/Expat license](https://opensource.org/licenses/MIT).

'Creative' and 'Yale' themes by [Sean O'Brien](https://webio.me) are released under the [GNU Affero GPLv3](https://www.gnu.org/licenses/agpl-3.0.html) or any later version. For more details, see `LICENSE`.

Creative Commons logos are subject to a [trademark policy](https://creativecommons.org/policies/) that specifies you download the images directly from 
[https://creativecommons.org/about/downloads/](https://creativecommons.org/about/downloads/).  Unless otherwise noted, content from [creativecommons.org](https://creativecommons.org) is licensed under a [Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/).

The Creative Commons heart graphics in `assets/caring-is-sharing.svg` and `patternbg-creative-commons.png` were redrawn by Sean O'Brien from the [CC 'donate' heart](https://creativecommons.org/wp-content/uploads/2014/02/heart-donatepage.png).  They are licensed under a [Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/).

Other licensing information is included alongside specific components, so please browse the directories before appropriating or remixing.  For example, the font 'Source Sans Pro' is released under the SIL Open Font License, whose text is in the `LICENSE` file alongside the font files.

