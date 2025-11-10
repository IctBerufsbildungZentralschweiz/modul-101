# HTML Strukturelement \<div>

#### HTML

**HTML Preprocessor**

**About HTML Preprocessors**

HTML preprocessors can make writing HTML more powerful or convenient. For instance, Markdown is designed to be easier to write and read for text documents and you could write a loop in Pug.

[Learn more](https://blog.codepen.io/documentation/editor/using-html-preprocessors/) · [Versions](https://codepen.io/versions/)

{% tabs %}
{% tab title="None" %}
None
{% endtab %}

{% tab title="Haml" %}
Haml
{% endtab %}

{% tab title="Markdown" %}
Markdown
{% endtab %}

{% tab title="Slim" %}
Slim
{% endtab %}

{% tab title="Pug" %}
Pug
{% endtab %}
{% endtabs %}

**Add Class(es) to**

**Adding Classes**

In CodePen, whatever you write in the HTML editor is what goes within the `<body>` tags in [a basic HTML5 template](https://blog.codepen.io/documentation/features/preview-template/). So you don't have access to higher-up elements like the `<html>` tag. If you want to add classes there that can affect the whole document, this is the place to do it.

**Stuff for**

**About the**

In CodePen, whatever you write in the HTML editor is what goes within the `<body>` tags in [a basic HTML5 template](https://blog.codepen.io/documentation/features/preview-template/). If you need things in the `<head>` of the document, put that code here.

{% hint style="warning" %}
Insecure Resource — The resource you are linking to is using the 'http' protocol, which may not work when the browser is using https.
{% endhint %}

↑ Insert the most common viewport meta tag

***

#### CSS

**CSS Preprocessor**

**About CSS Preprocessors**

CSS preprocessors help make authoring CSS easier. All of them offer things like variables and mixins to provide convenient abstractions.

[Learn more](https://blog.codepen.io/documentation/editor/using-css-preprocessors/) · [Versions](https://codepen.io/versions/)

{% tabs %}
{% tab title="None" %}
None
{% endtab %}

{% tab title="Less" %}
Less
{% endtab %}

{% tab title="SCSS" %}
SCSS
{% endtab %}

{% tab title="Sass" %}
Sass
{% endtab %}

{% tab title="Stylus" %}
Stylus
{% endtab %}

{% tab title="PostCSS" %}
PostCSS
{% endtab %}
{% endtabs %}

[Need an add-on?](html-strukturelement-less-than-div-greater-than.md#0)

**CSS Base**

**About CSS Base**

It's a common practice to apply CSS to a page that styles elements such that they are consistent across all browsers. We offer two of the most popular choices: [normalize.css](http://necolas.github.io/normalize.css/) and a [reset](http://meyerweb.com/eric/tools/css/reset/). Or, choose **Neither** and nothing will be applied.

* Normalize
* Reset
* Neither

**Vendor Prefixing**

**About Vendor Prefixing**

To get the best cross-browser support, it is a common practice to apply vendor prefixes to CSS properties and values that require them to work. For instance `-webkit-` or `-moz-`.

We offer two popular choices: [Autoprefixer](https://github.com/postcss/autoprefixer) (which processes your CSS server-side) and [-prefix-free](http://leaverou.github.io/prefixfree/) (which applies prefixes via a script, client-side).

* Autoprefixer
* Prefixfree
* Neither

**Add External Stylesheets/Pens**

Any URLs added here will be added as `<link>`s in order, and before the CSS in the editor. You can use the CSS from another Pen by using its URL and the proper [URL extension](https://blog.codepen.io/documentation/url-extensions/).

```
```

[Powered by ![Algolia](https://cpwebassets.codepen.io/assets/settings/algolia-9e1c0c887f4db420704b2a79926864019ef156bcecc9d5774a7e4eaa731fc5b5.svg)](https://www.algolia.com/?utm_source=react-instantsearch\&utm_medium=website\&utm_content=codepen.io\&utm_campaign=poweredby)

**About External Resources**

You can apply CSS to your Pen from any stylesheet on the web. Just put a URL to it here and we'll apply it, in the order you have them, before the CSS in the Pen itself.

You can also link to another Pen here (use the `.css` [URL Extension](https://blog.codepen.io/documentation/url-extensions/)) and we'll pull the CSS from that Pen and include it. If it's using a _matching_ preprocessor, use the appropriate URL Extension and we'll combine the code before preprocessing, so you can use the linked Pen as a true dependency.

[Learn more](https://blog.codepen.io/documentation/editor/adding-external-resources/)

{% hint style="warning" %}
Insecure Resource — You are linking to a resource using the non-secure http:// protocol, which may not work when the browser is using https:// like CodePen enforces.
{% endhint %}

{% hint style="info" %}
URL Extension Required — When linking another Pen as a resource, make sure you use a [URL Extension](https://blog.codepen.io/documentation/url-extensions/) of the type of code you want to link to. Either `.css`, `.js`, or the extension of a matching code processor.
{% endhint %}

\+ add another resource

***

#### JavaScript

**JavaScript Preprocessor**

**About JavaScript Preprocessors**

JavaScript preprocessors can help make authoring JavaScript easier and more convenient.

[Learn more](https://blog.codepen.io/documentation/editor/using-js-preprocessors/) · [Versions](https://codepen.io/versions/)

{% tabs %}
{% tab title="None" %}
None
{% endtab %}

{% tab title="Babel" %}
Babel (includes JSX processing)
{% endtab %}

{% tab title="TypeScript" %}
TypeScript
{% endtab %}

{% tab title="CoffeeScript" %}
CoffeeScript
{% endtab %}

{% tab title="LiveScript" %}
LiveScript
{% endtab %}
{% endtabs %}

**Add External Scripts/Pens**

Any URL's added here will be added as `<script>`s in order, and run _before_ the JavaScript in the editor. You can use the URL of any other Pen and it will include the JavaScript from that Pen.

```
```

[Powered by ![Algolia](https://cpwebassets.codepen.io/assets/settings/algolia-9e1c0c887f4db420704b2a79926864019ef156bcecc9d5774a7e4eaa731fc5b5.svg)](https://www.algolia.com/?utm_source=react-instantsearch\&utm_medium=website\&utm_content=codepen.io\&utm_campaign=poweredby)

**About External Resources**

You can apply a script from anywhere on the web to your Pen. Just put a URL to it here and we'll add it, in the order you have them, before the JavaScript in the Pen itself.

If the script you link to has the file extension of a preprocessor, we'll attempt to process it before applying.

You can also link to another Pen here, and we'll pull the JavaScript from that Pen and include it. If it's using a matching preprocessor, we'll combine the code before preprocessing, so you can use the linked Pen as a true dependency.

[Learn more](https://blog.codepen.io/documentation/adding-external-resources/)

{% hint style="warning" %}
Insecure Resource — You are linking to a resource using the non-secure http:// protocol, which may not work when the browser is using https:// like CodePen enforces.
{% endhint %}

{% hint style="info" %}
URL Extension Required — When linking another Pen as a resource, make sure you use a [URL Extension](https://blog.codepen.io/documentation/url-extensions/) of the type of code you want to link to. Either `.css`, `.js`, or the extension of a matching code processor.
{% endhint %}

\+ add another resource

***

#### Packages

**Add Packages**

Search for and use JavaScript packages from [npm](https://www.npmjs.com/) here. By selecting a package, an `import` statement will be added to the top of the JavaScript editor for this package.

```
```

[Powered by ![Algolia](https://cpwebassets.codepen.io/assets/settings/algolia-9e1c0c887f4db420704b2a79926864019ef156bcecc9d5774a7e4eaa731fc5b5.svg)](https://www.algolia.com/?utm_source=react-instantsearch\&utm_medium=website\&utm_content=codepen.io\&utm_campaign=poweredby)

**About Packages**

Using packages here is powered by [esm.sh](https://esm.sh/), which makes packages from npm not only available on a CDN, but prepares them for native JavaScript ESM usage.

All packages are different, so refer to their docs for how they work.

If you're using React / ReactDOM, make sure to turn on Babel for the JSX processing.

***

#### Behavior

* Auto Save — If active, Pens will autosave every 30 seconds after being saved once.
* Auto-Updating Preview — If enabled, the preview panel updates automatically as you code. If disabled, use the "Run" button to update.
* Format on Save — If enabled, your code will be formatted when you actively save your Pen. Note: your code becomes un-folded during formatting.

#### Editor Settings

**Code Indentation**

* Spaces
* Tabs

**Code Indent width**

1 2 3 4 5 6

**Want to change your Syntax Highlighting theme, Fonts and more?**

Visit [your global Editor Settings](https://codepen.io/settings/editor).

***

### HTML Editor Example

0 unsaved changes

HTML Options

* Format HTML
* View Compiled HTML
* Analyze HTML
* Maximize HTML Editor
* Minimize HTML Editor
* Fold All
* Unfold All

{% stepper %}
{% step %}
### Step 1

```html
xxxxxxxxxx
```
{% endstep %}

{% step %}
### Step 2

```html
<p>Ich bin ein erster Absatz.</p>
```
{% endstep %}

{% step %}
### Step 3

```html
<p>Ich bin ein zweiter Absatz.</p>
```
{% endstep %}

{% step %}
### Step 4

```html
​
```
{% endstep %}

{% step %}
### Step 5

```html
<div class="red">
```
{% endstep %}

{% step %}
### Step 6

```html
    <p>Ich bin ein erster Absatz.</p>
```
{% endstep %}

{% step %}
### Step 7

```html
    <p>Ich bin ein zweiter Absatz.</p>
</div>
```
{% endstep %}
{% endstepper %}

***

### CSS Editor Example

CSS Options

* Format CSS
* View Compiled CSS
* Analyze CSS
* Maximize CSS Editor
* Minimize CSS Editor
* Fold All
* Unfold All

```css
xxxxxxxxxx
```

```css
p {
    background-color: indianred;
}
.red {
    background-color: indianred;
}
```

***

### JS Editor Example

JS Options

* Format JavaScript
* View Compiled JavaScript
* Analyze JavaScript
* Maximize JavaScript Editor
* Minimize JavaScript Editor
* Fold All
* Unfold All

```js
xxxxxxxxxx
```

***

#### Preview / Console

1904px

Clear

***

(Embedded configuration and internal JSON/state data omitted — retained only the user-facing settings, options, links, code samples, and warnings from the original content.)
