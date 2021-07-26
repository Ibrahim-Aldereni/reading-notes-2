# **Lists and Keys:**

- **What does .map() return?**

  map method will return an array

- **If I want to loop through an array and display each value in JSX, how do I do that in React?**

  see the example below (1):

  ```JSX
    const numbers = [1, 2, 3, 4, 5];
    const listItems = numbers.map((number) =>
      <li>{number}</li>
    );

    ReactDOM.render(
    <ul>{listItems}</ul>,
    document.getElementById('root')
    );
  ```

- **Each list item needs a unique 'key'**

- **What is the purpose of a key?**

  Key make react recognize if the item changed or removed.

# **How to Use the Spread Operator in JavaScript:**

- **What is the spread operator?**

  JavaScript spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.(2)

- **List 4 things that the spread operator can do.**

  - Copying an array
  - Concatenating or combining arrays
  - Using Math functions
  - Using an array as arguments (2)

- **Give an example of using the spread operator to combine two arrays.**

  ```javascript
  let arr1 = [1, 2];
  let arr2 = [3, 4];

  let arr3 = [...arr1, ...arr2];

  console.log(arr3); // result: [1,2,3,4]
  ```

- **Give an example of using the spread operator to add a new item to an array.**

  ```javascript
  let arr1 = [1, 2];
  let arr2 = [...arr1, 3, 4];

  console.log(arr2); // result: [1,2,3,4]
  ```

- **Give an example of using the spread operator to combine two objects into one.**

  ```javascript
  let ob1 = { name: "ahmad" };
  let ob2 = { age: 20 };
  let ob3 = { ...ob1, ...ob2 };

  console.log(ob3); // result: {name: "ahmad", age: 20}
  ```

# **How to Pass Functions between Components:**

- **In the video, what is the first step that the developer does to pass functions between components?**

  Add prop to the parent component with the function that need to passed top the child

- **In your own words, what does the increment function do?**

  Update the state count according to the name

- **How can you pass a method from a parent component into a child component?**

  Using a prop in parent with a function then call it in the child

- **How does the child component invoke a method that was passed to it from a parent component?**
  By accesing the prop that have a function value that passed from the parent

---

## Things I want to know more about:

- How the react app effected if we don't add key value to listed items?
- Difference between spread and Rest?

## Sources:

- (1) [Lists and Keys](https://reactjs.org/docs/lists-and-keys.html)

- (2) [How to Use the Spread Operator in JavaScript](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

[Back to home page](../README.md)
