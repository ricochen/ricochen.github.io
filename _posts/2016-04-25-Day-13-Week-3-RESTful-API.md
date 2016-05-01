---
layout: defaultpost
title: "Week 3 RESTful API"
date: 2016-04-25
---

Diving into the world of HTTP and using RESTful API, there are four common verbs that are used to communicate between the server and client using ajax. GET is used to fetch data from the server to the client and is read only. POST is used when the processing that should happen on the server is meant to be repeated. PUT creates or updates a specified resource on the server. DELETE deletes a specified resource on the server.<br />
All four of these ajax requests have two outcomes, either success or failure and depending on the outcome will output a different status code. For example, 200 means the request was successful.<br />
The only safe method is GET, as the other three can modify a resource, so it's important to fully understand the data beforehand.