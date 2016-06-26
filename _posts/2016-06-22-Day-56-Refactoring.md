---
layout: defaultpost
title: "Refactoring"
date: 2016-06-22
---

The components and containers we wrote didn't make use of routing, and some were children of other components when they shouldn't be. I spent the day refactoring components and containers to work correctly with react-router and nested routes since we now had a lot more to show on the front-end.<br />
One of the containers, Metrics, was a child of SentimentPlot, a d3 graph container. However, Metrics is its own feature in which it shows the user key statistics of our data whereas SentimentPlot is an independent container. But the way Metrics was getting Reddit and Twitter data was through props from its parent, and since I removed it from its parent and instead made it render as its own route, it no longer had access to the Reddit and Twitter data. I had to refactor it using state from Redux with mapStateToProps. This meant changing a lot of variables from this.props.data to this.props.reddit.data...etc. In the end I managed to fully convert it to using Redux as well as synchronized our app's routing to work with nested routes and multiple components.