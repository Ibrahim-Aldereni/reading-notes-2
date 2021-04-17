# **HTML & CSS (Ch16 - Ch19) Notes:**

## Ch16 - Images Notes:

+ You can control the size of the image using `width` and `height` properties in CSS.

+ To center the image:
  1. Change the image display to `block`.
  2. Choose one of these 2 ways:
     + On the containing element, you can use the `text-align` property with a value of `center`.
     +  On the image itself, you can use the use the `margin` property and set the values of the `left and right margins to auto`.

+ The `background-image` property allows you to place an image *behind any HTML element.*
+ `background-repeat` property help control repetition of the background image and it have 4 values: repeat,repeat-x,repeat-y and no-repeat. 
+ `background-attachment` property control whether a background image should stay in one position or move as the user scrolls and it have 2 values: fixed nad scroll.
+ `background-position` property to specify where in the browser window the background image should be placed and it have 2 pair values *The first represents the horizontal position and the second represents the vertical*.

  ```css
  /* these two setting have the same result*/
  body {
    background-position: center center;
    background-position: 50% 50%;
    }
  ```

+ When a single image is used for several different parts of an interface, it is known as a **sprite**, and this donr by change the background position whne hover or when click. The advantage of using sprites is that the web browser only needs to request one image rather than many images, which can make the web page load faster.



## Ch19 - Practical Information Notes:



[Back to home page](../README.md)