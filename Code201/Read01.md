# Class-01

## How Websites Are Created

All websites use HTML and CSS, but content management systems, blogging software, and e-commerce platforms often add a few more technologies into the mix.

## STRUCTURE

The use of headings and subheadings in any document often reflects a hierarchy of information. For example, a document might start with a large heading, followed by an introduction or the most important information.

This might be expanded upon under subheadings lower down on the page. When using a word processor to create a document, we separate out the text to give it structure. Each topic might have a new paragraph, and each section can have a heading to describe what it covers.

## HTML Describes the Structure of Pages

to describe the structure of the web page, a code is added to the words we want to appear on the web page. the code bellow is an example how we put the words between codes:

```<html>
<body>
<h1>This is the Main Heading</h1>
<p>This text might be an introduction to the rest of
the page. And if the page is a long one it might
be split up into several sub-headings.<p>
<h2>This is a Sub-Heading</h2>
<p>Many long articles have sub-headings so to help
you follow the structure of what is being written.
There may even be sub-sub-headings (or lower-level
headings).</p>
<h2>Another Sub-Heading</h2>
<p>Here you can see another sub-heading.</p>
</body>
</html>
```

## EXTRA MARKUP

### The Evolution of HTML

Since the web was first created, there have been several different versions of HTML. and becuase of that each web page should begin with  a DOCTYPE declaration to tell a browser which version of HTML the page is using:

``` <!DOCTYPE html>
```

### COMMENTS IN HTML

If you want to add a comment to your code that will not be visible in the user's browser, you can add the text between these characters:

``` <!-- comment goes here -->
```

### Information About Your Pages

The `<meta>` element lives inside the `<head>` element and contains information about that web page.

The `<meta>` element is an empty element so it does not have a closing tag. It uses attributes to carry the information.

## HTML5 Layout

HTML5 introduces a new set of elements that allow you to divide up the parts of a page with out using the `<div>` element. The names of these elements indicate the kind of content you will find in them. They are still subject to change, but that has not stopped many web page authors using them already. For example the header now can be sitted inside the `<header>` element and the navigation bar inside the `<nav>` element. The point of creating these new elements is so that web page authors can use them to help describe the structure of the page.

### Headers & Footers

The `<header>` and `<footer>` elements can be used for:

* The main header or footer that appears at the top or bottom of every page on the site.

* A header or footer for an individual article or section within the page.

### Navigation

The `<nav>` element is used to contain the major navigational blocks on the site such as the primary site navigation.

### Articles

The `<article>` element acts as a container for any section of a page that could stand alone and potentially be syndicated.

### Sections

The `<section>` element groups related content together, and typically each section would have its own heading.

### Linking Around Block-Level Elements

HTML5 allows web page authors to place an <a> element around a block level element that contains child elements. This allows you to turn an entire block into a link. for example:

![](images/Read01-1.JPG)

## PROCESS AND DESIGN

There are several questions you should ask yourself when you're going to design a web page:

* **Who is the Site For?**

Every website should be designed for the target audience—not just for yourself or the site owner. It is therefore very important to understand who your target audience is.

* **Why People Visit YOUR Website**

Now that you know who your visitors are, you need to consider why they are coming. While some people will simply chance across your website, most will visit for a specific reason.

* **What Your Visitors are Trying to Achieve**

It is unlikely that you will be able to list every reason why someone visits your site but you are looking for key tasks and motivations. This information can help guide your site designs.

* **What Information Your Visitors Need**

You know who is coming to your site and why they are coming, so now you need to work out what information they need in order to achieve their goals quickly and effectively.

* **How Often People Will Visit Your Site**

Some sites benefit from being updated more frequently than others. Some information (such as news) may be constantly changing, while other content remains relatively static.

### WireFrames

A wireframe is a simple sketch of the key information that needs to go on each page of a site. It shows the hierarchy of the information and how much space it might require. For example:

![](images/Read01-2.JPG)

## THE ABC OF PROGRAMMING

### A : What is script and how do I create one?

A script is a series of instructions that a computer can follow to achieve a goal. To write a script, you need to first state your goal and then list the tasks that need to be completed in order to achieve it.

### B : How computers fit in with the world around them

 Computers create models of the world using data, where programmers who are responsible for build these models so the computer can understand it.

 Computers use data to create models of things in the real world. The events, methods, and properties of an object all relate to each other: Events can trigger methods, and methods can retrieve or update an object's properties.

### C : How do you write a script for a web page

Web developers usually talk about three languages that are used to create web pages: HTML, CSS, and JavaScript. Where possible, aim to keep the three languages in separate files, with the HTML page linking to CSS and JavaScript files.

Each language forms a separate layer with a different purpose. Each layer, from left to right. builds on the previous one.

HTML resposible for the content layer, CSS for the presentation layer and the javascript for the behavior layer.

