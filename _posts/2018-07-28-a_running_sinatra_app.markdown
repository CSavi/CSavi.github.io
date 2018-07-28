---
layout: post
title:      "A Running Sinatra App"
date:       2018-07-28 17:00:14 +0000
permalink:  a_running_sinatra_app
---


Creating this app was a lot more fun and engaging as I could extend my creativity with implementing new features I’ve been learning. Just like the CLI project, designing this app gave me the “big picture” on how all the moving parts work together to showcase a useful, protected, and efficient platform for which users can enjoy.

Trail-Tracker is a trail running app that allows users to log and share their running trails with other runners. I used the Corneal gem to generate the app’s structure, which made setup faster and syntax-error-proof. I just modified the MVC and tables to match the attributes I wanted for my users and trails.

**MVC** or Model-Views-Controller is a popular way to build frameworks as it provides a separation of concerns. It was energizing to see each functioning with its own tasks to produce the end product. 

**Models** are where the logic is stored. I built two models –*Users* (a has_many relationship) and *Trails* (a belongs_to relationship).

**Views** are what the user sees and where they interact with the app. It’s basically the front-end of the project that showcases artsy styling. 

**Controllers** are just as they sound –controlling the navigation.  They interact with the models and views, receiving data from the browser to the app, and from the app to the browser.  My app contains three controllers: *Application Controller* (helper functions and anything relating to homepage), *Users Controller* (securing the views /login, /setup, /logout requests), and *Trails Controller* (CRUD of the app).

The main challenge I faced during this project, was learning new error messages, but after debugging in pry while in shotgun and utilizing a few external resources, I got to learn and understand them enough to detect and resolve similar ones quickly. This project makes me excited to continue developing my portfolio and extending my knowledge how to create from various frameworks.  



