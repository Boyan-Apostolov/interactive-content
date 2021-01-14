# Lists And Keys

[slide]

# Lists

When we work with lists or collections of data we will use the `map()` method.

Here is an example of using the `map()` method on a collection.

```js
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((number) => number * 2);
console.log(doubled); 
```

Here is how we render multiple components.

Use the `map()` method to create a "li" element with the **current number** inside of it surrounded by curly braces like so: `<li>{number}</li>`.

Then we return an unordered list with all the elements from the "ListItems" variable.

```js
function NumberList(props) {
    const numbers = props.numbers;
    const listItems = numbers.map((number) =>
        <li>{number}</li>
    );
    return (
        <ul>{listItems}</ul>
    );
);
```

[/slide]

[slide]

# Keys

What is important to know is that we should give the elements of the collection **unique keys**.

If we do not do that we will see a warning message in the browser.

Our application will be working and the data will be displayed successfully.

Although this is not going to cause a problem it is not the way React works.

We should give **unique keys** to the elements inside the array.

This way React can manage its state effectively by keeping track of any changes happening to any particular element in the collection.

The best way to pick a key is to use a string that uniquely identifies a list item among its siblings.

Most often we use id's as keys. They go inside the element, in this case a `<li key={some key}></li>` element.

```js
const todoItems = todos.map((todo) =>
    <li key={todo.id}>
        {todo.text}
    </li>
);
```

[/slide]

[slide]

# Extracting Components with Keys

Keys only make sense in the context of the surrounding array.

```js
function ListItem(props) {
  // Correct! There is no need to specify the key here:  
  return <li>{props.value}</li>;
}

function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    // Correct! Key should be specified inside the array.    
    <ListItem key={number.toString()} value={number} /> 
    );
  return (
    <ul>
      {listItems}
    </ul>
  );
}
const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);
```

[/slide]

[slide]

# Keys and indexes

Keys serve as a hint to React but they do not get passed to your components. 

Do not use indexes for keys if the order of the components may change! 

Just work with IDs as we have already mentioned. 

If you need the same value in your component, pass it explicitly as a prop with a different name.

Keys do not need to be globally unique but only among their siblings. 

They only exist **within the scope** of the `map()` method.

```js
function Blog(props) {
  const sidebar = (
      <ul>
        {props.posts.map((post) =>
            <li key={post.id}> 
                {post.title}
            </li>
        )}
    </ul>
  );
  const content = props.posts.map((post) => <div key={post.id}><h3>{post.title}</h3>
      <p>{post.content}</p>
    </div>
  );
  return (
    <div>
      {sidebar}
      <hr />
      {content}    
    </div>
  );
}

const posts = [
  {id: 1, title: 'Hello World', content: 'Welcome to learning React!'},
  {id: 2, title: 'Installation', content: 'You can install React from npm.'}
];
ReactDOM.render(
  <Blog posts={posts} />,
  document.getElementById('root')
);
```

With the example above, the "Post" component can read `props.id`, but not `props.key`.

[/slide]