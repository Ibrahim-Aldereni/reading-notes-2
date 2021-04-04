# **HTML & CSS (Ch2-Ch10) Notes:**

## Notes:
+ Semantic Markup don't affect the structure of the web page but add extra information so you know the type of element you insert.
![semantic](img/semantic.png)

+ White spaces or multiple spaces treated as a single space in HTML.
![spaces](img/whitespace.jpg)

+ CSS rule contains two parts: selector and declaration, a declaration split into property and value. see the figure below:
![css](img/CSSrule.png)

+ There are many different types of CSS selector that allow you to target rules to specific elements in an HTML document, in the figure below some of them:
![selectors](img/selectors.jpg)

## Example:

> in this example we see a different types of CSS selectors.

```html
<!DOCTYPE html>
<html>
  <head>
  <title>CSS Style</title>
  <style>
    *{  >>>> this is Universal Selector
      color: red;
    }

    h1{ >>>> this is Type Selector
      background: blue;
    }

    .div1{ >>>> this is Class Selector
      font-size: 15px;
    }

    div>p{  >>>> this is Child Selector
      color: green;
    }
  </style>
  </head>
  <body>
    <h1>this is heading</h1>
    <div class="div1"> this is div
      <p>this is paragraph<p>
    </div>
  </body>
</html>  
```

## Definitions list:
+ White space Collapsing >> treat the multiple spaces as single space.
+ Semantic markup >> provides extra information.
+ Structural markup >> the elements that you can use to describe both headings and paragraphs.
+ Block elements >> they start on a new line.
+ Inline elements >> they flow within the text and do not start on a new line.
+ Inheritance >> when apply some property to the parent element the child will be affected.

## Cheat sheet:

+ `<b>` Defines bold text
+ `<i>` Defines italic text
+ `<sup>` Defines a super-scripted text
+ `<sub>` Defines a sub-scripted text
+ `<br>` Inserts a single line break
+ `<hr>` Defines a horizontal rule
+ `<strong>` Defines strong text
+ `<em>` Defines emphasized text
+ `<link>` Defines a resource reference
+ `<style>` Defines a style definition

---
# **Javascript (Ch2-Ch4) Notes:**

## Notes:
here insert some images

## Example:


## Definitions list:



## Cheat sheet:


  

[Back to home page](../README.md)