---
layout: defaultpost
title: "React-Router"
date: 2016-06-16
---

The learning never ends! Right after learning and using redux-promise as middleware, I have to learn react-router to use in our app. The good news is I've gotten better at learning frameworks and libraries and can pick up new ones fairly quickly. React-router is used to show React components based on the path. For example, for an email application the root route '/' might just show a login component. Then when the user logs in, it will route to a different route like '/home', and show different components, such as the user's emails.<br />
Implementing react-router in our app wasn't nearly as hard as learning React and Redux. All it took was refactoring index.js to render a Router that has routes and browserHistory instead of the App component. And creating a routes file that renders react components based on the route, which is imported into index.js.<br />
Now a user will be brought to the home page when using our app, which includes a search bar. After searching for keywords that they would like to see data visualization and sentiment on, the URL path changes and renders the react components tied to that route. In other words, the search bar dissapears and graphs and KPIs are shown.