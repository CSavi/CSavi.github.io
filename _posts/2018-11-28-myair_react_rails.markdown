---
layout: post
title:      "MyAir || React+Rails"
date:       2018-11-28 15:05:54 -0500
permalink:  myair_react_rails
---


This Airbnb clone required quite the setup, but once I got going, it was difficult to pump the breaks. React immediately won my affection, but when Redux appeared, emotions began to shift. After delving into supplemental reading, I began to understand and appreciate the key benefits Redux provides:

1. ***One Store:***

Instead of multiple stores, Redux provides one store (one large JS object) with multiple properties that can get added onto that store. The store can never be mutated or changed, but can only create new versions of the store, resulting in a full history of the app’s state during every phase. 

2.	***Provider Components:***

Inherited from Redux, the Provider component’s job is to listen to the store. Since it wraps the entire application, as the store changes, it will in-turn re-render the entire application according to that change.

3.	***Smart/Container Components vs Dumb Components:***

Smart or top-level components are aware of Redux framework. They can pull properties off the store and inject them in all child components. Dumb components simply re-render whatever is passed into it. It has no knowledge of higher or abstract intelligence. These components can also dispatch actions, which can dispatch other actions.

4.	***Reducers:***

Multiple reducers modify pieces of data off the store. Because reducers do not depend on each other, they can all react off the same action. They all make their own individual changes from the triggered action, the store updates, and then the Provider component re-renders the entire application.

5.	***Extras:***

Redux is the newest and best of today due to its simplified data –one store. This results in no racing conditions. Every change produces a re-render of the application. 

After feeling much more comfortable with how Redux works with React to produce clean and efficient code, I am eager to apply these frameworks to future creations in the near future. Long live R&R.

