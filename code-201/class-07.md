# **(Domain Modeling) Notes:**

+ Here's some tips to follow when building your own domain models using object-oriented programming (OOP):
  + When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
  + Model its attributes with a constructor function that defines and initializes properties.
  + Model its behaviors with small methods that focus on doing one job well.
  + Create instances using the new keyword followed by a call to a constructor function.
  + Store the newly created object in a variable so you can access its properties and methods from outside.
  + Use the this variable within methods so you can access the object's properties and methods from inside.

---
# **HTML (Ch6 tables) Notes:**

+ The contents of the table are written out row by row. Example of HTML table:

```html
<table> <!--this tage used to create table-->
  <tr> <!--table row-->
    <th scope='col'>name</th> <!--table heading-->
    <th scope='col'>age</th>
    <th scope='col'>mark</th>
  </tr>
  <tr>
    <td>Ahmad</td> <!--table data-->
    <td>20</td>
    <td>75%</td>
  </tr>
  <tr>
    <td>Osama</td>
    <td>18</td>
    <td>90%</td>
  </tr>
</table>
```
![table](img/table.jpg)

+ HTML table attribute:
  + `scope='col'` used with `<th>` to indicate the the header in column
  + `scope='row'` used with `<th>` to indicate the the header in row
  + `colspan="here num of columns"` used with `<th>` and `<td>` indicates how many columns that cell should run across.
  + `rowspan="here num of rows "` used with `<th>` and `<td>` indicates how many rows that cell should run across.

+ `<thead>` and `<tbody>` and `<tfoot>` used for *long tables* to distinguish between different parts of the table, it helps to easy reading and easy styling the table.

---
# **Javascript (Ch3 Functions, Methods, and Objects) Notes:**



[Back to home page](../README.md)