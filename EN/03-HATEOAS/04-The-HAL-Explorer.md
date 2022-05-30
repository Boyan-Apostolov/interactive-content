[slide hideTitle]

# HAL Explorer

[video src="https://videos.softuni.org/hls/Java/Java-Spring-Advanced/EN/03-HATEOAS/21-hal-explorer-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

The HAL Explorer provides us with a graphical representation of our API.

It allows us to view each response, along with available actions, response statuses and headers.

Begin by adding the HАL Explorer as a Maven dependency in `pom.xml`:

```xml
<dependency>​
     <groupId>org.springframework.data</groupId>​
     <artifactId>spring-data-rest-hal-explorer</artifactId>​
</dependency>​
```

[/slide]

[slide hideTitle]

# Example

In this example, we try to access `http://localhost:8080/students`:

[image assetsSrc="Java-Spring-Advanced-HATEOAS-1.jpg" /]

For each relation, the Explorer lists the available HTTP methods.

It also displays embedded resources in an organised way:

[image assetsSrc="Java-Spring-Advanced-HATEOAS-2.jpg" /]

This is what they look like in plain JSON:

[image assetsSrc="Java-Spring-Advanced-HATEOAS-3.png" /]

In this snippet, we see the first student (with an id of 1), along with available links to `self`, `student` and `orders`.

[/slide]