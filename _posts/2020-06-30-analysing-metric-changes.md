---
layout: post
title: Analyzing Metric Changes
date: 15-07-2020 12:00:00 +0800
categories: product
summary: A framework for analyzing metric changes in a product. There are things in your control and some that are not. How do you explain the change?
published: true
---
Analysing metric changes and measuring the performance of products is one of the most important responsibilities in the product. This leads to answering questions like (and more):

1. How do we increase engagement and conversion?
2. Is there a problem with the funnel?
3. Which of these two features/design options works better?

In this framework, I am outlining a way to think about 2 — is there a problem in the funnel? This would typically be in response to a metric changing significantly from its baseline. Mostly downwards. But upwards needs to be understood as well — it could point to a way to improve the product!

---

## TL;DR Version

Here’s a quick version of the framework to analyse metric changes. For a detailed explanation, continue reading below.

### Data Accuracy

1. Instrumentation pushing data to your analytics tool.
2. Does the tool have a bug?

### Patterns

1. Are there explainable patterns.

### Product

1. Were there recent product changes?
2. Check the data for explanations.

### Internal Factors

1. Were there recent changes shipped by other teams?
2. Check for business changes.

### External Factors

1. Check with your customers.
2. Check for changes in the competitive landscape and macroeconomic and natural environment.

---

## The Long Version

### Check for Data Accuracy

This should be the first step. There is no point diving into deep analysis if the data is not right. Garbage in, garbage out.

**Check the instrumentation pushing data to your analytics tool.** On the web, you can check the API calls. Or, better if your developers have built some sort of an add-on that allows you to check the data that is being pushed. (We had a custom Chrome Extension built for this purpose at Cleartrip.) Apps can also be tested similarly. But requires a bit more effort to debug along with the app development team.

Depending on the analytics tool you use, there might be another way to check if the data is accurate. If the tool allows you to inspect data at an individual user level, then you can perform a bunch of steps related to the metric you are tracking and check if the data shows up correctly in the tool. For example, we would go through a booking funnel and make a note of the search parameters, selections made and other inputs. Then check for the same against the user profile. Repeat this 2–3 times with different inputs to validate the data.

*Ideally, you should follow the steps above before a feature or product is launched to ensure that this doesn’t become a problem in the real world. But bugs ship.*

**Then check if the tool itself has a bug.** The issues are more likely to be related to how the tool processes and presents the data, rather than with pushing data itself. If there are bugs in the tool, then this will manifest itself not just for the current metric but also in other cases. Check other metrics and funnels if you can spot similar inconsistencies.

*Most businesses today rely on third-party analytics tools. It is just not worth investing in building a robust analytics framework without significant scale or for regulatory reasons. So, if the tool isn’t performing as you expect, it is worth digging deeper and consider alternatives.*

### Check for Patterns

Once data and tool accuracy are eliminated as potential causes, dive into the data to understand what’s happening.

**Check for explainable patterns.** Depending on the industry many metrics follow a pattern. Knowing this can help explain what is going on. Patterns could be related to seasonality (e-commerce purchases go up during festivals), weather conditions (the outdoor experiences market goes down during monsoons) or competition actions (competitor launches a big TV campaign).

If you can identify the pattern, you can quickly validate this by comparing historical trends and the impact of similar patterns in the data. This will save a lot of time in analysis and help reach a conclusion sooner.

### Check Your Product

The next step is to go deep into understanding if it’s your product that caused the variation.

**Check for recent changes.** Did you ship changes recently? Could that explain the change? If you introduced changes with an A/B test, compare it to the control data. Else, do a before and after comparison within a small window.

If you did make changes, it is time to dive deeper into the data.

**Check the data for explanations.** Navigating the data for explanation is like navigating a maze. You can get lost if you are not careful. There are infinite ways to look at the data. But only a handful can explain the deviation. With too many small slices the sample size starts reducing which in turn reduces the explainability of the data.

While checking the data, also look for changes in user behaviour. This is unlikely to happen overnight unless it was linked directly to a release. So, check the trends. Is there a pattern of a metric going down (or up) over time.

If you did not ship any changes, it’s time to look elsewhere in the organisation.

### Check Other Internal Factors

**Check for recent changes shipped by other teams.** Find out if any releases were pushed by other teams that might cause an issue. This is especially true if there are code dependencies or shared resources within an organisation.

**Check for business changes.** Changes in business tactics can impact metrics. For example, increased marketing spend increases the top of the funnel leading to a conversion drop. Was there a pricing change? Were there changes in the support function?

### Check for External Factors

You’ve gone through the whole process, and you still can’t explain the change. Now what? It is time to look outside.

**Check with your customers.** Talk to customers to understand if their expectations or needs have changed. Have they hit the limit of what’s achievable with your product? Do they like an alternative better?

**Check the competitive landscape.** Did a new competitor enter the industry? Was there a pricing change? Or, a massive marketing campaign?

**Check the macroeconomic and natural environment.** Once all options are exhausted, it is time to zoom right out and look at the economy and environment at large. This is more relevant today than it has ever been — COVID-19, trade wars, push for manufacturing independence, mega cyclones and earthquakes are all potential factors impacting metrics.

---

This post turned out to be longer than I expected it to be. But it is difficult to explain an analytics framework without explaining the thought process behind it. If you are interested in the short version, I have added a tl;dr version of the framework as well.
