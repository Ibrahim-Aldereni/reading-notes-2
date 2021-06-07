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

---

## Things I want to know more about:

## Sources:

- (1) [Lists and Keys](https://reactjs.org/docs/lists-and-keys.html)

[Back to home page](../README.md)
