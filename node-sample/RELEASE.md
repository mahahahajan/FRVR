# NodeJS Sample Application for AT&T Enhanced WebRTC JS SDK

This software provides a node application with the following functionality:
  * Provide user management for the sample application
  * Provide OAuth endpoint for Mobile Number authorize and callback
  * Provide login and logout functionality for Virtual Number and Account ID users

## v1.0.0
December 7, 2014

* **New:** Step-by-step sample applications (Recipes) link in the main sample application.
This is a set of simple examples including code snippets. Just launch the main
NodeJS sample application and go to https://localhost:9001/recipes/

* **Features:**
  * RESTful API:
    * `/users` - user management
    * `/login` & `/logout` - authentication (session management)
    * `/oauth/authorize` - authorize a device
    * `/oauth/callback` - redirection to sample application

### Known Issues

* XHR Error: `net::ERR_INSECURE_RESPONSE`
  * **Workaround:** load the Sample App URL in your browser, e.g., `https://127.0.0.1:9001` and click the _proceed to URL (unsafe)_.

* Error Registering Users (HTTP 409) - `POST https://localhost:9001/users 409 (Conflict)`
  * **Workaround:** Delete the file `/node-sample/users.json` and restart the Node Sample Application
