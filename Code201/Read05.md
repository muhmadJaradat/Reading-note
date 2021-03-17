# Images, Color, Text

## Images

There are several things to consider when selecting and preparing images for your site, but taking time to get them right will make it look more attractive and professional. In this chapter you will learn how to:

* Include an image i ●● n your web pages using HTML

* Pick which image format to use

* Show an image at the right size

* Optimize an image for use on the web to make pages load faster

A picture can say a thousand words, and great images help make the difference between an average-looking site and a really engaging one.

If you are building a site from scratch, it is good practice to create a folder for all of the images the site uses.

### Adding Images

To add an image into the page you need to use an `<img>` element. This is an empty element (which means there is no closing tag). It must carry the following two attributes:

* **src:** This tells the browser where it can find the image file. This will usually be a relative URL pointing to an image on your own site.

* **alt:** This provides a text description of the image which describes the image if you cannot see it

        <img src="images/quokka.jpg" alt="A family of
quokka" title="The quokka is an Australian
marsupial that is similar in size to the
domestic cat." /> 

## Color

### Foreground Color (color)

The color property allows you to specify the color of text inside an element.

    h1 {
color: DarkCyan;}

### Background Color

CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.

    body {
background-color: rgb(200,200,200);}

## TEXT

### Choosing a Typeface for your Website

When choosing a typeface, it is important to understand that a browser will usually only display it if it's installed on that user's computer.As a result, sites often use a small set of typefaces that are installed on most computers.

### Techniques That Offer a Wider Choice of Typefaces

There are several ways to use fonts other than those listed on the previous page. However, typefaces are subject to copyright, so the techniques you can choose from are limited by their respective licenses.

* **font-family:** The user's computer needs the typeface installed. CSS is used to specify the typeface.

* **font-face:** CSS specifies where a font can be downloaded from if it is not installed on the computer.

* **Service-based Font-Face:** Commercial services give users access to a wider range of fonts using @font-face.