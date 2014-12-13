# Node Sample Web Application for AT&T Enhanced WebRTC JS SDK

A node application with the following functionality:
  * Provide user management for the sample application
  * Provide OAuth endpoint for Mobile Number authorize and callback
  * Provide login and logout functionality for Virtual Number and Account ID users

## System requirements

* Chrome for OSX (v39)

## Contents of this Package

This package contains the software necessary to run a sample application to be used together with
a NodeJS DHS.

- `/package.json` - Configuration options
- `/app.js` - Main NodeJS program

## Configuring the DHS

The configuration is located in the file: `/package.json`

```javascript
...
"dhs_https_host": "localhost",
"dhs_https_port" : 10011,

"sample_http_port": 9000,
"sample_https_port": 9001,
...
```

## Running the DHS

1. Install NodeJS dependencies: `$ npm install`
2. Execute the NPM `start` script `$ npm start`.
**NOTE**: The `start` script will use the Production environment by default.

## Loading the Web Application

1. Open your Chrome Browser
2. Load the URL: https://localhost:9001 to load the application.

# RESTful API

## Register User

Registers a new user for the sample application.

```
POST /users
```

### Parameters

``` javascript
{
  "user_id": "user_id",
  "user_name": "user_name",
  "password": "password",
  "user_type": "user_type"
}
```

### Response

**Virtual Number users**

``` javascript
{
  "user_id": "user_id",
  "user_name": "user_name",
  "user_type": "user_type",
  "virtual_number": "virtual_number"
}
```

**Account ID users**

``` javascript
{
  "user_id": "user_id",
  "user_name": "user_name",
  "user_type": "user_type",
  "account_id": "account_id"
}
```


## Delete User

Deletes an existing user from the sample application.

```
DELETE /users/:id
```

### Parameters
None

### Response
HTTP 201 Success. Deleted user: user_id


## Login
```
POST /login
```

### Parameters

```Javascript
{
  "user_id": "user_id",
  "password": "password"
}
```

### Response

``` javascript
{
  "user_id": "user_id",
  "user_name": "user_name",
  "user_type": "user_type",
  "role_type": "role_type"
}
```

## Logout
```
DELETE /logout
```

### Parameters
None

### Response

``` javascript
{
  message: 'User logged out successfully'
}
```

## Authorize

Endpoint for authorizing Mobile Number users using AT&T's OAuth.


```
GET /oauth/authorize
```

### Parameters
None

### Response
`HTTP 302`


## Authorize Callback

Endpoint for oauth authorize callback.

```
GET /oauth/callback
```

### Parameters

* `code=auth_code`

### Response

`HTTP 302`


## Glossary

* API: Application Programming Interface
* GA: General Availability
* DHS: Developer Hosted Server
* JS: JavaScript
* SDK: Software Development Kit
* WebRTC: Web Real-Time Communications, a W3C standard
