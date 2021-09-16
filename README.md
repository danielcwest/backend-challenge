# Bigeye backend code challenge

Prerequisites
-------------
You will need to have git and Java 8 installed.  Note that this code will only run on Java 8 specifically.

Background
----------

The purpose of this challenge is to demostrate one's ability to code up a REST API.  The
Server can be started with the command `./gradlew run`.  Feel free to test out the server to make
sure it works and think about how you might want to solve the questions below, but please don't 
start coding up a solution before the scheduled interview time.

Note that we are using Hibernate as an ORM for this scaffold.  If you prefer a different ORM library,
feel free to add that to the build.gradle and wire it up before the interview.

Tables
------

There are two tables with records existing in the database: 
```
PERSON
FIELD  	  TYPE  	    NULL  KEY  	DEFAULT  
ID	      INTEGER(10)	NO	  PRI	(NEXT VALUE FOR "PUBLIC"."SYSTEM_SEQUENCE_CADDDCD7_06E0_4242_A535_6F0B08CACCA4")
FULL_NAME VARCHAR(255)	NO	  NULL
JOB_TITLE VARCHAR(255)	NO	  NULL

LOGIN
FIELD    	TYPE  	      NULL  	KEY  	DEFAULT  
ID	        INTEGER(10)	  NO	    PRI	    (NEXT VALUE FOR "PUBLIC"."SYSTEM_SEQUENCE_833A9C8E_D25D_4BFE_B2AE_6375B409DA6D")
PERSON_ID	INTEGER(10)	  NO		NULL
LOGIN_TIME	DATETIME      NO		NULL
```

the Logins table tracks all of the logins for the people in `person`

Existing endpoints
------------------

The following curl commands should return valid results:

`curl localhost:8000/health`

`curl localhost:8000/people/2`

Tasks
-----
1. We already have code for the person retrieve function, implement the other CRUD functions for Person
2. Implement a function to retrieve all logins for a given person
3. Implement the CRUD functions for Logins
4. Testing (if we have time)

Things we are looking for
-------------------------

1. Ability to understand/constrain the problem
2. Well organized clean code
3. Thoughtful REST endpoints
4. Ability to isolate and debug problems as they arise
5. Familiarity with Java and comfort working within an existing repo
6. Familiarity and comfort writing tests



