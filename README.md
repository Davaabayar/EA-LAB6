#Lab 6 - Java Persistence Query Language (JPQL) Exercise JPQL.1 
*The Setup:* 
In this exercise you will write several JPQL queries against a given data set. Start this exercise by downloading the provided Lab6-JPQL project from Sakai, and adding the Hibernate, MySQL and log4j dependencies to it. 
The Application: The provided application uses the following flight scheduling problem domain.
 
Currently the application simply retrieves and prints all the flight info stored in the database. Running the application should produce output that contains something like:
 
*The Exercise*
Look through the application code, and once you feel comfortable with what it does update the JPQL queries in Application.java to retrieve the following data:
a)	All flights leaving the USA with a capacity > 500
b)	All airlines that use A380 (model) airplanes
c)	All fights using 747 planes that don’t belong to ‘Star Alliance’
d)	All flights leaving before 12pm on 08/07/2009

