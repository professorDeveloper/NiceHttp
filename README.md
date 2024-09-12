# NiceHttp Copied From Blatzar Thanks for Blatzar

[![](https://jitpack.io/v/Blatzar/NiceHttp.svg)](https://jitpack.io/#professorDeveloper/NiceHttp)

A small and simple Android OkHttp wrapper to ease scraping. Mostly for personal use.

Featuring:

- Document scraping using jsoup
- Json parsing using jackson
- Easy functions akin to python requests

## Getting started

### Setup

In build.gradle repositories:

```groovy
maven { url 'https://jitpack.io' }
```

In app/build.gradle dependencies:

```groovy
implementation 'com.github.professorDeveloper:NiceHttp:+'
```

### Scraping a document

```kotlin
lifecycleScope.launch {
    val requests = Requests()
    val doc = requests.get("https://github.com/Blatzar/NiceHttp").document
    // Using CSS selectors to get the about text
    println(doc.select("p.f4.my-3").text())
}
```

