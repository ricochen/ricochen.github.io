---
layout: defaultpost
title: "Asynchronous"
date: 2016-04-21
---

After reading the 5 cores for the first half of the sprint, today we started on the coding portion. The goal is to make features of a reminder app work while keeping the code modular and organized. The modules are separated by their functionality, so there is a module for functions, data and variables that are used for the login portion, a module for the reminder functionality, etc. This makes the code a lot easier to read as they are grouped by their purpose and makes private data inaccessible to the user.<br />
There is a node server hosted locally that contains data on a few users: their login, password, session ID, and reminders that they have written. When a user logs in, their username and password is sent to the server using jQuery's ajax function, which checks to see if it is valid, and if so makes an asynchronous callback to return that user's session ID. The user is redirected to an http url that contains their session ID and from there the dashboard is displayed, along with other functionalities like add reminder and delete reminder.<br />
The takeaway from this is to use modules to prevent polluting the global namespace and not have random function calls everywhere, and also to understand how asynchronous programming works and how powerful it is as it doesn't stop the thread that JavaScript runs on like synchronous programming does if there's a bug, but instead will wait until it is ready to be called.