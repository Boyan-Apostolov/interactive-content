# Virtual DOM

[slide hideTitle]

# What is Virtual DOM?

The **virtual DOM** represents the real DOM, kept in the browser.

This **virtual DOM** is a React concept kept in the memory by the **ReactDOM** library.

**ReactDOM** library syncs the real DOM with the virtual one.

The React elements associated with **Virtual DOM** represent the user interface.

Generally, React tracks all components in the Virtual DOM and keeps the **order** of the operations.

When a change happens in the virtual DOM, a **diffing algorithm** compares it with the real DOM.

This algorithm returns what is updated, and React knows which component to modify.

React has a **declarative** syntax.

In this syntax, we need to describe the result, and it will show in the browser.

[/slide]
