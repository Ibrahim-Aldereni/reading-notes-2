# **Thinking in React:**

- **How would you break a mock into a component heirarchy?**

  By drawing boxes around every component (and subcomponent) in the mock and give them all names.

- **What is the single responsibility principle and how does it apply to components?**

  It means that the component should do one thing only.

- **What does it mean to build a ‘static’ version of your application?**

  It means we don't want to add interactivity and states.

- **Once you have a static application, what do you need to add?**

  You need to add states.

- **What are the three questions you can ask to determine if something is state?**

  1. Is it passed in from a parent via props?
  2. Does it remain unchanged over time?
  3. Can you compute it based on any other state or props in your component? (1)

- **How can you identify where state needs to live?**

  - Identify every component that renders something based on that state.
  - Find a common owner component (a single component above all the components that need the state in the hierarchy).
  - Either the common owner or another component higher up in the hierarchy should own the state. (1)

---

## Things I want to know more about:

- How to Break The UI Into A Component Hierarchy?

## Sources:

- (1) [Thinking in React](https://reactjs.org/docs/thinking-in-react.html)

[Back to home page](../README.md)
