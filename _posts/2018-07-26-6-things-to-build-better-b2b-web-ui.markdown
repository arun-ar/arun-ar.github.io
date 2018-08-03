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


What are the top things that you should consider while designing and developing a B2B/B2E web UI? Here are the top 6 things that I see most people miss to consider.

## 1. Keep the knowledge in the systems
		
First thing is to build a Design System and Pattern Library.  

###  So, What's a Design System ? 
Design systems are like living Style Guides with documentation and code as extra. Design systems will be the one place where each and every UI component will be maintained and referred to by designers and developers.

Pattern libraries are similar to Design systems. Here the components are not just visual but behaviour too. Each Component is more like a little application - at molecular scale. For example, a Grid or a Login component. With pattern libraries, you don't have to rebuild a custom grid component or login component for every application in your enterprise. 

Thanks to frameworks like Angular2 & React, finally pattern libraries are easy to setup as we have moved away from the notion of building web pages to building components.

###  What's the use of Design System ?
UX Designers usually use a [Front-end Style Guide](http://bradfrost.com/blog/post/style-guides/) as hand off document to the developer. Its a static document containing the specifications of UI elements, mostly visual. But this document can become ineffective when there are multiple projects with many developers and designers as there will be no single source of truth. And Style Guide gets outdated cause of its static nature. 

Design Systems serve as a single source of truth for both designers and developers. Having the knowledge in the systems (design system & pattern library) reduces the [bus factor](https://en.wikipedia.org/wiki/Bus_factor) too. 

###  Why is it essential for a B2B application ? 
Typically, an Employee uses at least 3-5 applications within an Enterprise on a daily basis. A similar user interface across those 3-5 applications will help in higher productivity and less onboard time for a new employee. 

So B2B applications should build and leverage Design Systems/Pattern Libraries to ensure consistent user interface.

## 2. Make them Endure

B2B applications are normally used for 6 to 8 hours a day so it is very important to continuously test their endurance. Earlier desktops were thick clients and the developers had standard ways to fine tune their applications to deal with endurance issues like memory leaks, performance slow down, etc.,. But with web applications, browsers being the runtime, coding to many browsers has become much more complicated. 

So it is very essential to perform endurance tests on all targeted browsers as part of continuous integration (CI) builds at regular intervals (may be for every sprint) to keep track of the application's endurance capacity.

## 3. Get out of Browsers 

Browsers are the runtime environments for your web code. Coding to multiple runtimes is always a pain in the neck. For B2C applications, we can't avoid serving the application on a plethora of browsers but for B2B applications you don't need to do target every other browser. You can restrict the users to use only browser runtime by packaging your web application into a desktop application.
      
You can wrap your SPA web application using [Electron](https://electronjs.org/) framework to create desktop applications. Electron uses Chromium and Node.js (which will be part of your distributable desktop client) to render. Electron also enables offline feature which can come in handy for applications on cruise ships or similar. 

## 4. Declutter your Desktops

A B2B user would want to do his/her job effectively. They know where things are and what they need to do.  But too much clutter on their application screen might really put them down at a subconscious level owing to less productivity and bad user experience. 

[Minimalism](https://www.sitepoint.com/what-is-minimalism/) is a design style wherein clutter on their design estate (be it a portrait, a product or even life) is kept none or minimal. I see sticking to a [Mobile-First-Design](https://www.uxpin.com/studio/blog/a-hands-on-guide-to-mobile-first-design/) approach for a Desktop application will ensure the design stays minimalistic (avoiding much visual clutter).

## 5. Keep the keys 'Hot'

We are used to keyboard shortcuts on our desktop applications. But those shortcuts are the one thing that I see missing in most of the B2B web applications. When the thick client B2B applications were transformed to web applications, most of the developers ignored the keyboard shortcuts feature making the application less efficient. 

Since B2B applications need to focus on user productivity, it is necessary to have keyboard shortcuts in them. 

## 6. Close the Loop  

Once a B2B application goes live, we almost never collect usage analytics. Usage Analytics provide clear details on the features that are widely used and that aren't. Also which role-user uses which feature extensively or rarely. 

So it is always a good practice to configure analytics or conduct a survey to get feedback from the users. These feedback can help you in improving the current system and in avoiding those mistakes in your future systems.  
	   
## Last One 
Lastly, pick a web framework (like Angular, React, Vue.js) that fits your Enterprise and the team. Adopting to one framework (or at the most two) across Enterprise shall provide great advantage in reusing components and talents across applications. You can find many articles on the web on how to choose a framework.


Hope you found the list useful. What will be your top 6 ? or Is there something I missed ? Let me know in the comments section. 