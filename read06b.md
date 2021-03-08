# INTRODUCING CSS

**CSS** is responsible for making your web page more attractive by creating rules that specify how the content should be appear.

The key to understanding how CSS works is to imagine that there is an invisible box around every HTML element.

CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a **selector** and a **declaration**.

![](Images/read06b-1.jpg)

CSS declarations sit inside curly brackets and each is made up of two parts: a **property** and a **value**, separated by a colon. You can specify several properties in one declaration, each separated by a semi-colon.

![](Images/read06-2.jpg)

## USING EXTERNAL CSS LINK

### LINK

The link element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning it does not need a closing tag), and it lives inside the head element. It should use three attributes:
#### href

This specifies the path to the CSS file (which is often placed in a folder called css or styles).

#### type

This attribute specifies the type of document being linked to. The value should be text/css.

#### rel

This specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file.

    <link href="css/styles.css" type="text/css"
rel="stylesheet" />    

## USING INTERNAL CSS

### style 

You can also include CSS rules within an HTML page by placing them inside a style element, which usually sits inside the head element of the page. The style element should use the type attribute to indicate that the styles are specified in CSS. The value should be text/ css.

    <style type="text/css">
body {
font-family: arial;
background-color: rgb(185,179,175);}
h1 {
color: rgb(255,255,255);}    

## CSS SELECTORS

There are many different types of CSS selector that allow you to target rules to specific elements in an HTML document. The following table shows the most common selectors:

![](Images/read06b-3)

# COLOR

## Foreground Color

The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:

### RGB VALUES

These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)

### HEX CODES

These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80

### COLOR NAME

There are 147 predefined color names that are recognized by browsers. For example: DarkCyan

## BACKGROUND COLOR

CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.

You can specify your choice of background color in the same three ways you can specify foreground colors: RGB values, hex codes, and color names

## OPACITY

CSS introduces the opacity property which allows you to specify the opacity of an element and any of its child elements. The value is a number between 0.0 and 1.0 (so a value of 0.5 is 50% opacity and 0.15 is 15% opacity). You can do this by using rgba:

    background-color: rgba(0,0,0,0.5);}    

## HSL COLORS

CSS introduces an entirely new and intuitive way to specify colors using hue, saturation, and lightness values.

### HUE 

Hue is the colloquial idea of color. In HSL colors, hue is often represented as a color circle where the angle represents the color, although it may also be shown as a slider with values from 0 to 360.

### SATURATION

Saturation is the amount of gray in a color. Saturation is represented as a percentage. 100% is full saturation and 0% is a shade of gray.

### LIGHTNESS

Lightness is the amount of white (lightness) or black (darkness) in a color. Lightness is represented as a percentage. 0% lightness is black, 100% lightness is white, and 50% lightness is normal.