---
layout: defaultpost
title: "Promises"
date: 2016-04-20
---

I have good news, I'm finally done with all the reading for this sprint! The amount of content and level of depth covered in the past 3 days was like nothing I've ever done before, so I'm a little bit happy to say the least. The next 3 days will be strictly coding and putting into practice all the reading.<br />
One of the most important concepts I learned and read about is Promises. It is new to JavaScript and was released in ES2015. I've only touched on the surface of Promises, but it is a solution to callback hell as it does not allow inversion of control like callbacks do. Promises are also asynchronous meaning it's callback will not run until it's parent function is called, and in promises there are two outcomes: fulfilled and rejected. With promises, control is maintained in that a proprietary callback function is only called in the case of success, or fulfillment, or another proprietary function is called in the case of failure, or rejection. With promises, the callback function is not handed to a third party, where errors may be created by that third party because control is inverted to them, which is the case when using regular callbacks.<br />
There is a lot more about promises that I haven't addressed, and I will save that for when I have mastery over it.