[slide hideTitle]
# Summary


# In this lesson you learnt:

- Error boundaries are special React components that handle errors while a given component renders
  - The errors must occur in the child component tree

```js
class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { 
      hasError: false
    };
  }

  static getDerivedStateFromError(error) {
    return { 
      hasError: true
    };
  }

  componentDidCatch(error, errorInfo) {
    logErrorToService(error, errorInfo);
  }

  render() {
    if (this.state.hasError) {
      return <h1>Please try again later</h1>;
    }

    return this.props.children; 
  }
}
```


- Jest and Enzyme are used together for testing purposes
  - Jest is a test runner, assertion, and mocking library
  - Enzyme is a testing utility with additional functionality

```js
/// ...
import ListItem from './ListItem';
/// ...

return (
    <ul className="list-items">
      {items.map(item => <ListItem key={item} item={item} />)}
    </ul>
  );
```

```js
/// ...
it('renders list-items', () => {
    const items = ['one', 'two', 'three'];
    const wrapper = shallow(<List items={items} />);

    // Let's check what wrong in our instance
    console.log(wrapper.debug());

    // Expect the wrapper object to be defined
    expect(wrapper.find('.list-items')).toBeDefined();
    expect(wrapper.find('.item')).toHaveLength(items.length);
  });
/// ...

```
- Server\-side rendering improves performance and increases response time
  - Search engine optimization increases page visibility


[/slide]
