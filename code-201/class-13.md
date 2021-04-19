# **Notes:**

+ Historically, web applications don't have local storage. Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data.

+ Microsoft invented a great many thingsOne of these things was called DHTML Behaviors, and one of these behaviors was called *userData*. userData allows web pages to store up to 64 KB of data per domain.

+ In 2007, Google launched **Gears**. Gears can store unlimited amounts of data per domain in SQL database tables.

+ **HTML5 Storage** it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you.

+ In HTML5 Storage the data is actually stored as a **string**. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() to convert it.

+ Get and set local storage in HTML5:

  ```javascript
  // first way: 
    let foo = localStorage.getItem("bar"); // get
    localStorage.setItem("bar", foo); // set

  // second way:
    let foo = localStorage["bar"]; // get
    localStorage["bar"] = foo; // set
  ```

+ `removeItem()` method for removing the value for a given named key.

+ `key()` property to get the total number of values in the storage area and to iterate through all of the keys by index.

+ Example of setting and getting boolean and number:

  ```javascript
    // set boolean in (local storage object)
    localStorage["halma.game.in.progress"] = gGameInProgress;

    // get boolean and convert it to boolean (cuz it saved as string)
    gGameInProgress = (localStorage["halma.game.in.progress"] == "true");

    // set number:
    localStorage["halma.movecount"] = gMoveCount;

    // get number and convert it:
    gMoveCount = parseInt(localStorage["halma.movecount"]);
  ```

[Back to home page](../README.md)