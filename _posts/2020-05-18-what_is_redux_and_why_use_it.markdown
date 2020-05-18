---
layout: post
title:      "What is Redux and Why Use it"
date:       2020-05-18 13:54:18 -0400
permalink:  what_is_redux_and_why_use_it
---

In simple terms Redux is a state management tool. Redux provides all of our components with access to the global store and takes the ability to make changes to state away from our components creating a more predictable method to manipulate state. 

Redux might seem like a chore to learn because React components can manage their own state and pass props to children components. While this is true, In larger applications with hundreds of components managing state can become difficult. Trying to decide where state should live in a large application is confusing and can lead to unreadable code. 

With Redux we do not have to concern ourselves with where state should live. We simply have a global store and pass what parts of that store we need to the components that need it by using methods like mapStateToProps. This allows us to write clean concise code that is easy to understand. 

So how does Redux work? The way Redux works can seem confusing at first but is fairly simple once you understand some core concepts. There are three key parts to Redux store, actions, and reducers. 

The store holds the entire state for the application. Each individual component can access the store without having to make use of props. This allows us to take only the data from the store that we need and pass it only to the components that need it. 

Actions are simply POJOs (plain old JavaScript objects). Actions contain a type property that is used to indicate the type of action and a payload that contains the data that should be used to perform the action. These actions are created via an action creater. An action creater is a function that returns an action. 

Reducers are pure functions, functions that when given the same data will always produce the same results. This means they are predictable and controlled. Reducers take the current state of the application and make changes to it based on the action provided. 

Redux is intimidating at first glance but once you understand the individual pieces you can start to appreciate such a useful tool. 
