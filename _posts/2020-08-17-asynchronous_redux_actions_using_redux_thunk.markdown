---
layout: post
title:      "Asynchronous Redux Actions Using Redux Thunk"
date:       2020-08-17 19:11:42 -0400
permalink:  asynchronous_redux_actions_using_redux_thunk
---

By default actions in Redux are dispatched synchronously, which is a problem for any non-trivial app that needs to communicate with an external API or perform side effects. Thankfully though, Redux allows for middleware that sits between an action being dispatched and the action reaching the reducers.
Redux Thunk is a middleware that lets you call action creators that return a function instead of an action object. That function receives the store’s dispatch method, which is then used to dispatch regular synchronous actions inside the body of the function once the asynchronous operations have completed.
The most common use-case for Redux Thunk is for communicating asynchronously with an external API to retrieve or save data. Redux Thunk makes it easy to dispatch actions that follow the lifecycle of a request to an external API.
For instance, given the common example of a todo app, creating a new todo item normally involves first dispatching an action to indicate that a todo item creation as started, then, if the todo item is successfully created and returned by the external server, dispatching another action with the new todo item. In the case where there’s an error and the todo fails to be saved on the server, an action with the error can be dispatched instead.
