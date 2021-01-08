# Fetch API

[slide]
# Fetch API: Description

The **Fetch API** provides an interface for accessing and manipulating requests to servers from web browsers.

`fetch()` function which provides easy way to access data from an API asynchronously.

Functionality like this was previously achieved using `XMLHttpRequest`.

The `fetch()` function accepts **one argument**, which will be the URL to which send the request. 

By default a `GET` request is sent, if we want to send other requests, we will have to set them up by passing a **second** argument to the function.

Fetch returns `promise`, where we can use `then` and `catch` so can catch errors if they occur or catch the result which returns API itself.

For more information, see the fetch [documentation](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) itself.

[/slide]

[slide]
# Fetch API: Example

In this example we access GitHub API, we can only access publicly open routs.

```js
fetch('https://api.github.com/users/k1r1L')
    .then((response) => response.json())
    .then((myJson) => console.log(myJson))
    .catch((myErr) => console.error(myErr));
```

We `fetch()` a given user by username. 

When we **successfully** fetch a user, we get a promise, which we call `response.json`, which will return the data in the form of JSON. 

Once we have the data, we are free to start using it in context, or we can update the state.

With `catch()`, we can catch errors.

Result:

[image assetsSrc="Compenents-Deep-Dive-3.png" /]

[/slide]

[slide]
# Fetch API: Example(2)

Fetch can be used **asynchronously**, it is depending on us what to use asynchronously or not.

Best practice to use `async` `await` so we can take advantage of the better performance.

```js
(async () => {
  try {
    const response = await fetch('https://api.github.com/users/k1r1L');
    const myJson = await response.json();
    console.log(myJson);
  } catch (myErr) {
    console.error(myErr);
  }
})();
```

Result:

[image assetsSrc="Compenents-Deep-Dive-4.png" /]
[/slide]

[slide]
# Fetch Services

The basic idea is to isolate the concern of fetching data inside components.

Fetching data logic should separated as service.

```js
const apiUrl = '...';

export const getData = () => {
    return fetch(apiUrl)
        .then(res => res.json())
        .then(data => data.results)
        .catch(error => console.error(error))
};

```

In this example, we have the function `getData` and return a response.

This is the best way we can fetch data because we do not **unnecessarily** contaminate our components.

We separate the logic of data acquisition and creation, where we can use only functions that we need.

[/slide]

[slide]
# Fetch Services: Usage

When we separate data retrieval in a service, we can insert that service into components and use them.

```js
import { getData } from 
'./services/fetching-data-service';

class App extends Component {
  state = {
    data: ...
  };
  componentDidMount() {
    getData().then((data) => {
      this.setState({ data })
    });
  }
  render() {
    return ...;
  }
}
```

[/slide]