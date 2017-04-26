---
layout: post
title: A Hot Mess of Data
---

Data science is like a house party, and data scientists are the hosts.  The guests are your data: and they can trickle in, or rush in all at once, but definitely at some point you don't really know who's there.  When that party is bumpin', hosts have to make sure to not get shut down, limit noise, make sure nothing breaks, no guests get hurt, and that everyone has a good time just as planned.  If party hosting has taught me anything, it's that nothing ever goes quite as planned.

![MetisWeek2](/images/metiswk2.jpg)

**Luckily, Week 2 of Metis gave me a crash course in data science survival skills - and we had to throw our own data party.  Here I'll outline some challenges from week 2, and my takeaways.**

### 1. When you invite all your friends, and no one shows up.
Before getting started on our first passion project, [Project Luther](), we had to narrow the scope of our questions.  All we knew was that it had to involve predictive regression (on quantitative or qualitative data).  My topic?  Craft beer.

Inspired by [Partially Derivative](http://partiallyderivative.com/podcast/2017/03/21/robot-bartender-overlords) and [Charlie Bamforth](http://faculty.bftv.ucdavis.edu/fst/Bamforth/underg.html) of the Brewing Program at UC Davis (and my own insatiable curiosity), I probed the web looking for as many variables (aka features) as I could find on craft beer brands.  With the features I found on CraftCans.com and BeerAdvocate.com, I decided my question would revolve around whether or not I could predict the community ratings on Beer Advocate.com, given features like (ABV, size of the can, bitterness, etc).

In order to do this, I learned how to leverage Python packages like BeautifulSoup and Selenium in order to iterate over all the website links I had to scrape and take the features of interest.  We explored strategies and tactics to navigate the robot defenses, while also being mindful of 'terms of use.'  In the end, I had a local cache of 80+ HTML files to wrangle, munge, and play with.

### 2. When you expect your friends, and get a bunch of randos. 
Cleaning and tidying up data for use in regression is a hot mess.  You get multiple variables in a single column, text strings mixed up with numerical data, and features that encompass more than one 'observational unit.'  in a paper titled [Tidy data](http://vita.had.co.nz/papers/tidy-data.pdf) by Hadley Wickham, he lays out a framework for cleaning data.  I did my best to follow such rules, but in the interest of time I didn't clean my whole dataset - I still had other things to do!

Without packages like Pandas, or using Regular Expressions, it would be such a buzzkill to do it all by hand.  The trick is being able to clean your 'dirtiest' scrape, and conditioning all future scrapes off the dirtiest instance.  Easily, this is where the majority of my time was spent - just getting everything in order.  Without helper functions to automate the process, this data party would be beyond my control.

### 3. Damage Control! Limit noise and make sure nothing breaks.
Here's where things get a bit more interesting.  In modeling predictive algorithms for beer ratings, it's useful to know what features would be good predictors of such ratings.  

It's also useful to know what features might be interacting with each other.  Ideally, we'd want all features to be independent variables (whereas interacting features may result from confounding variables).  For example, If ABV and bitterness were related, then we may want to only use one in the model, or creatively math them together into one feature (since they interact anyway).  Ideas like this keep the model predictive and adjust the data based on our modeling approach.

Along the way, I was using packages like Matplotlib and Seaborn to visualize the shape and spread of my features and ratings, while using Statsmodels in order to narrow in on P-values for each feature.

--------------------------------------

![TypicalDay](/images/typicalday.jpg)

### As for the rest of Week 2...
While all of this was going down, Week 2 was also the beginning of professional development activities.  My careers mentor was helpful in giving me resume and job search advice, while plugging me into the right networks here in San Francisco.

This whole thing is super immersive, with high expectations on performance and effort.  My success here isn't measured in grades or a diploma, but rather in how well I'm understanding the material, and whether or not I'll be ready to apply and share this new knowledge with my team, and the world.

### The Pi-Shaped Individual

![PiShapedIndividual](/images/pishapedindividual.jpg)

At the same time, I'm more than a data scientist.  The above graphic shows what I hope to be my repertoire of skills by Age 27.  Although I came into this program to expand on data science as a 'specialty,' this is only one phase in my larger pursuit to use my skills to serve humanity.  But we'll see where this goes!  Though I have a roadmap of skills, my careers roadmap is still a blank canvas.

**Sometime next week, I'll recap week 3, my finished project and presentation, my initial attempts at regression, and thoughts on Decision trees (CARTs), Ensembles, and other models.**