---
layout: post
title:      "How CORS work"
date:       2020-07-22 15:33:01 -0400
permalink:  how_cors_work
---


The fourth software engineering project requires the app to use Javascript frontend with a Rails API backend. Client/server interaction must be handled asynchronously in JSON format. The Rails backend needs to have a resource with a has-many relationship and have at least 3 AJAX calls (at least two of Create, Read, Update, and Delete).
My JS + Rails API project is a dog shelter management system that keeps a record of the resident dogs and their records. The object model relationship is a dog has many events in his/her record.The project is structured such that the front-end is decoupled from the back-end. This partition allows me to run both ends at the same time, with Rails sever running on localhost:3000 while the front-end Javascript and HTML/CSS run separately on the browser. This partition also allows both ends to be deployed together or separately.I uncommented the line gem ‘rack-cors’ to allow cross-origin resource sharing (CORS). CORS is a mechanism that allows restricted resources on a web page to be requested from another domain outside the server’s domain. It provides browsers a way to request remote URLs only when they have permission and allows servers to reject requests from unknown origins.
