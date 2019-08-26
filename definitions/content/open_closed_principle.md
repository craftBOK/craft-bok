---
type: content
tags: solid, principles
---
# Open Closed Principle

The **Open Closed Principle** is about the art of adding new features without endangering your system.

<div style="border: 2px dotted grey; padding: 10px">
Call for Action:

This article needs your input, please find related issues [here](github...).
We're looking for following content
* good videos
* online accessible resources in simple speech
* resources for kids
* nice visuals (preferrably PUML)
</div>

## Definition

A module should be open for extension, but closed for modification. [1]

## Code Examples

\[Expect Tabs here with different Programming Languages]

### Example in Java

* Consider this example from the repository
* What’s problematic here?

```Java
public class BadExample {
   public String contentOf(Types type, String url) {
       switch (type) {
           case FILE:
               return readFromFile(url);
           case HTTP: 
           case HTTPS:
               return readFromWeb(url);
       }
       return null;
   }

   private String readFromWeb(String url) { … }
   private String readFromFile(String url) { … }
}
```

\[Uncover the next step]

Consider the following context

```Java
public enum Types {
   FILE, HTTP, HTTPS, S3
}
```

\[Uncover the next step]

* Adding new known types will result in unexpected behaviour.
* Especially bad, when others rely on your system as a black box!

## Recommendations

### Goes well with

* SOLID (120 people recommended this) [upvote](#)
* [Pair Programming](pair_programming.md) (120 people recommended this) [upvote](#)

### Katas

For learning how to apply the open close principle you can use a Kata.
Choose one from [kata-log.rocks](http://kata-log.rocks/solid-principles.html) for example.

You can do them alone in a [pair](pair_programming.md) or as a [workshop](workshop-kata.md) 

#### List

* Racing Car Kata (Recommended by 10) [upvote](#)
* Submit a suggestion …

## Recommendedd Level

* **Seniority:** Learn at Junior level [vote](#)
* **Complexity:** Medium Complexity [vote](#)

## Read Further

* [1] Robert C. Martin, Design Principles and Design Patterns, Object Mentor, 2000 | [Link](http://staff.cs.utu.fi/staff/jouni.smed/doos_06/material/DesignPrinciplesAndPatterns.pdf)
