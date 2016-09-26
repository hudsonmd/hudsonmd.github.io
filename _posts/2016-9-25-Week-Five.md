---
layout: post
title: Week Five
---
**1. What did I do last week?** 
<br>
My group spent the majority of the week trying to piece together a working boost cache from piazza posts and then redesigning our program to allow the mocking of data we were collecting from our boost caches. Based on the last two projects I can confidently say that programming the solution to these projects takes a tiny fraction of the time compared to setting up input/output and monitoring piazza for updated project requirements. An unrelated but extremely interesting lecture accompanied these efforts on Wednesday, as a guest from JPL gave the class real world insight into the role of software engineers in space exploration. This speaker not only described the rituals that his team found effective when woorking through their projects, but also demoed software that was actively being developed for virtually mapping mars through the microsoft hololens.

**2. What was in my way?** 
<br>
My group used binary cache files for the project and found it extremely difficult to redesign our project to mock out these cache file inputs. We at first attempted to utilize google mock, but found that although its parent project google test was included in the docker image google mock had not been installed. Then, after hours of trying to construct an istringstream out of binary data, we pivoted and implemented our mocking through an object oriented approach that relied upon interfaces.

**3. What will I do next week?** 
<br>
I'm going to focus on reviewing my notes and preparing for next week's test. It seems as though this week is going to be my calm before the storm so I'll likely try to get a head start on next week's reading as well. 

**Pick of the week :** 
<br>
There's a completely free online database called firebase(https://www.firebase.com/) that is perfect for proof of concept projects. I do a lot of my personal development in AngularJs and have found a module called AngularFire that makes interacting with firebase trivially easy and has allowed me to rapidly prototype by writing web services that utilize firebase rather than needing to create a full server for database interaction at the beginning of the project.