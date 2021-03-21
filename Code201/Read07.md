# Object-Oriented Programming, HTML Tables

## Tables

A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results.

Each block in the grid is referred to as a table cell. In HTML a table is written out row by row.

The `<table>` element is used to create a table. The contents of the table are written out row by row.

You indicate the start of each row using the opening `<tr>` tag. (The tr stands for table row.)

It is followed by one or more `<td>` elements (one for each cell in that row).

At the end of the row you use a
closing `</tr>` tag.

Each cell of a table is represented using a `<td>` element. (The td stands for table data.)

At the end of each cell you use a closing `</td>` tag.

``` 
<table>
<tr>
<td>15</td>
<td>15</td>
<td>30</td>
</tr>
<tr>
<td>45</td>
<td>60</td>
<td>45</td>
</tr>
<tr>
<td>60</td>
<td>90</td>
<td>90</td>
</tr>
</table> 
```

The `<th>` element is used just like the `<td>` element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.)

Even if a cell has no content, you should still use a `<td>` or `<th>` element to represent the presence of an empty cell otherwise the table will not render correctly.

## Functions, Methods, and Objects

### Creating an object using constructor notation 

The new keyword and the object constructor create a blank object.

You create a new object using a combination of the new keyword and the object() constructor function.

### THIS

The keyword this is commonly used inside functions and objects. Where the function is declared alters what this means. It always refers to one object, usually the object in which the function operates.