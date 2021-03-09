# Middleware

[slide hideTitle]

# What is a Middleware?

A **middleware** is a **function** that has access to:

- The **request** object (`req`)
- The **response** object (`res`)

- The **next middleware function** in an application's **request-response cycle**:
  - The `next` keyword is most commonly used to designate it;
  - Utilised to create a **middleware stack**.

We use middleware functions to:

- **Execute** any code in the function body;
- **Modify** the **request** and **response** objects;

- Call the **next middleware** in the stack.

- **End** the **request-response cycle**.

## How to load a Middleware

To load **our middleware**, we utilize the `app.use()` method which accepts our function as a parameter.

Here is a simple example:

```js
var express = require("express");
var app = express();

app.use(function (req, res, next) {
  console.log("Hello World!");
  next();
});
```

First, we **import** the `express` framework.

Then we create a new instance of the **app object**.

We hand over our middleware function to the `app.use()` method.

In the function body we have called the `console.log()` method with a simple string.

We call the **next function**, if such exists in the **middleware stack**, with the help of `next()`.

[/slide]

[slide hideTitle]

# Types of Middleware

We can use **Application-level** middleware by declaring `app.use()`, which we discussed earlier.

We can also use the `app.METHOD()` function to create **route-specific** middleware.

## Router-level middleware

**Router-level** middleware is very similar to the application-level middleware.

One **main difference** is that we **bound it** to an instance of `express.Router()`, instead of `express()`:

`const router = express.Router()`

To load router-level middleware, we use the `router.use()` or `router.METHOD()` functions:

```js
const express = require("express");

const app = express();

const router = express.Router();

router.use((req, res, next) => {
  console.log("Time:", new Date());
  next();
});
```

## Error-handling middleware

**ExpressJS** comes bundled with **error-handling parameters** by **default**.

We define **error-handling middleware** functions in mostly the same fashion as other middleware functions.

The main characteristic of error-handling functions is that they accept a fourth argument \- the `error` object:

```js
app.use(function (err, req, res, next) {
  console.error(err.stack);
  res.status(404).send("This page does not exist.");
});
```

In this example, we call the `console.error()` with the error stack as a parameter.

We also assign a status of "**404 - Not Found**" to the response object.

## Third-party middleware

**Third-party middleware** enables a lot of **additional functionality**.

We install third-party middleware as any other **Node.js module**:

`npm install name-of-middleware-module`

After it finishes installing, we have to **import it**, either at the application level or at the router level.

We will use the `cookie-parser` module as an example:

```js
const express = require('express');
const cookieParser = require('cookie-parser');
const app = express();

app.use(cookieParser()));
```

Assuming we have already run `npm install cookie-parser`, our next step is to import it into our file:

`const cookieParser = require('cookie-parser');`

Then we load the cookie-parsing middleware as follows:

`app.use(cookieParser())`

[/slide]

[slide hideTitle]

# Custom Middleware

We can create **custom middleware** only for a **specific path**.

The `app.use()` and `app.METHOD()` functions can accept a string-formatted **route** alongside the **middleware function** as parameters:

```js
app.use("/post/:postId", (req, res, next) => {
  const postId = req.params.postId;

  let postExists = postId !== undefined;

  if (!postExists) {
    res.redirect("/home");
  } else {
    next();
  }
});

app.get("/post/:postId", (req, res) => {
  res.send("Post details");
});
```

In this example, we check if a blog post with a given `postId` exists in a database.

Depending on that, we either redirect the user to the homepage or show more information about the post.

[/slide]

[slide hideTitle]

# Third-Party Middleware

There is a lot of **third-party middleware**, which enables extra features.

The following table showcases some commonly used middleware and their use cases:

| **Middleware module** | **Description**                                                                         |
| --- | --- |
| `body-parser`         | Parses the body of an HTTP request.                                                     |
| `cookie-parser`       |  Parses the header of a cookie. Populates the `cookies` property of the request object. |
| `errorhandler`        | Enables debugging and error handling in the developer environment.                       |
| `cors`                | Enables cross-origin resource sharing (CORS).                                           |
| `serve-static`        | Used to serve static files.                                                             |

[/slide]