# **HTML & CSS (Ch4-Ch15) Notes:**

## Notes:

+ You can create a link to other site by decalring `<a href=''>` anchor tag with an attribute of `href` that holds the site URL.

+ Relative URL have types, see the figure below to understand:

![url](img/relativeURL.jpg)

+ To have a link that open email address we use href attribute start with (mailto), and also to open it on other tab you can use (target) attribute, see the code below:

```html
<a href="mailto:jon@example.org" target="_blank">Email Jon</a>
```

+ CSS position Schemes are: normal flow(static), relative, absolute and fixed.
  + **Static position**: is the default position where each element starts a new line even if there is a room beside other element.
  + **Relative position**: move the element in relation to the static position, then you can add offset (right, left) to move it horizontally, or offset (top, bottom) to move it vertically.
  + **Absolute position**: will take the element out of the normal flow(static) and will not affect the other elements positions(like it is not there), and here also you can add offset to move it.
  + **Fixed position**: It positions the element in relation to the browser window. so, when a user scrolls down the page, it stays in the exact same place, and to control where the fixed position element appears in relation to the browser window, the element offset properties are used.

![css-positions](img/CssPosition.jpg)

## Example:

```css
h1{
  position: fixed;
  top: 0px;
}
```

> in the example above we make the (h1) element fixed on the screen, so when you scroll down the page the h1 will have a fixed place and you will stay see it.


## Definitions list:

+ **URL** >> Uniform Resource Locator.
+ **absolute URL** >>  the full web address for the site, and they have domain names.
+ **relative URL** >> the link to other page within the website, and they don't have domain names.
+ **Directories** >> folders on the website.
+ **root folder** >> folder contains all the website files and folders.
+ **index.html** >> default homepage of a site written in HTML.
+ **Parent Folder** >> the main folder that contain inside it other folders.
+ **Child Folder** >> the folder that it's inside other folder (parent).

## Cheat sheet:

### HTML:

+ `<a href='' taget='_blank>link</a>'` link that open in new tab.
+ `<a href="mailto:jon@example.org">Email </a>` link that opens and email.
+ `<a href='#top'>top</a>` link related to other tag in the same page.

### CSS:

+ `position` property determines the position of the element.

---
# **Javascript (Ch3-Article) Notes:**

## Notes:

+ Steps of writing the functions:
  1. Declaration.
  1. Returning value.
  1. Calling.

```javascript
function Size(w,h){ // declaring function with parameters (w,h)
  let area = w * h;  // code to be executed
  return area;   // value to be returned out of the function
}

Size(3,2);  // calling the function and provide the arguments
```
  
+ There is 2 types of functions: named and anonymous, see the code below to understand:

```javascript
// named function
function sum(a,b){
  let add = a+b;
  return add;
}
sum(1,2)

// anonymous function
let sum = function(a,b){
  let add = a+b;
  return add;
}
sum(1,2)
```

+ You can declare and call the function at the same time, and this is called Immediately Invoked Function Expression, see code below:

```javascript
// Immediately Invoked Function
(function sum(a,b){
  let add = a+b;
  return add;
}())
```

+ Pair Programming means that 2 developers working on the same workstation to code together.

+ Pair Programming have 2 roles: one is the driver and the other is the navigator. the driver is the only one that touc hthe keybord and writing code, navigator on the other hand give advices and fix bugs and typos and think about the big picture.

+ Benefits of Pair Programming:
  1. More efficiency.
  1. Engaging collaboration.
  1. Learning from each other.
  1. improve social and interpersonal skills.
  1. Get ready to job interviews.
  1. Get ready for work environment.


## Definitions list:

+ **Function** >> have series of statements as a group to perform a certin task.
+ **Methods** >>  same as the function but it's created inside and object.
+ **parameters** >> informations passed to the function to run.
+ **function calling** >> write the name of the function with parentheses and paremeters if required after declaring it.
+ **Named function** >> function that have a name and you can call it before declare it.
+ **Anonymous function** >> trated as expression and have no name and you can't call it before declare it.
+ **IIFE** >> Immediately Invoked Function Expression, means a function declared and called at the same time.
+ **Local variable** >> also called function level variable, which used inside a function (local scope).
+ **Global variable** >> any variable outside a function (global scope).

## Cheat sheet:

+ ```javascript
  // Immediately Invoked Function
  (function sum(a,b){
    let add = a+b;
    return add;
  }())
  ```
+  ```javascript
    // named function
    function sum(a,b){
      let add = a+b;
      return add;
    }
    sum(1,2)
    ```
+   ```javascript
    // anonymous function
    let sum = function(a,b){
      let add = a+b;
      return add;
    }
    sum(1,2)
    ``` 


[Back to home page](../README.md)