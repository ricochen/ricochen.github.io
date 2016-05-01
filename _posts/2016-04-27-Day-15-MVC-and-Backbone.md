---
layout: defaultpost
title: "MVC and Backbone"
date: 2016-04-27
---

The idea of a MVC is pretty cool. It stands for model, view, controller and makes listening to events and triggering updates a lot easier than writing those functions from scratch. One of the things I thought about in the previous sprint was how to automatically update the client whenever data in the backend is changed due to another client's actions. A naive way would be to use setTimeout or setInterval, but now I see that MVCs fix exactly this problem.<br />
With MVC, a model is usually created to match a functionality, whether that be the entire app, a friends list, or a song queue. It handles the logic for the application data. A view is connected to a model, and listens for events, in which it handles display of the data. A controller is the part of the application that handles user interactions and lets the model know which events have occurred.<br />
The MVC framework for this sprint is Backbone and it is one of the harder frameworks to understand. Nonetheless, I appreciate its purpose, and am going to dive into the documentation to fully understand it. One of the best parts though is that Backbone uses modules, which is one of my favorite ways to organize code because of its readability.