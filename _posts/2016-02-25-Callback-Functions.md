---
layout: defaultpost
title: "Callback Functions"
date: 2016-02-25
---

After rereading some of the JavaScript is Sexy blogs [Understand JavaScript Callback (Higher-Order) Functions](http://javascriptissexy.com/understand-javascript-callback-functions-and-use-them/){:target="_blank"} I finally understand the concept of a callback function and how to use them. Not only are they versatile but they allow for asynchronous programming.


```
function singSong(artist, song) {
  console.log(song + ’ is a song by ’ + artist);
  console.log(“Isn’t she lovely. Isn’t she wonderful.”);
}

function getSong(firstName, lastName, song, callback) {
  var fullName = firstName + ‘ ‘ + lastName;
  if (typeof callback === ‘function’) {
    callback(fullName, song);
  }
}

getSong('Stevie’, 'Wonder’, “Isn’t She Lovely”, singSong);
```