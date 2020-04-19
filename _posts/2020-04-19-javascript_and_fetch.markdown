---
layout: post
title:      "Javascript and Fetch "
date:       2020-04-19 22:06:34 +0000
permalink:  javascript_and_fetch
---

Fetch is a method used in javascript that provides an interface for asynchronous fetching of resources accross the network. Asynchronous means you can send a request for information and recieve a response without having to reload the browser or navagate to that resource. This allows you to perform multiple task at the same time to improve performance.

Fetch takes one madatory argument, the path to the resource you want to fetch `fetch(url)`. This fetch will return a promise. A promise is an object that represents the eventual completion or failure of an asynchronous operation and its reulting value. Once the pending promise is fulfilled with a value or error, an associated handler (`.then` or `.catch`) that is defined by the programmer is queued up and executed. 

```
fetch(url)
  .then((response) => {
    return response.json();
  })
  .then((data) => {
    console.log(data);
  });
```

In the first `.then` handler the `response` argument is the variable assigned to the promise recieved from the fetch. We then use a method `.json()` on the promise to convert the data to something useful, a javascript object. In the next `.then` handler the value of the `data` argument is what was returned from the previouse `.then`. At this point in the fetch, we can manupulate our data in the way that suites your application. In this example we just `console.log(data)`. 





