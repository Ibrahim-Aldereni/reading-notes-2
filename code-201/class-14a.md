# **Transforms Article Notes:**

+ To make sure that the browser support the transform property use **prefixs** before the property name.

  ![prefixes](img/prefixes.jpg)

  + example of the prefix use:

    ```css
      button{
        -webkit-transform: scale(1.2);
        -moz-transform: scale(1.2);
        -o-transform: scale(1.2);
      }
    ```

+ `rotate` value accept from 0-360deg, and if positive it will rotate clockwise and if negative counterclockwise. see example below:

  ```css
    .image1{
      transform: rotate(20deg);
    }
    .image2{
      transform: rotate(20deg);
    }
  ```

   ![Rotate](img/rotate.png)

+ `scale` value controls the size of the element, 1 is the default value, >1 will enlarge and <1 will shrink. see example below:

  ```css
    .image1{
      transform: scale(.6);
    }
    .image2{
      transform: scale(1.20);
    }
  ```

    ![scale](img/scale.png)

  > It is possible to scale only the height or width of an element using the **scaleX and scaleY** values.


+ `translate` value moves element in x&y axis, see example below:

  ```css
    .image1{
      transform: translateX(-10px);
    }
    .image2{
      transform: translateY(25%);
    }
    .image3{
      transform: translate(-10px, 25%);
    }
  ```

  ![translate](img/translate.png) 

+ `skew` value controls the distortion of an element, see example below:

  ```css
    .image1{
      transform: skewX(5deg);
    }
    .image2{
      transform: skewY(-20deg);
    }
    .image3{
      transform: skew(5deg, -20deg);
    }
  ```

  ![skew](img/skew.png)

+ You can use multiple tranform values at once, see example below:

  ```css
    .image1{
      transform: rotate(25deg) scale(.75);
    }
  ```

  ![multipleTransfom](img/multipleTransfom.png)


+ The default transform origin is the center of an element, both 50% horizontally and 50% vertically, you can change that see examples:
  + `transform-origin: 0 0` top left or `transform-origin: top left`
  + `transform-origin: 100% 100%` bottom right

---
# **Transitions & Animations Notes:**

+ `transition` you can change appearance and behavior of an element when hover or click on the element. There is 4 properties `transition-property`, `transition-duration`,`transition-timing-function`, and `transition-delay`.

  + example:
    ```css
      .box {
      background: #2db34a;
      transition-property: background;
      transition-duration: 1s;
      transition-timing-function: linear;
      }
      .box:hover {
        background: #ff7b29;
      }
    ```
    ![transition](img/transition.gif)

+ only the properties identified within the `transition-property` value will be affected by any transitions.

  + example:

    ```css
      .box {
        background: #2db34a;
        border-radius: 6px;
        transition-property: background, border-radius;
        transition-duration: 1s;
        transition-timing-function: linear;
      }
      .box:hover {
        background: #ff7b29;
        border-radius: 50%;
      }
    ```
    ![transition2](img/transition2.gif)


+ `transition-timing-function` property is used to set the speed in which a transition will move and it have these values: linear, ease-in, ease-out, and ease-in-out.

+ `transition-delay` property used to set how long a transition should be stopped before executing.
  + example:
    ```css
      .box {
        background: #2db34a;
        border-radius: 6px;
        transition-property: background, border-radius;
        transition-duration: .2s, 1s;
        transition-timing-function: linear, ease-in;
        transition-delay: 0s, 1s;
      }
      .box:hover {
        background: #ff7b29;
        border-radius: 50%;
      }
    ```
    ![transition3](img/transition3.gif)

+ When more control is required, transitions need to have multiple states. In return, this is where `animations` pick up where transitions leave off.

+ The `@keyframes` rule includes the `animation name`, `any animation breakpoints`, and the `properties` intended to be animated.

+ See more info about animation and keyframes her >> [Transitions & Animations](https://learn.shayhowe.com/advanced-html-css/transitions-animations/#shorthand-transitions)



[Back to home page](../README.md)