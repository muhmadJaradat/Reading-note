# HTML & CSS structure
In all kinds of documents, structure is very important in helping
readers to understand the messages and the same applies to the website structure.
So HTML uses tags (characters that sit inside angled
brackets) to give the information they surround special
meaning. like h1 tag used write the text in a large heading: 

```<h1>This is the Body of the Page</h1>```

Tags usually come in pairs. The opening tag denotes
the start of a piece of content; the closing tag denotes
the end.

To learn HTML you need to know what tags are
available for you to use, what they do, and where they
can go.
# Extra Markup
HTML has several versions to keep up with the evolution of the technologies, because of that every web page should have something called DOCTYPE to indicate the HTML version that the web page used:

```<!DOCTYPE html>```

For adding comments in your code which will be not visible to the user you can use these characters:

```<!-- comment goes here -->```

# Class attribute
this will save you time if you want to modifiy several different elemants in the same way so you can identifiy these elements in a class. the example bellow shows how this can be done:

```<p class="important">```

now this paragraphg is identifiyed in 'important class'
# Block elements
Some elements will always appear to start on a new line in the browser window. These are known as block level elements.

Examples of block elements are: 


``<h1>, <p>, <ul>, and <li>``
# Inline elements
Some elements will always appear to continue on the same line as their neighbouring elements. These are known as inline elements.

Examples of inline elements are

``<a>, <b>, <em>, and <img>.``
# Grouping text & elements in a block
### div
this elements allows you to group a set of elements together in one block block-level box.

Using an id or class attributeon the <div> element, however, means that you can create CSS style rules to indicate how much space the <div> element should occupy on the screen and change the appearance of all the elements contained within it. the following example shows how you can do it:

``` <div id="header">
<img src="images/logo.gif" alt="Anish Kapoor" />
<ul>
 <li><a href="index.html">Home</a></li>
 <li><a href="biography.html">Biography</a></li>
 <li><a href="works.html">Works</a></li>
 <li><a href="contact.html">Contact</a></li>
</ul>
</div><!-- end of header --> ```  
```
### Span
The <span> element acts like an inline equivalent of the ``<div>`` element. It is used to either:
1.  Contain a section of text where there is no other suitable element to differentiate it from its surrounding text
2. contain a number on inline elements , example:

``` <p>Anish Kapoor won the Turner Prize in 1991 and
 exhibited at the <span class="gallery">Tate
 Modern</span> gallery in London in 2003.</p> ``` 
 ``` 
 usually you will see a class or id attribute is used with span elements:
 * to explain why you used it
 * and to impact the CSS styles to these elements
 # IFrames 
 An iframe is like a little window that has been cut into your page and in that window you can see another page. The term iframe is an abbreviation of inline frame.

 The main use of iframe is to embed a google map into a page. However, the Ifram content can be any html page anywhere on the web.

 An iframe is created using the iframe element. There are a few attributes that you will need to know to use it:
 * src : The src attribute specifies the URL of the page to show in the frame.
 * height: 
 The src attribute specifies the URL of the page to show in the frame.
 * width: The width attribute specifies the width of the iframe in pixels. the example bellow shows how you can do it:

 ``` <iframe
width="450"
height="350"
src="http://maps.google.co.uk/maps?q=moma+new+york
&amp;output=embed">
</iframe> ``` 
