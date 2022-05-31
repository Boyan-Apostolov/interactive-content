# Exception Techniques Use Cases

[slide hideTitle]
# What to Use When

[video src="https://videos.softuni.org/hls/Java/Java-Spring-Advanced/EN/04-Error-Handling/28-use-cases-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Spring offers **many choices** when it comes to **error handling**.

Be careful mixing **too many of these**, because we may not get the wanted behavior.

Especially when using **REST API**, it is recommended HTTP response status codes be used.

In all other cases, we **can redirect** the user to a nice-looking error page.

There is some semantics, that should be followed, though.


[/slide]

[slide hideTitle]
# Exception Techniques Use Cases

For custom exceptions, consider adding `@ResponseStatus` to them.

For Controller-specific exceptions, `@ExceptionHandler` methods should be added alongside the actions.

For all other exceptions, `@ExceptionHandler` methods in `@ControllerAdvice` classes should be implemented.


[/slide]