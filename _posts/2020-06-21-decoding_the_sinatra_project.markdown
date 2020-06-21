---
layout: post
title:      "DECODING THE SINATRA PROJECT "
date:       2020-06-21 12:26:59 +0000
permalink:  decoding_the_sinatra_project
---




Hello Readers, 
Welcome back to my blog for another review on project 2 of the cohort. This time we were tasked with creating an app/website and database for tracking something important using Sinatra. The hardest part of this task was actually coming up with something that I can track publically. Since its summer time in NYC and in my area street racing is a big thing, I decided to track cars. Before I get into decoding the requirements for this project, there are some great resources that I would like to share. First if you need help with the walk thru of setting up the MVC files (the route I took) Avi’s video does a great walk thru of that. However, if you need a more comprehensive guide, on youtube, there is video by Aysan Isayo called Sinatra CRUD. I highly recommend this video as she uses a gem called CORNEAL that gives you most of the folders you need to run the app. OK lets get into it. 

The most important part of this project is understanding CRUD. In layman’s terms, this means you have to create an website/app where the user can 
Create a post/blog/etc.  
Read or see the actual post/blog/etc.  on the webpage
Update or edit the post/blog/etc.  they created
Destroy/Delete the post/blog/etc.  they created


Decoding the requirements 

1.	Build an MVC Sinatra application – As mentioned before Aysan’s or Avi’s youtube video can help you set up the folders.

2.	Use ActiveRecord with Sinatra. – ActiveRecord is a gem which you can bundle install and house in your gemfile.
3.	Use multiple models – In my models folder, I have User and Car. Here is where I specific a few things. Has Many/belongs to relationship and 
Validates that my user must have an email that cannot be duplicated and in an email form. Validates that cars created must have make model color year and that the 
Year is entered as a numerical value.

4.	Use at least one has_many relationship on a User model and one belongs_to relationship on another model – in the model folder specifies the relationship between models.
In my case. User has many cars and cars belong to user.

5.	Must have user accounts - users must be able to sign up, sign in, and sign out. – This is a 2 part creation. Your controllers where you create code that allow your user to 
Create a user name via sign up, login, logout and save them to database. 
Then there is the views folder that house your html (hypertext markup language) code for the user to actually see and carry out these tasks on the web browser.

6.	Validate uniqueness of user login attribute (username or email). – Coded in your model’s folder. This allows user to use a unique email or an email that cannot be duplicated and also
In a correct form of an email. 

7.	Once logged in, a user must have the ability to create, read, update and destroy the resource that belongs_to user. – Another 2 Folder task. Controller and Views. 

The controller, in my case Car controller, has a code that allows users to create but limiting editing and deleting to current user. 
The views allow all users to see/read a list of cars created 

8.	Ensure that users can edit and delete only their own resources - not resources created by other users. – same task as above set updating and destroy code to current users only
9.	Validate user input so bad data cannot be persisted to the database – I used a validate uniqueness code here for user input. You can use many different validation code.. I don’t have a specific source other than google certain validation codes that you would like to use. 

10.	BONUS: Display validation failures to user with error messages. (This is an optional feature, challenge yourself and give it a shot!) –  This refers to number 9 in terms of different validation codes and displaying an error when user enter wrong code. In my case I used a uniqueness validation for emails which prevents duplication of emails. It also redirect user back to login page and error message states email must be unique.


The wrap up on the project making the app presentable and readable for front end users. Here the skill is in the html for readable language and css for beautification. Tons of youtube videos on how to carry out certain design functions. I ran out of time actually trying to use css. Which at some point ill probably go back and make my app “pretty”.

Thanks for reading! Happy Coding!




