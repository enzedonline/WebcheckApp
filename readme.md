Demo RESTful API from the node.js masterclass at pirple.com

Overview
The example used here is to build a RESTful API for an uptime monitoring application using no npm modules or dependencies. It will use several built-in modules. 
Not using best practice. The code will be refactored in later examples.
The purpose of the monitor is to allow the user to enter a URL and receive alerts when those resources go down or come back up.
It will include sign-up/sign-in to allow users to retain and edit their settings.
It will include functionality to receive alerts via SMS rather than email. SMS will be sent using the Twilio API, no external modules are included.
For the purposes of this app, data will be stored in JSON files rather than a database. 

Requirements:
1.	The API listens on a port and accepts incoming HTTP requests for POST, GET, PUT, DELETE and HEAD.
2.	The API allows a client to connect, then create a new user, then edit or delete that user.
3.	The API allows a user to sign in which gives them a token to that they can use to connect for subsequent authenticated requests.
4.	The API allows a user to sign out which invalidates their token.
5.	The API allows a signed in user to use their token to create a new “check”.
6.	The API allows a signed in user to use their token to edit or delete any of their “checks”.
7.	The API limits a user to a maximum of 5 checks.
8.	In the background, workers perform all the checks at appropriate times and send alerts to the user when a check changes its status from up to down and vice versa.
