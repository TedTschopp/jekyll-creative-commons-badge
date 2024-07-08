# jekyll-creative-commons-badge
A modular Jekyll include for displaying Creative Commons license badges.

## How to use
- Place the `creative-commons.html` file in your Jekyll `_includes` folder.
- Place either the `creative-commons.css` or the minified `creative-commons.min.css` stylesheets wherever you host your CSS files.
- Import the CSS files wherever you plan on using the include, either before the closing `</head>` tag or directly before the include.
- Implement the badge by placing the include where you want to use it. (ex. `{% include creative-commons.html %}`)

The badge icons are provided courtesy of [Creative Commons](https://creativecommons.org/share-your-work/). No external imports or local storage of image files are required: the SVG files were converted to base64 encoded data URIs and are used in the CSS files directly.

### Include parameters
The badge include has two required parameters: `terms` and `url`. The `terms` parameter helps define the badges to use and the `url` parameter should be a link to the Creative Commons page for the license you're referencing.

The `terms` parameter has the following available strings:

- `by`: Attribution
- `nc`: Non-commercial
- `sa`: Share-alike
- `nd`: No derivitives
- `zero`: CC0 - public domain

To use these strings for the `terms` parameter, separate them by a space (eg. `terms="by nc sa"`)

#### Examples
Display a badge for the Creative Commons BY-NC-SA license:
```liquid
{% include creative-commons.html terms="by nc sa" url="https://creativecommons.org/licenses/by-nc-sa/4.0/" %}
```
... or the CC0 (public domain) license:
```liquid
{% include creative-commons.html terms="zero" url="https://creativecommons.org/publicdomain/zero/1.0/" %}

```
