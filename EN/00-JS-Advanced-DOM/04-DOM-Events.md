[slide]

# DOM Events

DOM events are **specific actions** that happen at a given time.

They could be as simple as:

- `Pressing a key`

- `Clicking with the mouse`

- `Scrolling up and down`

- `Dragging an item across the page`

These events are useful because they can be **tracked** and **handled** whenever they happen.

DOM events are typically used together **with a handler function**, which is executed **after** the event as a reaction to it.

Here is an example of how to attach a handler for an event:

```js
h1Ref.addEventListener("click", handlerFunction);
```

In the example above the `handlerFunction` is attached to the `h1Ref` and is to be executed **after** the element has been **clicked**.

The `addEventListener` method accepts the following parameters:

- `Type of event`

- `The function to handle the event`

There is another optional parameter to this method, which will be covered later.

[/slide]
