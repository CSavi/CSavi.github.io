---
layout: post
title:      "Practice_Made_Perfect -Rails"
date:       2018-08-24 14:19:47 +0000
permalink:  practice_made_perfect_-rails
---


My Rails project was inspired by an idea I had a few years back to find an app to organize a music studio’s instructors and students. I built this app with the intention of it developing into a management tool designed for music studios to maintain records of their instructors and their lesson planning lesson prep hours, but also for instructors to maintain their weekly assignments they submit to management and a way to create lessons and oversee their students’ practice hours and progress.

For this first phase of the app, I created a lessons join table between instructors and students with user submittable attributes –lesson_datetime and lesson_description –as lesson belongs to both models. I then created my routes, including shallow routes for the child, assignments and for it’s parent, instructor. This enabled me to capture this relationship in my routing. 

I then was able to add presence, numericality, and uniqueness validations to most of my models, ensuring only valid data is saved to my database. Partials made the views cleaner and easier to maintain, but it took me a bit to understand how to best write clean syntax for partials. This project gave me great practice for that.

The biggest hurdle was getting ahead and spending time on the views with missing functionality. Building this app taught me to get a solid framework working before adding extra features as that created unnecessary time and issues to debug. Rails is quite different from Sinatra in easier and harder ways, but it was fun to see the difference between the two and to understand better when to utilize one over the other for a particular project. 

