# Parmpara Project

## What is done:-
 - signUp - password hashing, creating token for authorization
 - login - password decrypt, authorization
 - creating post - user and create, view, delete and update posts on the base of their role
 - question and answer - this is like a meraki app, user can create a course and subexercise of that course if the user have access
 

## Basic Mysql implementation with knex
Create three tables 1. user registration, 2. user posts and 3. Question answer and for each table I have to write four routs(get, post, put and delete)

# MVC
## Model (Queries, Model is known as interface of db)
- connection (db connection using knex and creating tables)
  - database.js - database connection which is "user_details" 
  - user_registration_table.js - creating user registration table
  - user_posts_table.js - creating user posts table
  - q_and_a.js - creating question and answer table(que_ans)

queries - (all about query) 
- user_registration.js - all the queries for user registration table
- user_posts.js - all the queries for the user posts table
- q_and_a.js - all the queries for question answers table

## V(View)
- nothing

## Controller (Logic, only routes are there since the project is not about logic test)
- routes - this folder is for all the routs
  - user_registration.js - all the routs of user_registration queries
  - user_posts.js - all the routs of user_posts queries
  - q_and_a.js - routs of q_and_a.js queries

## How to run-
  - server.js - this is my main file, have added script in the package.json file so to run the server with nodemon type "npm run server".

  - nodemon - nodemon is a tool that helps develop node.js based applications by automatically restarting the node application when file changes in the directory are detected.

**Inputs** 
 1. User registration
    - Name, email, password
 2. user post
    - Date, imgurl, captionforimg
 3. Question and answers
    - question_id, question, answer  


#### Dependencies
 - nodemon - to restart the server automatically everytime I change anything in the code, so that after changing something in the code we don't have to close and re-start/run the server


#### What is:- 
### route
 route is basically a path in http methods (get, post, put, delete, etc)
  - syntax - get(rout, callback)/ get('/user', function(req, res){})
### res.send()
 This function takes an object as input and it sends this to the requesting client. Here we are sending the string "Hello World!".
### app.listen(port, [host], [backlog], [callback]])
 only port parameter is required here
### app.all()
 this method is generally used for defining middleware
### regex
 regex to restrict URL parameter matching.
 - example - app.get('/things/:id([0-9]{5})', callback)

## Middleware 
middleware as functions that execute after the server receives the request and before the controller action sends the response. The biggest thing is that middleware functions have access to the response (res) and request (req) variables and can modify them or use them as needed. Middleware functions also have a third parameter which is a next function. This function is important since it must be called from a middleware for the next middleware to be executed. If this function is not called then none of the other middleware including the controller action will be called.

blog - https://blog.webdevsimplified.com/2019-12/express-middleware-in-depth/

## REST/RESTfull API
REST is a standard of creating API

video - https://www.youtube.com/watch?v=lY6icfhap2o

# Extra
- postman console short-cut - CMD/CTRL + ALT + C
- 
