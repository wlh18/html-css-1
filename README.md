# Lesson Sections

1. [HTML/CSS I Lecture Notes](#HTMLCSS-I-Lecture-Notes)
1. [Additional Resources](#additional-resources)
1. [HTML/CSS I Mini Project](#HTMLCSS-I-Mini-Project)
1. [HTML/CSS I Afternoon Project](#HTMLCSS-I-Afternoon-Project)

# Student Learning Objectives

### HTML

* Student can describe and create an HTML file (?)
* Student can use the head tag to insert meta information about the page
* Student can insert comments in HTML (?)
* Student can change the title and icon of their webpage (?)
* Student can use the body tag to specify what will be displayed
* Student can use div, p, h1-h6, and span tags to layout a flow of information
* Student can use ol, ul, and li tags
* Student can use nav, footer, and header tags
* Student can use img tags to bring in pictures
* Student can use a tags to route to another webpage
* Student can use link tags to bring in CSS files
* Student can use and describe inline, inline-block, and block level elements (?)
* Student can use the class and id attributes (?)
* Student can utilize and understand the benefits of semantic HTML (?)
* Student can visualize HTML/CSS in terms of boxes/containers (?)

### CSS

* Student can describe what CSS is
* Student can bring in and use a new font in a project
* Student can can use id, class, descendant, child, and addition selectors in CSS to style elements (?)
* Student can use the font, color, and background-color properties (?)
* Student can use text-align property
* Student can use background property to specify colors or images used for backgrounds
* Student can describe the box-model (?)
* Student can explain box-sizing: border-box (?)
* Student can use height, width, margin, padding, and box-sizing properties
* Student can describe the difference between px, %, vh/vw, em, and rem (?)
* Student can use the float property
* Student can use and describe a reset file
* Student can understand and utilize a mockup (?)


# HTML/CSS I Lecture Notes

<details open>
    <summary>Lecture Introduction</summary>
    
In this lecture we introduce HTML and CSS. HTML (HyperText Markup Language) and CSS (Cascading Style Sheets) are two of the building block languages of web applications, and they are considered "front-end" technologies. HTML gives content *structure* and *meaning* by defining the "elements" that the web page is made up of. CSS is a presentational language that is used for only for the *layout* and *styling* of a webpage. JavaScript, together with HTML and CSS, is responsible for bringing our websites to life.

Check out this visual analogy for what HTML, CSS, and JavaScript do respectively: 

![deadpool-HTML-CSS-JS](images/deadpool-HTML-CSS-JS.gif)
    
</details>

## HTML

HTML stands for Hyper Text Markup Language. HTML is used to create the infrastructure of a webpage. HTML is **NOT** a programming language; HTML is considered a "markup" language. HTML does not contain logic, and HTML elements contain very little, if any, native styling. HTML is simply used to specify the structure and basic parts of a page.

>Note: Over the years, there have been many versions of HTML. As of 2014, the most up-to-date version is HTML5, which introduced a number of new features to the language. For more details, see here: https://stackoverflow.com/questions/134727/whats-the-key-difference-between-html-4-and-html-5

### Making an HTML File
<details>
    <summary>Information</summary>
    
HTML files are created by ending the name of a file with an `.html` extension. This extension tells browsers and code editors to read the file as HTML. 

>Note: `index.html` is the standard name for a root HTML file since the browser looks for files called `index` by default.
</details>

### HTML Syntax Overview
<details>
    <summary>Information</summary>

HTML is based around filling "tags" with "content" in order to create HTML "elements".


```html
    <thisisatag>This is the content</thisisatag>
```

Above is the basic syntax of an HTML element.

1. First is the tag itself. HTML tags are declared using angle brackets `<>`, with the name for the tag contained within the `<>` brackets.
2. Most HTML tags come in pairs of opening and closing tags. The closing tag begins with a `/` immediately after the first angle bracket to indicate that it is corresponding closing pair of the HTML tag.
3. Between the angle brackets is where developers specify the type of tag they are using. There are various types of tags native to HTML, which will be covered shortly.
4. Tags are wrapped around the **content** that is stored inside that HTML tag. The content together with the tag creates an HTML element. 

>Note: Some elements are called "self-closing" or "void" elements because their tags should not be written in pairs. This is because they are not designed to contain content. See the example below:
```html
    <input />
```
>Notice that there is only one tag, and it uses a forward slash at the ending of the tag.
</details>

### Basic HTML Page Structure
<details>
    <summary>Information</summary>

Here's an example of a basic HTML page structure: 

```html
<!DOCTYPE html>
<html lang="en">
  <head>
     <!-- Meta tags and external links go here too -->
    <title>Document</title>
  </head>
  <body>
      <!-- Content of page goes inside the body tag -->
  </body>
</html>
```

Now, let's break down the structure seen above.

`<!DOCTYPE html>` - This tag is pretty unique, and it's actually not an HTML element; it's an instruction to a web browser that lets it know what type of file to expect. 
>Note: Always make sure that this is the first declaration in an HTML document, otherwise the page may not work.

`<html>` - The html tag tells the browser that everything contained inside the tag should be read as html. The `lang` "attribute" can be used to specify the human language that the contents are written in. This element will act as the root tag for the file, which means that everything will be contained inside of this tag. 

`<head>` - The head tag is a container used to contain "metadata" (data about data). Metadata is what is used to define the title of the document, character set, and other details that are relevant for accessibility and SEO. Metadata is not displayed on the web page for the user.

`<title>` - This is a metadata tag that will contain the title of the document. 
>Fun Fact: The title determines which words are displayed on the web page tab. 

`<body>` - The body tag is the container for all the elements that will make up a web page. Everything inside of the body tag will be displayed on the web page. This is where developers will store elements such as divs, spans, hyperlinks, text, etc.
</details>

### Comments in HTML
<details>
    <summary>Information</summary>

Comments can be written in HTML code to help clarify what's going on in the development environment. Comments will not appear in the browser, so they're not necessarily intended to be viewed by the users of a site. Comments are instead an excellent way to communicate with other developers, and even ourselves, about what's supposed to be going on in the code.

Comments begin with `<!--` and close with `-->`.

```html
<body>
    <!-- This is a comment that will not be displayed on the web page -->
</body>
```
</details>

### Meta Tags

Meta tags are used to provide information about a site that can be used by search engines and other software. Web crawlers and search engines use the metadata contained within meta tags to evaluate, rank, and sort through websites. Good usage of metatags can help optimize a site's ranking in search results. 

>Note: Meta tags need to be placed inside the `<head>` tag of the file.

<details>
    <summary>Example Meta Tags</summary>

```html
<head>
    <meta charset="UTF-8">
    <!-- charset stands for character set, and this information is used so the web browser knows which characters, or alphabets, are being used. UTF-8 (Unicode) covers almost all of the characters and symbols used in the world. -->
    <meta name="description" content="best website ever made">
    <!-- the description tag has a content attribute that dictates the primary description of your site as it appears in search engines -->
    <meta name="keywords" content="greatest, best, ultimate, GOAT, website, of all time">
    <!-- keywords are used to help search engines recognize what search words can be used to point users toward a site-->
    <meta name="author" content="matias perez-ferrero">
    <!-- the author tag serves to credit the creator of a website -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- a browser viewport is the area of web page in which the content is visible to the user. The width attribute can be used to set a specific width in pixels of the intended display. Here it is set to a special value (“width= device-width”) which is the width of the device in terms of CSS pixels at a scale of 100%. The initial-scale property governs the zoom level when the page is loaded for the first time. -->
</head>
```
</details>

### Semantic HTML

Semantic elements are elements that also communicate some meaning, as opposed to being used simply for display. Semantic HTML is crucial for accessibility issues and Search Engine Optimization (SEO). 

<details>
    <summary>Semantic HTML Information</summary>

Examples of nonsemantic HTML: `<div>, <span>`

Examples of semantic HYTML: `<footer>, <header>, <nav>, <form>, <table>, <article>, <main>, <section>`

Notice how the tag names imply some significant meaning about their contents. Appropriate usage of semantic HTML can boost a site's SEO, and also enable screen reading softwares to work more effectively for people with disabilities. 

When it comes to making your sites more accessible, here are three easy tips to follow: 
1. Always use the semantic tag alternative if it's an option
1. Attach labels to each of your `<input />` elements
1. Use a `<button>` tag whenever you use an `onClick` event handler. For more reasons on why you should try to always use buttons with onClicks, see here: https://blog.benmyers.dev/clickable-divs/

>Note: As of Oct. 2019, the Supreme Court has cleared the way for discrimination law suits against websites that are not accessible to people with disabilities. The Supreme Court let stand a ruling that the Americans With Disabilities act requires web pages to be equally accessible as any other utility to those with disabilities. This means that creating accessible websites will be legally mandatory in the near future. In light of this, be aware that chrome has developer tools that can help audit accessibility issues, and you can also add this extension that provides more advanced features for discovering accessibility issues: https://chrome.google.com/webstore/detail/axe-web-accessibility-tes/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US 

</details>

### Common Tags In HTML

There are many different tags that can be used to create HTML elements. Here, we will review the more commonly used HTML tags. 

<details>
    <summary>Heading Tags</summary>

Heading tags are used to create headers for content on a webpage. Heading tags can come with built-in font size and weight variations corresponding to their level, depending on the browser. These can be removed with a reset CSS file, or customized by developers using their own stylesheets. 

There are 6 levels of heading tags that are available for use. The lower the number of the heading is, the more important it is.

```html
<h1>Heading One</h1>
<h2>Heading Two</h2>
<h3>Heading Three</h3>
<h4>Heading Four</h4>
<h5>Heading Five</h5>
<h6>Heading Six</h6>
```
</details>

<details>
    <summary>Nav Tags</summary>
    
The `<nav>` tag defines a set of navigation links. Screen readers for disabled users can use the nav element to determine whether to omit the initial rendering of the content, which increases performance of the site and software.
>Note: Not all links of a document should be inside a `<nav>` element. The `<nav>` element is intended only for major blocks of navigation links.
</details>

<details>
    <summary>Paragraph Tags</summary>

The `<p>` tag can be used to declare that an element will be a paragraph.

```html
<p>Hey, I'm a paragraph!</p>
```
</details>

<details>
    <summary>Div and Section Tags</summary>

The `<div>` tag represents a division or a section within a web page. It is not semantic, as it doesn't imply anything about the contents of the tag. Div tags are often used as a container, or wrapper, for other elements in order to arrange the inner elements or apply some javascript functionality. 

```html
<div>
    <p>I'm using a div tag to create a division within my web page that "houses," "wraps," or "contains" a paragraph tag</p>
</div>
```

A semantic alternative to the `<div>` tag is the `<section>` tag. It can be used the same way that one would use a `<div>` tag, but it implies that the content is a meaningful section of the web page. 

```html
<section>
    <p>I'm using a section tag to create a semantic division within my web page that contains a paragraph tag</p>
</section>
```
</details>

<details>
    <summary>Span Tags</summary>

The `<span>` tag is used to group inline elements in the document. The span tag does not provide any visual changes on its own.

Span tags can be used, in conjuction with ids or classes, as a "hook" inside of another element to apply more specific styling or functionality to that content. 

```html
<span>
    <p>I'm a <span id="different-styled-font">span</span> tag inside of a p tag inside of a span tag!</p>
</span>
```
</details>

### Inline, Block, and Inline-Block Elements

Every HTML element has a default display property value assigned depending on the tag used. The two default display values are: `inline` and `block`. You can also assign an `inline-block` value to the display property. 

Here's a visual representation of differences between the properties: 

![inline-inline-block-block](images/inline-inline-block-block.png)

Now let's explore some more of the features of each. 

#### Block Level
<details>
    <summary>Block Level Information</summary>

Block level elements have some whitespace above and below the element. Block level elements also do the following: 

1. Do not allow elements to sit to their left or right
1. Force a line break after the block element
1. Acquire full width if width is not defined (i.e. width is 100% by default)
1. Can be assigned a height and width
1. Respect top, right, bottom, and left paddings and margins

Here are some common elements that are assigned `display: block` by default:

* `<ul>`
* `<form>`
* `<main>`
* `<footer>`
* `<nav>`
* `<div>`
</details>

#### Inline Level
<details>
    <summary>Inline Level Information</summary>

Inline level elements *DO NOT* start on a new line and will only take up as much width as needed. They have no line breaks before or after the element. They also do the following: 

1. Allow other inline or inline-block elements to sit to their left and right
1. Cannot be assigned a width and height
1. Respect left and right margins and padding, but *not* vertical margins and padding

>Note: Inline elements can be given vertical padding and borders of their own, but they will not push away other elements. This concept is easily confused, so check out this article for more details on inline-level elements: https://hacks.mozilla.org/2015/03/understanding-inline-box-model/

Here are some common elements that are assigned `display:inline` by default:

* `<button>`
* `<a>`
* `<label>`
* `<br>`
* `<span>`
</details>

#### Inline-block Level
<details>
    <summary>Inline-block Information</summary>

Inline-block elements are placed as inline elements (on the same line as adjacent content), but they otherwise behave like block level elements. Inline-block level elements also do the following: 

1. Allow other elements to sit to their left and right
1. Respect top and bottom margins and padding
1. Respect height and width

HTML elements are not given `display: inline-block` by default. Inline-block can only be manually defined. 
</details>

### Tag Attributes

Attributes are used in HTML to provide extra information or features to a tag. All tags can have attributes, and attributes should always be placed in the opening tag. 

Basic Syntax for an attribute:

```html
<tagname attributeName="attributeValue">content</tagname>
```

The attribute above has both a name and a value. The value is *assigned* to the name, and is wrapped in quotes. Notice also that the attribute is declared and assigned in the opening tag. 

Common attributes:

* `href` - the href attribute is commonly paired with an `<a>` tag, and it is used to specify a URL path to link to
* `src` - image tags can use the src attribute to specify the source path or file name of the image displayed
* `height` - the height attribute is used to assign a height to an element. It can take values of `px`, `%`, `vh`, `em`, or `rem`
>Note: Using `box-sizing: border-box` will affect how height is rendered. 
* `width` - the width attribute it similarly used to assign a width to an element. It can take values of `px`, `%`, `vh`, `em`, or `rem`

### Separation Tags

There are a couple of tags that can be used to create space or separation between elements. These tags are `<hr>` and `<br>`.

* `<hr>` - this tag is used to create white space between elements
* `<br>` - this tag is used to insert a single line break between elements

### Lists

There are two kinds of lists that can be created in HTML. They are known as ordered, or unordered lists. Each type of list is comprised of list items.

`<ul>` - this is the tag used to create an unordered list
* This will create a list-like structure using bullet poiints

`<ol>` - this is the tag used to create an ordered list
* This will create a list-like structure using numbers

`<li>` - this is the tag used to indicate that the content is a part of the list. It is short for "list item."

Syntax:

```html
<!-- Unordered List -->
<ul>
    <li>About</li>
    <li>Contact</li>
</ul>

<!-- Ordered List -->
<ol>
    <li>About</li>
    <li>Contact</li>
</ol>
```

### Inputs

Input boxes are commonly used to capture user input. `<input />` tags are used create input elements in HTML.

Input tags will need a `type` attribute applied in order to know what kind of input will be inserted. If there is not one applied, it will default to `type="text"` which is just a normal input box a user can type in. Below are some of the different types of inputs

>Note: `<input />` tags are an example of one of the more commonly used "self-closing" or "void" elements in HTML. They should *NOT* be written in pairs.

<details>
    <summary>Different Types of Inputs</summary>

* `<input type="button" />` 
* `<input type="checkbox" />`
* `<input type="color" />`
* `<input type="date" />`
* `<input type="datetime-local" />`
* `<input type="email" />`
* `<input type="file" />`
* `<input type="hidden" />`
* `<input type="image" />`
* `<input type="month" />`
* `<input type="number" />`
* `<input type="password" />`
* `<input type="radio" />`
* `<input type="range" />`
* `<input type="reset" />`
* `<input type="search" />`
* `<input type="submit" />`
* `<input type="tel" />`
* `<input type="text" />`
* `<input type="time" />`
* `<input type="url" />`
</details>

### Buttons

Buttons are a great way to enable users to interact with a web page.

`<button>` - this is the tag used to create a button.

In order to make buttons interactive, an event handling attribute, like `onClick` would need to be added. Events will be covered in the near future, so don't worry about them for now. Here's an example of what a button might look like:

```html
<button onClick="someFunction()">Cool Button!</button>
```

### Images

Images can be embedded into a web page via the `<img>` tag.

The `src` attribute is necessary to specify the source of the image shown. It can be a relative, local path, or a URL to some external source.

Image elements can also use an `alt` attribute to specify text that will display if the image source can't be loaded. Including descriptive `alt` tags is another way to enable a better experience for users with disabilities, as screen readers can read out the alt tag for visually impaired users. 

```html
<img src="https://images.unsplash.com/photo-1560807707-8cc77767d783?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=675&q=80" alt="long coated white and brown puppy lying on a bed" height="500" width="500"/>
```

### Form

A `<form>` tag can be used to create a form in our HTML. This form can be used to collect user data.

An HTML form contains `form elements`. Form elements are different types of input fields like text area, radio buttons, check boxes, etc.

```html
<form>
  First name:<br>
  <input type="text" name="firstname"><br>
  Last name:<br>
  <input type="text" name="lastname">
  <input type="submit" value="Submit">
</form>
```

`<input type="text">` - this defines a one line input field for user input

`<input type="submit">` - this defines a form button that will submit the data typed into the form

### Tables

We can create tables to organize content in HTML by using a `<table>` tag.
* Every table row is created using the `<tr>` tag.
* A table header column is created using the `<th>` tag
* a table cell is defined using the `<td>` tag

```html
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th> 
  </tr>
  <tr>
    <td>Tayte</td>
    <td>Stokes</td> 
  </tr>
  <tr>
    <td>Matt</td>
    <td>Bodily</td> 
  </tr>
  <tr>
    <td>Catie</td>
    <td>Mondon</td> 
  </tr>
</table>
```

## CSS

CSS stands for cascading style sheets. CSS is another one of the core languages of the web, but CSS is used mainly for creating style and layout of our HTML structure.

CSS is not a programming language, it is a styling language. We can add CSS to our HTML files.

### Methods To Do CSS

There are three main ways that we can do CSS:

1. Inline CSS

This is where we use the `style=""` attribute on the opening tag of a HTML element.
We should always try to avoid adding css this way.

2. Internal CSS

This is where we can write our CSS in the same HTML file, but we encapsulate it inside of a `<style>` tag.

3. External CSS

This is where we create a seperate style sheet to house our styling.

To follow this pattern (which is the most common way to write css) we will need to make a style sheet that ends with the extension `.css`.
Then we will need to link our style sheet to our HTML file. Inside of the `<head>` tag, we can use a `<link>` tag to link them together.

```html
<head>
    <link rel="stylesheet" type="text/css" href="stylesheet.css">
</head>
```

Above there are three attributes associated with the `<link>` tag to link the style sheet:
1. `rel` - this is the attribute where we tell the HTML file what the relation is
2. `type` - this is where we declare the type of file
3. `href` - this is where we declare the path to the style sheet we want to use

### Selectors

Selectors are used in CSS to determine what element we want to apply a specific styling to. Selectors are followed by a set of curly braces that is known as the `declaration`. Inside the declaration, we will use key/value pairs to select a property on the select element and apply value to that property.

```css
div {
    background-color: tomato;
}
```

There are a few ways to select an element to apply styling to:

1. We select the tag, if we do this it will apply this style to all the tags that we have selected

```css
div {
    background-color: tomato;
}
```

2. We can select an html class.

On the html tag, we can give it an attribute of `class=""` to give it a class name. We can use classes to apply styles to multiple elements using that classname.

HTML:
```html
<div class="container">

</div>
```

CSS:
```css
.container {
    background-color: tomato;
}
```

We need to prefix our selector with a `.` to declare we are looking for a class.

3. We can select an html id

This is the same as the selecting a class, but we should never have more than one element with the same id.

HTML:
```html
<h1 id="title">This is my title</h1>
```

CSS:
```css
#title {
    color: tomato;
}
```

Notice how we prefix our selector with a `#` to declare we are selecting an id.

### CSS Selector Patterns

We can target multple elements at once, or be very specific about what element to select to apply a set of styles to.

Using these different selector patterns will help keep our code `DRY`.

We can use a `,` to select multiple elements at once to apply the same styling.

```css
h1, div, span {
    color: blue;
    background-color: tomato;
}
```

We can use a white space ` ` or the carot `>` to go select a specific element that is nested inside of other elements.

```css
nav div h1 {
    color: blue
}

nav > div > h1 {
    color: red;
}
```

### CSS Specificty

CSS specificity refers to a set of rules that browsers use to determine which styles are applied when there is a conflict. 

This set of rules work on a point system. Each selector has a different point value given to it. The higher the point value, the more likely that style is to be applied to the element. We use this set of rules to determine how to override or avoid overriding styles that conflict.

Point System:

`Inline Styling` - this is where we apply styles directly to the HTML tag. Inline styling is worth 1000 points.

```html
<h1 style="color: blue">This is my title</h1>
```

`ID` - when we use an id to apply styles, it will gain 100 points in this system

```css
#title {
    color: blue
}
```

`Class` - when a class is selected to apply an element, it gains 10 points

```css
.containers {
    background-color: tomato;
}
```

`element` - when we target an element directly using this tag, it is applied only 1 point

```css
div {
    background-color: tomato;
}
```

### DRY Code => DRY CSS

`DRY` stands for 'don't repeat yourself'. This is a coding philosophy developers should aspire to follow to help avoid writing the same code over and over again. 

When it comes to CSS, here's tips to apply in order to stay DRY:


### Reset CSS

By default, the browser will apply its own set of styling rules to the elements inside of an HTML file.

We can use a `reset css` file to remove all default styling from a browser.

Check this website out to get a prebuilt reset css file: ![reset css](https://meyerweb.com/eric/tools/css/reset/)

### Display Property

The `display` property is a property that can help aid us in setting up the lay out for each element.

`display` has multiple values that we can give it:

`block` - this display value will cause each element to appear own a new line and will take up the full amount of width that it can

`inline` - this value will cause each element to not go to a new line and will only take up as much width as it needs. You can not edit the height or width of an inline element.

`inline-block` - works just like inline, but allows us to edit the height and width of the element

### Floats

The `float` property places an element on the left or right side of it's container, allowing text and inline elements to wrap around it.

```css
div {
    float: left;
}

img {
    float: right;
}
```

`clear` is the property we can use if we want to declare that nothing can sit on the side of the floated element

```css
div {
    float: right;
}

h1 {
    clear: right;
    /* this will make the h1 sit underneath the div because we are clearing everything to the left side of the div positioned right */
}
```

### Text Properties

There are multiple properties we can use to manipulate the way text looks on our web page.

Using good fonts and text colors are important for good design.

There are many different properties we can modify:

`font-size` - this will change the size of the font

`color` - this will change the color of the text inside of an element

`line-height` - will determine the total amount of space the content height will take up

`text-align` - property that defines where to align the text according to the size of the element

`font-family` - will determine what font family we want our text to be in

`letter-spacing` - will determine how much white space should be between each character

### Background Properties

These are properties that we can use to modify the background of an element.

There are many different background properties we can modify:

`background-image` - we can use an image as a background for an element. The content inside of the element will appear above the image.

```css
div {
    background-image: url('image.png')
}
```

`background-size` - this determines the size of the background

`background-position` - we can use this to adjust where and how the background image will align

`background-repeat` - we can use this to choose how and if the background image should be repeated

`background-color` - we can use this to change the background color of an element

### Box Model

The box model is a tool we can use when it comes to styling the layout of our elements. The box model is more of a concept or pattern to follow rather than actual code values.

Following the box model means that we are looking to style four specific parts of our elements in order to get the right layout and design of the element.

Those four properties are:

1. Margin
Margin is the white space between each element

2. Border
Border is the border of the box

3. Padding
Padding is the white space between the content of an element and its border

4. Content
The content of an element is anything inside of an element such as text, images, etc.

# Additional Resources

# HTML/CSS I Mini Project



# HTML/CSS I Afternoon Project


