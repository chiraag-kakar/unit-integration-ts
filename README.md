# URL Shortener API

- Backend for URL shortener application using NodeJs, Express, Typescript and MongoDB


# Steps to run locally 

- Clone the repository

- Change the current directory to Root directory of the Repo

- Install all the dependencies by running the following command : `npm i`

- Create a `.env` file in the root directory and 
add `MONGO_URI=mongodb+srv://xxxxx:xxxx@xxxxx.xxxx.mongodb.net/xxxx?retryWrites=true&w=majority` your respective value

- Run the following command `npm run build` to build the source

- Run the following command `npm start` to start the server locally.

- Run the following command `npm run dev` to start the server using nodemon in dev environment


### In this way you can setup and run the API server locally.


# Collections required :

* Url : To store longUrl, shortUrl, UserId, clicks count 


* User : To store details of User


# API Description :

Base URL : http://localhost:1337/api
API Endpoints :


# /health

* `GET` /ping

Response :
```json
{
    "message": "pong"
}
```

# /user

* `POST` /registerUser : registering User


Payload :
```json
{
    "name":"chiraag1",
    "email":"abc1@gmail.com",
    "password":"chiraag1"
}
```

Response :
```json
{
    "user": {
        "_id": "62441d9f46057e377c06bd7d",
        "name": "chiraag1",
        "email": "abc1@gmail.com"
    }
}
```

* `POST` /loginUser : user login

Payload :
```json
{
    "email":"abc1@gmail.com",
    "password":"chiraag1"
}
```

Response :
```json
{
    "user": {
        "_id": "62441d9f46057e377c06bd7d",
        "name": "chiraag1",
        "email": "abc1@gmail.com"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYyNDQxZDlmNDYwNTdlMzc3YzA2YmQ3ZCIsImlhdCI6MTY0ODYzMTQ0MywiZXhwIjoxNjQ4NjM1MDQzfQ.eu8lFz8R0f2eUB7s095hnNCCxcfyhi2MxvwzmMe4wwI"
}
```

* `GET` /validate : validating JWT token

Authorization :

Bearer Token 
```s
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYyNDQxZDlmNDYwNTdlMzc3YzA2YmQ3ZCIsImlhdCI6MTY0ODYzMTQ0MywiZXhwIjoxNjQ4NjM1MDQzfQ.eu8lFz8R0f2eUB7s095hnNCCxcfyhi2MxvwzmMe4wwI
```


```json
{
    "message": "Token(s) validated"
}
```


# /url

* `POST` /quick_create

Payload :
```json

```

Response :
```json

```


* `POST` /create

Payload :
```json

```

Response :
```json

```


* `GET` /dashboard

Payload :
```json

```

Response :
```json

```
* `GET` /search


Response :
```json

```

* `DELETE` /delete/:urlId

Response :
```json

```

* `PUT` /redirect/:shortUrl

Payload :
```json

```

Response :
```json

```

