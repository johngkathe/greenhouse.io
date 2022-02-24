# greenhouse.io

# About the Project

## About this Repository
This is a PaaS deployment of my greenhouse measurements software containing only the pertinent software components allowing it to function on the cloud.  Unlike the base version, it cannot access a local database, only a remote database hosted by MongoDB Atlas.

## URL
https://greenhouse-io.herokuapp.com/

*Note: The front end of this application is currently in development.  The contents of index.js are shown as a placeholder.*

## Why I made this application
This application serves as a simulation for making a software solution for a client because my dad is in the process of building a hydroponics greenhouse and would like software to assist him in collecting and aggregating for optimizing crop growth strategies and machine automization.  As is, the current implementation could be more readily handled in an Excel spreadsheet.

## Basic Functionality 
The bulk of greenhouse.io's current implementation revolves around the models and routes associated with the greenhouse data (given the lack of a front end, there can be no *true* MVC implementation in this application presently).  Via the Postman API or one MongoDB's database modification tools, CRUD operations can be performed.  No CLI operability was created since it would be impractical for the end-user and since a GUI is the next step forward in the development of this project.

## Language(s) Used
JavaScript - Has extreme flexibility for making web APIs and local applications too thanks to Node.js.  With all the frameworks available and my familiarity in the language this was the obvious choice.

## Frameworks Used
MongoDB - I chose this noSQL database to handle the storage of my greenhouse data.  I would rather work with JSONs than with SQL queries.

Express.js - The default framework for making REST AP s/CRUD operations... an essential element of any MEAN/MERN application.

Node.js - Another default.

## Data Management
Postman API - I used the Postman API to test each CRUD operation for robust functionality.  Currently that is the gateway in which I operate on all of my dummy data.

## Security
Password hashing is handled with the argon2 library using argon2's argon2id for robust protection against GPU cracking *and* side channel attacks... which is overkill in this context, but looking for a good password hashing library took longer than actually implementing this library in my code.

Tokenization is handled with  jwt.io's jsonwebtoken library.

