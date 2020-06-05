---
layout: post
title: Project 1 Reflection
---

Project 1 was about reading JSON data from a web API and summarizing that data in a vignette.

Thankfully, the NHL's API was consistently structured and easy to parse with the `jsonlite` and `httr` packages. I didn't have any issues with the actual data retrieval.

## Things to Improve

In hindsight, it would've been useful to look at a list of all of the columns in each of the tables and try to understand the relationships better between them before diving into creating numeric summaries of them. I had to revisit some work because I had made assumptions about what certain columns represented and their relationships to other tables. Getting an understanding of the relationships beforehand would have saved me a lot of time!

It also would have been useful to do a little more research into the meanings of some of the column names beforehand. I'm not sure if that documentation exists, but column names like `activePlayer` in context of franchise records ended up misleading me, as I'll touch on later.

Finally, I wish I could have dedicated more time to the process of brainstorming questions to ask about the data in my exploratory data analysis. While I feel like I asked some interesting questions and was able to answer them using the data, I feel that I could have dug a little deeper into why some of the results occurred, rather than accepting them at face value.

## Difficulties

One thing that I would have found useful would be a flag indicating if a player was currently active on a team in the team's records (e.g., skater and goalie records). The `activePlayer` field refers to a player's active status in the whole NHL, not on a particular team. I was able to find the information in another table and join it to the data I wanted, but I feel that the redundancy would have been worthwhile for this particular data.

The other difficulty I had was in joining some of the data. It was a process of understanding the syntax behind some of the joins, but eventually I figured it out.

## Takeaways

I haven't used the tidyverse packages very much until this class. I've really enjoyed working with them in this project, particularly with the pipe operator (`%>%`). I feel like it makes the code so much more readable! The operations that the tidyverse offers also seem to encompass most of my raw data operations in R. It's nice to be able to use tools in R that all follow the same general syntax.

I really enjoyed creating graphs with the `ggplot` package. After reading the chapter on visualization in the *R for Data Science* book, things made a lot more sense to me with regard to how some of the syntax is laid out. The `ggplot` cheatsheet was very helpful in creating many of the graphs.

I felt that I was better able to make inference from the graphs than from the numeric summaries. Something about visualizing the information makes it much more understandable to me for some reason.

## Website

My project's website is available here: <https://jubilant.me/st-558-project-1/>.
