[slide hideTitle]

# Problem with Solution: Blog

**Here is a link to the** [resources](https://videos.softuni.org/resources/javascript/javascript-applications/01-JS-Application-Asynchronous-Programming-Lab-Resources.zip) **for this task.**

Create a program for reading blog content.

It needs to make **requests** to the **server** and display **all blog posts** and their **comments**.

[Firebase URL](https://blog-apps-c12bf.firebaseio.com/)

Skeleton will be provided in the **Resources folder**.

The button with ID `btnLoadPosts` should make a **GET** request to `/posts`. 

The **response** from the **server** will be an **Object of objects**.

```
{-LhdbZ31ND3Rhw41UGMN: {..}, -Lhdc-Ttz9-KiWSuvh6W: {...}, -LhdcLmyARLEBibsSvjZ: {..}, -LhdccRyWr_7UCPtclmM: {..}}
-LhdbZ31ND3Rhw41UGmN: {body: "An asynchronous model allows multiple things to ha...he result (for example, the data read from disk).", id: "rrt87...
-Lhdc-Ttz9-KiW9uvh6W: {body: "In a synchronous programming model, things happen ...stops your program for the time the action takes.", id: "rrt87...
-LhdcLmyARLEB1bsSvjZ: {body: "One approach to asynchronous programming is to mak... the callback function is called with the result.", id: "rrt87...
-LhdccRyWr_7UCPtclmM: {body: "Working with abstract concepts is often easier whe...turn an object that represents this future event.", id: "rrté87...
__proto__: Object

```

Each object will be in the following format:

```js
{
    body: {
        postBody
    },
    id: {
        postId
    },
    title: {
        postTitle
    }
}
```

Create an `<option>` for each post using its **object key** as value and **current object title property** as text inside the node with ID "**posts**".

[image assetsSrc="JS-Applications-Asynchronous-Programming-Lab-2.jpg" /]

```js
<select id="posts">
   <option value="-LhdbZ31ND3Rhw41UGmN">ASYNCHRONOUS PROGRAMMING</option>
   <option value="-Lhdc-Ttz9-KiW9uvh6W">SYNCHRONOUS PROGRAMMING</option>
   <option value="-LhdcLmyARLEB1bsSvjZ">CALLBACKS</option>
   <option value="-LhdcecRyWr_7UCPtclmM">PROMISES</option>
</select>
```

When the button with ID "**btnViewPost**" is clicked, a **GET** request should be made to:

- `/posts/{postId}` to obtain the selected post (from the dropdown menu with ID "**posts**")

The following **request** will return a **single object** as described above

- `/comments`: to obtain all comments

The request will **return** an **Object of objects**.

```
{-LhdewtO2LIrzuThWlMj: f..}, -LhdfHFg8dNxK-qUaukL: {..}, -LhdfVg4IDKa@Cft-dQZ: {..}, -LhdfuAXoimPycgRRFf-3: {..}, -Lhdg@x8QG-j2vnNUALS: {..}, .}
-LhdewtO21IrzuThW1IMj: {id: "rrt8713kjxljda5r", postId: "rrt875tgjxlimgqb", text: "So good article. Nice!"}
-LhdfHFg8dNxK-qUaukL: {id: "rrt878p@jxljdgze", postId: "rrt87Stgjxlimgqb", text: "Rly helpful. Thanks!"}
-LhdfVg43IDKa@Cft-dQZ: {id: "rrt879ccjx1jd0@3", postId: "rrt879rkjxlimol2", text: "Now I understand it... Thanks!"}
-LhdfuAXoimPycgRRf-3: {id: "rrz123cjxhhfdoti443", postId: "rrt87twjxlimswr", text: "Amazing article! Good job!"}
-Lhdg@x8QG-j2vnNUh1S5: {id: "rrzi23smshhfdoti543", postId: "rrt87twjxlimswr", text: "You are the best! +1 For this Article!"}
-LhdgPKifSsYTJYN61SQ: {id: "rrz35smshhfdfti543", postId: "rrt87btcjxlimxui", text: "Good job my man! You are the best!"}
-LhdgZwm5UCF6eoSvU6g: {id: "rrz35sshshfdftid44", postId: "rrt87btcjxlimxui", text: "AMAZING ARTICLE! It's was pleasure to read it! Thanks bro!"}
-LhdghH3EHO1FrBesCcCp: {id: "rrz404smshshfdfti4e4", postId: “rrt87btcjxlimxui", text: "It was ok, next time you will crush them!"}
__proto__: Object

```

Each object will be in the following format:

```js
{
    id: {
        commentId
    },
    postId: {
        postId
    },
    text: {
        commentText
    }
}
```

You have to find these comments that are for the current post (check the **postId property**).

Display the post title inside `h1` with ID "post-title" and the post content inside ul with ID "post-body".

Display **each comment** as a `<li>` inside ul with ID "post-comments".

Do not forget to clear its content beforehand.

[image assetsSrc="JS-Applications-Asynchronous-Programming-Lab-5.jpg" /]

```js
<h1 id="post-title" >ASYNCHRONOUS PROGRAMMING</h1>
<p id="post-body" >
   "An asynchronous model allows multiple things to happen at the same time. When you start an action, your program
   continues to run. When the action finishes, the program is informed and gets access to the result (for example, the
   data read from disk)."
</p>
<h2>Comments</h2>
<ul id="post-comments">
   <li id="rrt8713kjxljda5r">So good article. Nice!</1li>
   <li id="rrt878pe@jxijdgze">Rly helpful. Thanks!</1i>
</ul>
```

[/slide]

