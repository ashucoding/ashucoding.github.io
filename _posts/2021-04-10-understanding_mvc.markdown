---
layout: post
title:      "Understanding MVC"
date:       2021-04-10 16:13:02 +0000
permalink:  understanding_mvc
---

The best analogy used.

"In a restaurant kitchen we have three key components:

A chef that makes the food

A waiter that takes the order and brings out the food

A table where the food is served to the customer

Using this as an analogy, we can assign the following roles to each of our restaurant components:

Model - The model is the chef, it should manage the critical aspects of the application. One of my favorite tasks in a Rails application is working with the model files. This is where you can be very expressive with the custom algorithms that you want to utilize and you also have direct access to the specific database record. The logic of your application should mainly reside in the model files.

Controller - The controller is the waiter. In the same way that the waiter takes the order from the customer to the chef and then brings the food to the table, the controller transmits data requests from the user to the model, and then delivers data that is rendered in the view to the user.

View - The view is the table. A table shouldn't do anything besides sit there and hold the food when it is delivered. In like manner the views should not contain any programming logic, they should simply render what the controller sends it. One of the top issues I discover when I review a Rails application that has a large number of bugs is that the developer integrated too much logic directly into the view." 

"To extend the restaurant analogy, the chef (your model) performs a number of tasks to create each meal that the waiter (controller) and especially the table (views) don't know anything about. Some of this domain logic would include items such as complex database queries, data relationships, and custom algorithms."
