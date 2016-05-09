---
layout: defaultpost
title: "Server Only"
date: 2016-05-04
---

Wait what? A server that communicates with other servers and no clients?! In what is known as server to server, instead of sending and receiving requests from clients, a server would send and receive requests to other servers.<br />
For this sprint, we have no client to interact with, and must use Node to store a url that a user types. But how can that be achieved without a JavaScript or jQuery click/submit function? By using a form element in html and specifying a method of POST, the form will submit data to wherever receives it. In Node, there are many modules and one of them is creating a new server. In the local server, by creating a function that gets the absolute path of wherever the index.html is located, node can receive that html and use it. And now when a user sends input in the text box, an event listener can be used in Node to listen for request data. That data will come in chunks, and it can be concatenated into a string that will act as a buffer of what the user sent. With that, the server now has access to data from the user without the need of a client.