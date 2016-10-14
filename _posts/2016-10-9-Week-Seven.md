---
layout: post
title: Week Seven
---
**1. What did I do last week?** 
<br>
This week brought along with it the first test, so most of the class time was spent solidifying our knowledge of the newer subjects such as creating iteratable object in c++ and learning to identify the nuances of using const in our type declarations. As I mentioned last week, my laptop had been having issues with maintaining an internet connection, but thankfully Professor Downing allowed me to attend the makeup exam  where I used a lab machine to take the test. With the logistical chalenges taken care of, I was free to start studying for the exam. My approach to studying for the exam is below in enumerated steps :
<br>
1. Quiz myself using the class quizzes on canvas
<br>
2. Read through my personal class notes
<br>
3. Review each canvas quiz that gave me trouble the first time
<br>
4. Read through the posted class notes on piazza
<br>
5. Review each canvas quiz again
<br>
6. Read through all non-project specific piazza posts
<br>
7. Read all of the posted example c++ files covered in class
<br>
8. Review each canvas quiz
<br>
9. Skim through the posted class notes on piazza
<br>
10. Skim through my personal class notes
<br>
11. Review any posted cheat sheets
<br>
12. Create my own cheet sheet or utilize a quality posted cheat sheet as a base and modify it as needed


**2. What was in my way?** 
<br>
After coordinating a time to take the makeup exam, my biggest challenge was just learning the material. I hadn't used c++ very often before this course and the exam entailed writing c++ without a compiler, so I focused on reviewing example after example after example of c++ code, worked through several practice problems that dealt with language features that I found non-intuitive, and repeatedly read through each of the functions we built in class in order to analyze the c++ way to solve problems. In fact, since we were allowed to bring in a note sheet to the exam with the class interfaces, I was able to simply focus on learning the language rather than memorizing the smaller details like the difference between a prefix and a postfix operator definition on a user defined class.


**3. What will I do next week?** 
<br>
I have a very challenging exam for my parallel algorithms course this week and the first half of a project due for that same course the following monday, so I will most likely dedicate the majority of the week to preparing for that exam. However, the next project is due in two weeks so I will also need to find a partner for the project and start coordinating programming sessions so that we could get an early start on the project.


**Tip of the week :** 
<br>
I've recently started seeing randomized algorithms in other courses that utilize the expected value of an algorithm rather than the deterministic value in order to solve problems much quicker with suprisingly high accuracy approximations. For example, if you remember 3-SAT from CS331, you'll remember that the problem involves finding the variable assignments that solve all of the clauses of form (x1 or x2 or !x3) and that the problem is np-complete. Although solving the problem deterministically can't be completed in polynomial time, a probabilistic algorithm that simply randomly assigns a true or false value to each variable  on O(n) time will satisfy each clause with probability 7/8. This is easy to prove if you simply consider the fact that each clause has 3 variables that can hold one of two values, so there are 2^3=8 possible combinations of values that can go into each clause. Since the variables are all "or-ed" together it would only take one of the variables being true for the clause to be satisfied. Therefore, since the only combination of values that does not include at least one true variable is (0 or 0 or 0) and there are 8 possible combinations, the remaining 7/8 variable assignments will evaluate to true. Since each variable is randomly assigned, the probability to assigning values that satisfy the clause is 7/8 and the expected value of this approximation is (7/8)*Optimal even though it is exponentially faster than any known method to deterministically solve the problem.