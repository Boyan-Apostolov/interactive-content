# Softuni Forum Workshop: Part 2

[slide hideTitle]

# Task Requirements

**Here is a link to the** [resources](https://videos.softuni.org/resources/javascript/javascript-angular/06-Modules-And-Routing-Workshop.zip) **for this task.**

We have created one dynamic page which lists all the themes sorted by two different criteria. 

The next step is to implement a few more pages and routes between them. 

Use the **HTML** and the **CSS** skeleton for all other additional pages that you must create. 

There is one catch, half of these pages require **authentication**. 

You must create some properties or services that **fake this authentication**. 

Because we do not know yet how to manipulate forms properly or the real case with the authentication and authorization, we will fix that later when we have the knowledge to do so.

[/slide]

[slide hideTitle]

# Logged in navigation bar

**Logged in**" "**user**" should be able to see the following navigations:

[image assetsSrc="Angular-Modules-And-Routing-Workshop.png" /]

The mini nav-bar includes:

**User's profile** - this tag should refer to the profile page `localhost:4200/profile`.

**Logout** - a tag that refers to the logout URL `localhost:4200/logout`.

The nav-bar below the logo of the SoftUni forum includes:

**Home** - a tag that leads to the **Home** page `localhost:4200/home`.

**Themes** - a tag that leads to all **Theams** page `localhost:4200/themes`.

**New Theme** - a tag for creating a **Theme** `localhost:4200/add-theme`.

[/slide]

[slide hideTitle]

# Not logged in navigation bar

"**Not logged in**" users should see the following navigations:

[image assetsSrc="Angular-Modules-And-Routing-Workshop(1).png" /]

The mini nav-bar includes:

**Login** - a tag that leads to the **Home** page `localhost:4200/login`.

**Register** - a tag that leads to the **Register** page `localhost:4200/register`.

[/slide]

[slide hideTitle]

# Home page - Not Logged in

This is the home page URL `localhost:4200/home`. This is a welcome user page. 

We can reuse the **Welcome** component here.

All "**users**" can access this page when they visit the forum. 

Here is how it looks like before the user has logged in:

[image assetsSrc="Angular-Modules-And-Routing-Workshop(2).png" /]

[/slide]

[slide hideTitle]

# Home page - Logged in

Logged in users will see the following view:

[image assetsSrc="Angular-Modules-And-Routing-Workshop(3).png" /]

[/slide]

[slide hideTitle]

# Register - Not Logged in

This is the URL of the register page `localhost:4200/register`. 

At this point change the fake **isLoggedIn** property to **true**. 

For now, we do not have a database with user registration, so make sure each registered user is stored in **userService** or some other appropriate place. 

This way each of them can be logged in successfully.

[image assetsSrc="Angular-Modules-And-Routing-Workshop(4).png" /]

[/slide]

[slide hideTitle]

# Login - Not Logged in

This is the URL of the login page `localhost:4200/login`. 

Change the fake **isLoggedIn** property to **true**. 

For now, we do not have a database with user registration, so make sure each registered user is stored in **userService** or some other appropriate place. 

[image assetsSrc="Angular-Modules-And-Routing-Workshop(5).png" /]

[/slide]

[slide hideTitle]

# Themes page - Not Logged in

This is the themes page URL `localhost:4200/themes`.

All "**users**" can access this page when they visit the main forum page. 

By clicking the title of a theme, you will be redirected to the theme content view. 

There are several differences between the logged and anonymous user. 

The anonymous user should see the following:

[image assetsSrc="Angular-Modules-And-Routing-Workshop(6).png" /]

[/slide]

[slide hideTitle]

# Themes page - Logged in

This is the themes page URL `localhost:4200/themes` for logged in users.

Note: Because you are still not logged in, you can **hardcode** this userId `5fa64b162183ce1728ff371d` in your service to write your logic for subscribed users - **Red** and **Green** buttons.

[image assetsSrc="Angular-Modules-And-Routing-Workshop(7).png" /]

[/slide]

[slide hideTitle]

# Theme comments - Not Logged in

Note: Because you are still not logged in, you can **hardcode** this userId `5fa64b162183ce1728ff371d` in your service to write your logic regarding the subscribed users - **Red** and **Green** buttons.

[image assetsSrc="Angular-Modules-And-Routing-Workshop(8).png" /]

[/slide]

[slide hideTitle]

# Theme comments - Logged in

**Logged in** user can write new comments or like other user's posts.

[image assetsSrc="Angular-Modules-And-Routing-Workshop(9).png" /]

[/slide]

[slide hideTitle]

# Create New Theme - Logged in only

Create the new theme page URL `localhost:4200/themes` where each logged-in user can create a theme.

When the "**Post**" button is clicked, you can try to make the "**POST**" request to `localhost:4200/themes` with the given theme information. 

After successful creation, redirect the current "**user**" to the theme comments page.

When the "**Cancel**" button is clicked, redirect the user to the **Home** page.

[image assetsSrc="Angular-Modules-And-Routing-Workshop(10).png" /]

[/slide]

[slide hideTitle]

# Profile - Logged in

This is the profile page URL `localhost:4200/profile`. 

This page will show the information about the currently logged-in user. 

For now, the data on this page will be static, except if you create more than the fake **isLoggedIn** property. 

The "**Edit**" button will replace the information fields with input fields, but this will be made in the next workshop when you learn more about handling forms.

[image assetsSrc="Angular-Modules-And-Routing-Workshop(11).png" /]

[/slide]

[slide hideTitle]

# Invalid routes

The page URL for all invalid routes `localhost:4200/??????`. 

Use it if an invalid path or wrong one is accessed.

[image assetsSrc="Angular-Modules-And-Routing-Workshop(12).png" /]

[/slide]

[slide hideTitle]

# Protected routes

Make sure all logged-in user pages are protected. 

That means if your fake "**isLoggedIn**" property is **false** the logged-in pages cannot be accessed. 

Create authentication guards.

[/slide]

