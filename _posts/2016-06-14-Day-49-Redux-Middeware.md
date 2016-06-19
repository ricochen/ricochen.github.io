---
layout: defaultpost
title: "Redux Middeware"
date: 2016-06-14
---

Yes! I understand how to use middleware and async actions in Redux now! It was mainly because I watched the entire section on Redux middleware today from the Udemy video series. It's actually really easy to handle promises with middleware, because the middleware will handle the async portion automatically.<br />
For example, I'm using an action to make a POST request to the server, which triggers the server to make a GET request to Twitter's API for tweets. After the GET request is resolved, the server sends the Twitter data to the client. I had trouble doing this at first with just actions and reducers, because I didn't have direct access to the promise that axios returns to use .then() in the component. But with a library called redux-promise, which applies middleware to the application between the actions and the reducers, it will check if an action has a payload property, and if that payload is a promise. If it is, it will wait until the promise is resolved and return the response object to the reducer, which can then be accessed in the container through mapStateToProps. If action.payload is not a promise, it will allow the action through normally.<br />
The steps above is exactly what I did in my app, and when I saw the list of tweets coming back from the server on the client side, (warning nerdy statement ahead) it felt like I just defeated the final boss in a Redux dungeon! Next, I will have to use React and Redux alongside d3 to create data visualizations.