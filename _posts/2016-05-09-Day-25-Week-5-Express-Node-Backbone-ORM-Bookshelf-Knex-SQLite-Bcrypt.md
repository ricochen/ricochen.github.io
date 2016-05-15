---
layout: defaultpost
title: "Week 5 Express Node Backbone ORM Bookshelf Knex SQLite Bcrpyt"
date: 2016-05-09
---

Wow, did I just list a bunch of random libraries and buzzwords? Nope, I actually used all of these in the current sprint to create a Bitly clone. Bitly is a tool that shortens URLs, and is especially useful for when there is a max character count such as Twitter's tweets. With so many libraries, where do I even begin? Having to sift through tabs and tabs of documentation and knowing when to use which method is a sprint in itself. There were times I thought I could use Knex to do an SQL query, only to find out there is a Bookshelf module exported from the server file, and to use Bookshelf instead.<br />
More importantly, why do I need all of these libraries that only create more abstraction? I can achieve the same result with just a few of the necessary ones. I think it's a good introduction to some useful tools that I can choose to use for future projects. But the real reason is because some of these libraries are extremely useful in that they act as wrappers over the original application.<br />
Express, for example, makes using Node a lot easier as it abstracts away many common Node modules and methods. Three lines in Express can be equivalent to many lines in Node, making the code less verbose while maintaining readability, and that is a plus in my books...or should I say libraries?