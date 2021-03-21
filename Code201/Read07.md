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

### Domain Modeling

Domain modeling is the process of creating a conceptual model in code for a specific problem.

A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. 

An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.

Here's some tips to follow when building your own domain models.

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.

2. Model its attributes with a constructor function that defines and initializes properties.

3. Model its behaviors with small methods that focus on doing one job well.

4. Create instances using the new keyword followed by a call to a constructor function.

5. Store the newly created object in a variable so you can access its properties and methods from outside.

6. Use the this variable within methods so you can access the object's properties and methods from inside.

### Creating an object using constructor notation

The new keyword and the object constructor create a blank object.

You create a new object using a combination of the new keyword and the object() constructor function.

### THIS

The keyword this is commonly used inside functions and objects. Where the function is declared alters what this means. It always refers to one object, usually the object in which the function operates.