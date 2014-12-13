# JavaScript SDK for AT&T Enhanced WebRTC API

# Contents of this package

* `/js/ewebrtc-sdk.min.js`: JavaScript client library for AT&T Enhanced WebRTC API
* `/node-dhs`: Node DHS
* `/node-sample/`: Node Sample Application
* `/node-sample/public/tutorial/index.html`: AT&T's Enhanced WebRTC Javascript SDK tutorial
* `/node-sample/public/api-docs/index.html`: JS SDK API reference documentation

# Using the Sample Application

This is a guide to setup AT&T's Enhanced WebRTC sample application. The sample application can be
used as a reference so that developers may learn from and build their own applications based on it.

## Summary

* Enroll in the [AT&T Developer program ](http://developer.att.com/)
* Create your application in the developer portal and generate application key/secret.
* Configure the Node DHS using your application key/secret generated above as well as some additional
configuration (see below).
* Configure the Node Sample Application with your DHS URL
* Install the Node DHS dependencies: Run `$ npm install` in the `node-dhs` directory.
* Install the Node Sample Application dependencies: Run `$ npm install` in the `node-sample` directory.
* Start the DHS: Run `$ npm start` from the `node-dhs` directory
* Start the Sample Application: Run `$ npm start` from the `node-sample` directory
* Launch browser to run the sample application: `https://localhost:9001/`

## 1. Enrolling and Creating your Enhanced WebRTC Application.

Before you can access the AT&T Platform services, you must enroll in AT&T's Developer Program, then register your
application for the services that you want to access and to get an API key and
secret key. These keys are necessary to call the underlying AT&T RESTful APIs
that access the services.

### 1.1. Enrolling in the Developer Program

1. Create a new developer account on the [AT&T Developer program](http://developer.att.com/), or login to
an existing account.
2. Request _Premium Access_ for your account from the CTS Middleware Data Team.

### 1.2. Creating your own Enhanced WebRTC application
**Prerequisite**: An AT&T Developer Account with _Premium Access_

Perform the following steps to register an application:

1. Sign In to your AT&T Developer Account created in the previous section.
2. Go to _Manage my Account_
3. Select _My Apps_ from the bar at the top of the page (right-most orange button).
5. Click _Setup a New Application_
6. Chose the scope: _Enhanced WebRTC_ & _In App Calling (displaying the AT&T user's phone number)_ from the list.

After your application is registered, you have an API Key and Secret key. These
keys are necessary to get your applications working with the AT&T Platform
APIs.

## 2. Installing System Requirements

Refer to the online documentation to install these dependencies for your system.

* [Download NodeJS](http://nodejs.org/download/)

## 3. Configure & Run the Node DHS

* Refer to: [`/node-dhs/README.md`](/node-dhs/README.md) for details on the
DHS's features and setup instructions.
* Refer to: [`/node-dhs/RELEASE.md`](/node-dhs/RELEASE.md) for the latest
Release Notes and information about known issues, workarounds, etc.

## 4. Configure & Run the Node Sample Application

* Refer to: [`/node-sample/README.md`](/node-sample/README.md) for details on
the Sample Application's features and setup instructions.
* Refer to: [`/node-sample/RELEASE.md`](/node-sample/RELEASE.md) for the latest
Release Notes and information about known issues, workarounds, etc.

### Notes

* The Node Sample Application uses the DHS for its initial configuration. It sets up:
* Enhanced WebRTC API Endpoint,
* DHS RESTful API


# 5. Acronyms and Terminology

* API: Application Programming Interface
* GA: General Availability
* DHS: Developer Hosted Server
* JS: JavaScript
* SDK: Software Development Kit
* WebRTC: Web Real-Time Communications, a W3C standard
