---
layout: post
title:      "Adding jQuery to Rails"
date:       2018-10-01 20:18:29 +0000
permalink:  adding_jquery_to_rails
---


This project in an expansion of my Rails application –“Practice Makes Perfect” – designed to enable instructors to track their lessons and various data of their students.  I implemented jQuery to render an index and show page resource and to create and render a comment resource without a page refresh.  I was initially overwhelmed with this project, but felt pushed to my limits as I began adding some fun extra features to my application. The end result was a much gratifying experience to say the least.

I created a comment model and a comments controller to enable instructors to add comments to their created lessons.  These comments were rendered via jQuery and JSON. For the JSON requests to work, I had to configure my controllers so they would respond to the JSON requests.

A big hurdle I had for rendering the comment resource came from my turbolinks. I changed them to ‘reload’ in the layouts/application.html.erb: data-turbolinks-track’: ’reload’ in the javascript_include_tag.

For the final requirement, I translated my JSON response into Javascript Model Objects. This resulted in creating a Comment prototype object and used it to append the comment to the DOM instead of the JSON response of the created comment.

This project taught me a huge amount on how to work with Rails, AJAX, and jQuery; and how to solve specific problems by embracing the classic ‘debugger.’ Excited to continue delving into deeper layers as this project created a big-picture understanding of JS as a frontend language.

