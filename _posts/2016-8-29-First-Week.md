---
layout: post
title: First Week
---

This week we went through a soft introduction to c++ by comparing a simple program line by line with the java equivalent commands. We also learned about our testing and test coverage tools through projected demos. Right now I'm mostly running into trouble with installing docker on a windows machine and am waiting on my textbook to arrive so that I can begin the readings. Next week I will catch up for lost time with the readings and finish setting up the environments required for this course as well as getting started on the first project.

On Friday Professor Downing gave us a quick introduction to unit testing with google test, but there is another type of framework that I like to use to make unit testing much more powerful.


<b>Why I like mocking :</b>
At their summer internships UT students are often asked to unit test their code, while integration testing is often left out. The point of unit testing is to isolate whether a single function is performing properly, in contrast to integration testing, which focuses on multiple functions interacting properly. 

<u>Now imagine you're a UT student who is working on a project with the following files :</u>
	

 - Main.Java
	 - function printDocuments : Uses a DataAccessInterface object to find all of the documents in the database
 - DataAccessInterface.java
	 - function findAllDocuments : unimplemented since it is part of the interface, but should return JSON
 - SqlAccess.java (implements DataAccessInterface)
	 - function findAllDocuments : actually implemented for a sql database and returns JSON
 - NoSqlAccess.java (implements DataAccessInterface)
	 - function findAllDocuments : actually implemented for a nosql database and returns JSON
	
	From my knowledge, any attempt to unit test the printDocuments function in Main.java without a mocking framework would have two options :
	
	1. Actually run the SqlAccess or NoSqlAccess version of findAllDocuments() and hope that whichever implementation you used is functioning correctly. This option violates the idea of unit testing however, as the test could fail due to issues with SqlAccess.findAllDocuments() even if Main.printDocuments() does everything it is supposed to do
	
	2. The other option is to create a third class, TestAccess.java which implements DataAccessInterface and stubs out function calls like findAllDocuments() with dummy data. This removes the dependency on other functions, but clutters the source code and requires a new class file to be made if you want to test how Main.printDocuments() responds if DataAccessInterface.findAllDocuments() throws an exception or gives a different data set than TestAccess returns.
	
	Mocking frameworks are most similar to the second approach in that they allow the programmers to decide what DataAccessInterface.findAllDocuments() returns without relying on a specific functioning implementation, but differ in that you don't have to create a unique class file for each behavior of TestAccess.findAllDocuments(). Rather, within your test file you can create mock objects alongside the test code and have them dynamically return dummy data or throw exceptions as needed for each test. In addition, many mocking frameworks introduce the idea of a Spy, which allows the test to verify that certain functions on the mocked object were called the correct number of times with the correct parameters.

**Which mocking framework is best for our projects :**
	Googletest already includes a mocking framework, googlemock, which should be more than enough for the course. 