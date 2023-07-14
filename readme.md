# jwt-json-server

This project adds jwt authentication to json-server

## Installation

npm install

to install the dependencies.

## Specify SECRET_KEY for encryption
Create a file 

.env

To hold the externalised resources

Add an entry to .env

SECRET_KEY=SomeSecretValueOfYourOwnChoosing


## Start The Server
Run the project using

npm run start

or

npx nodemon server.js


## Register a user

Generate a POST request to

http://localhost/auth/register

body:

{
    "email": "somebody@email.com", 
    "password": "LetMeIn"
}

## Login

Generate a POST request to

http://localhost/auth/login

body:

{
    "email": "somebody@email.com", 
    "password": "LetMeIn"
}

You will receive back a token:

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InNvbWVib2R5QGVtYWlsLmNvbSIsImlkIjoxLCJpYXQiOjE2ODkzMzE0NzUsImV4cCI6MTY4OTMzNTA3NX0.iNuVzmu7_AWZK4uhNuHKb3goWGAaeXXX0ojhBRHPbvY

Make an Authenticated Request

GET

http://localhost/records

Auth
Bearer

And supply the token


## database.json

The server will serve whatever records are in database.json treating this file as any other
json-server json file.




