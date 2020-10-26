---
layout: post
title:      "JavaScript with Rails Project "
date:       2020-10-26 02:50:52 +0000
permalink:  javascript_with_rails_project
---


   This project focused on building an app with rails using API and Javascript, while still implementing previous lesson such CRUD and relationships. 
	 
	 I made a simple app that loads posts and comments for travel blog. Very simple using REST API, CREATE and DELETE METHODS.


##Rest vs CRUD 

      REST = REpresentational State Transfer. This describes resources or for this project (URLs). REST is responsible performing actions in the applications. 
			With JavaScript it can send a  requests to the server and load new information without reloading the page. With this application we can load user information and receive updates from the server. During this application we can use the fetch() method which can be used with many type of requests such as POST, GET, PUT and DELETE. In my application I used GET and Fetch to load post and comments. 
			
			Example:
			
			
    fetchAndLoadPosts() {
        this.adapter
            .getPosts()
            .then(posts => {
                posts.forEach(post => this.posts.push(new Post(post)));
            })
            .then(() => {
                this.render();
            })
    }
			
			*** This is a snippet from my frontend code requesting to fetch and load post from my backend.  As you can see its using the GET method to request posts from the server.  The push new post and load/display.
			
			CRUD = Create Read Update Delete. Which describe the actions that a user can actually perform while using the application .
			
			During the planning phase I knew I wanted my users to be able to create posts and comments with the ability to delete as well. 
			
			createPost(e) {
        e.preventDefault();
        // console.log('post is being created')
        const value = this.newPostBody.value


        this.adapter.createPost(value).then(post => {
            this.posts.push(new Post(post))
            this.newPostBody.value = ''
            this.render()
        })
    }
		
		Here is an snippet of my "create post" code. Here you see the user has the ability to create a post (which is in the form of a BODY not a string).  Also notice the preventDefault() method cancels the event meaning that the default action that belongs to the event will not occur.
			
