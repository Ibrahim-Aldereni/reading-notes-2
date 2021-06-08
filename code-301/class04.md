# **Forms:**

- **What is a ‘Controlled Component’?**

  React component that renders a form and controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.(1)

- **Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.**

We should update the state with their responses as soon as they enter them, because when we submit we need to take the state value and show it.

- **How do we target what the user is entering if we have an event handler on an input field?**

  By using `value` attributes that have a value in the state, then saving the targeted value in the state `{value: event.target.value}`

# **The Conditional (Ternary) Operator Explained:**

- **Why would we use a ternary operator?**

- **Rewrite the following statement using a ternary statement:**

  ```javascript
  if (x === y) {
    console.log(true);
  } else {
    console.log(false);
  }
  ```

---

## Things I want to know more about:

## Sources:

- (1) [Forms](https://reactjs.org/docs/forms.html)

[Back to home page](../README.md)
