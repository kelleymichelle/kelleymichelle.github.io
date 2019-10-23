---
layout: post
title:      "Committing a Potential Disaster to Github"
date:       2019-10-23 09:48:39 -0400
permalink:  committing_a_potential_disaster_to_github
---


Rails projects! We got through Sinatra and I felt like I was grasping web development somewhat. Introducing the MAGIC OF RAILS. Guaranteed to make you want to smash your computer and toss it through a window. Might make you want to consider a different profession. Going through the curriculum provided was torturous. Flatiron introduced the thumbs up/ thumbs down feature to rate lessons and labs about halfway through Rails and I was like YES LET ME TELL YOU HOW AWFUL THIS IS. Oftentimes there would be a relevant lesson that was followed by a lab. You get through the lesson or codealong and you're like "ok I think I get it, not so bad". Then the Rails train hits you with the following lab. I felt like I was never going to grasp this. 

So I started my Rails project 2 weeks ago. I decided on an idea similar to Kickstarter. You sign up for an Account and choose whether you are an 'Inventor' or an 'investor'. An inventor can create ideas and comment or collaborate on other ideas. Investors can views ideas and I want them to be able to save an idea so they can "fund it". It's still a work in progress. 

My idea for the signup was that an inventor and investor were restricted to doing and accessing different things on the site. I tossed around the idea of needing 2 seperate sign ups and types of users or having an attribute in my user that would be able to restrict them. Then I was told about polymorphic relationships. 

I have an Account, Inventor and Investor tables. My Account table has an attribute of "Accountable". My Inventor and Investor tables each have an attribute of "Account". Then I set up the associations so ActiveRecord would know that this was polymorphic and each account would be assigned an "Accountable" and consequently each "Accountable" would have an associated "Account". 

Figuring out the signup was interesting. In my create method, it wouldn't let me create an Account if the Accountable didnt exist. So I had to create the Inventor or Investor and save it to the account. After saving it would immediately redirect the Account to the Accountable page where they put in the Accountable information and then it updates that information. From there I created helper methods which would determine if my current user was an inventor or investor and restrict their access to the site appropriately. Rails definitely taught me how to make helper methods on top of helper methods on top of helper methods. 

I definitely learned more about Rails doing this project than I did going through the curriculum. The benefit was that it showed you generally what you needed to do and you 100% learned where to look in documentation for things. 

I got way better at CSS! I started using flexbox and grid combined. I used a grid inside of a flexbox on top of a flexbox with a few more flexboxes thrown in for good measure. I used a much more minimalist design which I love. 

The realization that I can now create a fully functional website from scratch is pretty incredible. In 5 months I learned this huge thing. I think that is pretty cool. 


