---
layout: defaultpost
title: "Alchemy API"
date: 2016-06-24
---

Oh man, I think today is the first time I've ended up working more backwards than forwards. My sprint involved using the alchemy news API to retrieve the top news headlines for the week. Then I would send it through our sentiment function as well as render a few of the news links in the client and a snippet of the article body. It was going well, and I spent the majority of the day creating an API handler in the back-end and parsing the data to only send the url, title, text, and date to the client. As well as creating an action, reducer and container on the front-end to receive and render the alchemy data. BUT, I found out the hard way that alchemy only allows 1000 events per day in the free version. And each GET request amounted to about 40 events. I ended up hitting the daily limit. Also, alchemy's API key expires after 15 days unless I provide a credit card.<br />
At that point we concluded alchemy would not work with our app, and we went to find a new API for news headlines. I salvaged the remaining time I had in the day and created a d3 pie chart. Somehow, I got it to work with our Reddit and Twitter data and render in the client before the day ended, so at least I have that going for me.