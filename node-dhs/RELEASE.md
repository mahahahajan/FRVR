# NodeJS Server (DHS) for AT&T Enhanced WebRTC JS SDK

The DHS is a node application with the following functionality:
  * Manage configuration options for the SDK's Node Sample Application
  * Manage Application configuration (application key, secret, redirect_uri, etc.)
  * Handle AT&T OAuth Token creation using credentials and scope.
  * Create E911 Id given an address.

# v1.0.0 - GA

December 7, 2014

* **Features:**
  * Configuration file to setup AT&T Developer
Program enrollment assets (application key and secret, redirect_uri).
  * RESTful API:
    * `/config` - environment options necessary to configure the SDK.
    * `/tokens` - AT&T's OAuth use to generate Access Tokens
    * `/e911ids` - create E911 Ids
  * **Documentation:**
    * Instructions on how to setup & start the DHS pointing to different
    environments
    * Description of the RESTful API


### Known Issues

* DHS Configuration: Virtual Numbers must be valid 10-digit phone numbers.
