---
layout: single
title:  "6 Things to build better B2B Web UI"
excerpt: "Here are the Top 6 things that I see most people miss..."
header:
  overlay_image: /assets/images/annie-spratt-294450-unsplash.jpg
  caption: "Photo by [Annie Spratt](https://unsplash.com/@anniespratt) on [**Unsplash**](https://unsplash.com)"
date:   2018-08-03 00:21:07 +0530
tags: b2b development tricks
categories: technology design
---


What are the top things that you should consider while designing and developing a B2B/B2E web UI? Here are the "Top Six" things that I see most people miss to consider.

## 1. Design System and Pattern library
		
First thing is a common place where designers and developers can look up to for knowledge :) 

###  So, What's a Design System ? 
Design systems are like living style guides with documentation and code being extra stuff. Design system will be the one place where code, documentation and design of each and every component will be maintained and referred by designers and developers.

Pattern libraries are similar to Design systems. Here the components are not just visual but with behaviour added. They are more like micro-level or nano-level applications. For example, you don't have to rebuild a tailored grid component or login component for every application in your enterprise. Thanks to frameworks like Angular2 & React, finally people have moved away from the notion of web pages to components.

###  What's the use of Design System ?
To address consistent visual user experience, UX Designers use style guide as hand off document to the developer. It contains the specification, mostly visual, like size, colour, font etc., of each UI element that to be used in the application. But this isn't scalable for multiple projects with more developers. Also the style guide tends get outdated since its mostly a static document. 

Design Systems serve as single source of truth for designers and developers. Having the knowledge in the tools (design system & pattern library) reduces the bus factor too. 

###  Why it is needed for B2B applications ? 
A typical employee uses at least 3-5 applications within an Enterprise. A consistent UI for these application ensures less time for the user to learn and interact with the application as he/she doesn't need to remember different interaction patterns for different applications. This will also help the Enterprise to onboard new employees in less time. Apart from the above, a consistent user interface across applications promotes maximum reusability of components across Enterprise via Design systems and pattern libraries.  

## 2. Not just Performance but Endurance  

B2B applications are used 6 to 8 hours a day so it is very important how much the frontend can endure? 

Earlier desktops were thick clients and the developers had standard procedure to fine the application to deal with endurance issues like memory leaks, performance slow down etc., . But with web applications, browsers are the runtimes to which the code needs to fine tuned to achieve improved performance and endurance. 

So it is very essential to perform endurance tests as part of Continuous Integration (CI) build at least once a week to keep track of the application's endurance capacity.

## 3. Why Browsers ? 

Browsers are the runtime environments for your web code. Coding to multiple runtimes is a pain in the neck for any developer. For B2C applications, we can't avoid serving the application on a plethora of browsers but for B2B applications you can target for a specific browser. 

I am not advocating for 'entirely' thick client desktop applications but can we look at a middle path where we can use web technologies and browser runtime to create a 'lightweight' desktop client.  
        
Electron is one such framework which lets to create desktop clients using HTML/CSS/JS and uses chrome browser to render. Electron also provides Offline mode which can be handy for applications on cruise ships or the like. 

## 4. Declutter your Desktops

A B2B user will want to do his/her job effectively. He/She knows where things are and what they do but clutter on their application screen really puts them down at a subconscious level. Minimalism is a design trait that is followed to reduce clutter on their design estate, be it a portrait, a product or even life. 
       
I see Mobile-First Design approach for a Desktop application will really ensure the design stays minimalistic in style which will eventually improve the B2B user's productivity and experience. 

## 5. Hot Keys are always hot

We are used to see the keyboard shortcuts available on our desktop applications. Keyboard shortcuts are one thing I see missing in most of the B2B web applications. When all the thick client B2B applications were migrated to browser based web applications, I see most of them ignored the keyboard shortcuts. Since B2B applications need to focus on productivity of the users who have to use them on a daily basis, it is necessary to have keyboard shortcuts in B2B applications. 

## 6. Close the Loop Feed us Back 

We almost never collect information on usage patterns of our B2B applications. Usage Analytics provide clear details on the features that are widely used and features aren't used at all. similarly which user role uses which feature extensively or rarely. This helps in improving the application post live and also in building new B2B applications across the Enterprise.
	   
Lastly, pick a web framework (like Angular, React, Vue) that fits your Enterprise and the team. Adopting to one framework (or at the most two) across Enterprise shall provide great advantage in reusing components and talents across applications. You can find a plethora of articles on the web on how to choose a framework.

Hope you found the list useful. Let me know your list of top things for a B2B UI application.