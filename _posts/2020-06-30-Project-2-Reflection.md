---
layout: post
title: Project 2 Reflection
---

Project 2 was about buildling statistical models and automating report creation.

## Things to Improve

The first that that I would do differently would be caching model building results from the beginning. I spent a lot of time waiting for my random forest models to complete building, only to make a change and have the Knitted document build the same model again. Parallelization helped a lot, but it would still take 10-15 minutes for a random forest model to build. I eventually turned on the cache option in the block, which saved time, but I also realized that I had to change the cache directory once I started automating report creation because by default, `knitr` uses one cache directory.

The second thing that I would do differently would be to experiment with regression models before trying classification. I would have at liked to see how a multiple linear regression model would have performed on the data, particularly with some huge outliers in some of the `shares` data. I'm happy that I chose the classification approach because I was able to compare my results with what was achieved in the academic paper, but even some minor exposure to the linear regression model may have been interesting.

## Difficulties

The biggest difficulty that I had was in performing variable selection for the logistic regression model, where I hit several snags. I wanted try and use as many variables as I could and try to use programmatic ways to select the best ones. I wanted to use stepwise selection to select a subset of variables, but with 50 predictor variables, I found that the packages I tried to use took a long time to process and I got impatient. I also wanted to try using a genetic algorithm for variable selection using the `caret` package, but was unable to get it working after multiple hours of trying. I found a number of websites saying that stepwise selection is a poor way to do variable selection in logistic regression.

I ended up using Lasso regularization to act as a form of feature selection for my model, and used the lambda value as a hyperparameter that could be tuned with k-fold cross-validation. It just took me a while to figure out the best way to do feature selection for logistic regression.

## Takeaways

* The `caret` package was very useful in automating a lot of the boilerplate behind model building. It kept the code readable and made it easy to preprocess, train, and make predictions.
* Parallelization saves a lot of time. I used 8 CPU cores in my model building process.
* Variable selection is a difficult process. No wonder there are so many methods that people use to do it!
* Model tuning is a very time-consuming process. I'm glad that the `caret` package provides tooling to help with hyperparameter selection!

## Website

My project's website is available here: <https://jubilant.me/st-558-project-2/>.

The code is available here: <https://github.com/arharvey918/st-558-project-2/>.
