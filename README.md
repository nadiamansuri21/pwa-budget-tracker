# PWA Budget-Tracker
- Using Progressive Web Application (PWA) this application enables the user to add expenses and deposits to their budget with or without an online connection. When entering transactions offline, data should populate the total when connected back online.

### Demo

### User Story
AS AN avid traveller
I WANT to be able to track my withdrawals and deposits with or without a data/internet connection
SO THAT my account balance is accurate when I am traveling


### Acceptance Criteria
GIVEN a budget tracker without an internet connection
WHEN the user inputs an expense or deposit
THEN they will receive a notification that they have added an expense or deposit
WHEN the user reestablishes an internet connection
THEN the deposits or expenses added while they were offline are added to their transaction history and their totals are updated

## Table of contents
- [General Info](#Info)
- [Functionality](#Functionality)
- [Install](#Install)
- [Dependencies](#Dependencies)
- [Technologies](#Technologies)
- [Author](#Author)

# General Info

### What is Progressive Web Application (PWA)?
- A Progressive Web App (PWA) is a web app that uses modern web capabilities to deliver an app-like experience to users. These apps meet certain requirements (see below), are deployed to servers, accessible through URLs, and indexed by search engines.

### What is required for PWA?
To be considered a Progressive Web App, your app must be:

- Progressive - Work for every user, regardless of browser choice, because they are built with progressive enhancement as a core tenet.

- Responsive - Fit any form factor, desktop, mobile, tablet, or whatever is next.

- Connectivity independent - Enhanced with service workers to work offline or on low quality networks.

- App-like - Use the app-shell model to provide app-style navigation and interactions.

- Fresh - Always up-to-date thanks to the service worker update process.

- Safe - Served via HTTPS to prevent snooping and ensure content has not been tampered with.

- Discoverable - Are identifiable as “applications” thanks to W3C manifests and service worker registration scope allowing search engines to find them.

- Re-engageable - Make re-engagement easy through features like push notifications.

- Installable - Allow users to “keep” apps they find most useful on their home screen without the hassle of an app store.

- Linkable - Easily share via URL and not require complex installation.

#### Offline Support
- Apps should be able to work offline. Whether that be displaying a proper "offline" message or caching app data for display purpose.


# Functionality 

BUDGET-TRACKER Offline Functionality:
- Enter deposits offline
- Enter expenses offline

When brought back online:
- Offline entries should be added to tracker.

## *In order to achieve OFFLINE SUPPORT, a manifest file and a service worker file must be created.*

### Manifest ``` manifest.webmanifest ```
- #### Purpose
    - The manifest file is a simple text file (JSON file) that lists the resources (app's displayed name, icons, as well as splash screen) the browser should cache for offline access. 

### Service Worker  ``` service-worker.js ```
- #### Purpose
    - Service worker provides a programmatic way to cache app resources.  

- #### Service Worker Life Cycle
    - install
    - activate
    - fetch


- The service worker is registered/linked in the front end side (main html ``` index.html ``` ).


# Install
```bash
npm i install
```

### Run 
- 1. Install all dependencies
- 2. Create a terminal on the project root and run:
    ```` bash
    mongod
    ````
- 3. Create another terminal on the same folder and run:
    ``` bash
    npm start
    ```

### Deploy
- Follow the steps on how to deploy an app on heroku

1. Create a repository of your project in github. 
2. Clone that reporisitory to your VS Code using git:
``` bash
git clone "the link of the github repo"
```
3. In your project folder terminal create a heroku application using this command:
``` bash 
heroku create "name of your project"
```
4. Log in to your heroku account and look for your project in the DAHSBOARD. Go to the tabs located on top and click on DEPLOY. In the Deployement Method, click on the github icon to connect it to your github repository. Then on Automatic Deploy, click and enable automatic deploys

5. On the tabs on top, click Overview then on Installed add-ons click Configure Add-ons.

6. Since this project is build with MongoDB, search for mLab MongoDB in the Add-ons search. Make sure to select the "Sandbox-Free plan. Then provision it. 

7. Make sure that you have "process.env.MONGODB_URI" in your mongoose.connect under the server file. 

8. Try to add a code and push it to your github. It will automatically hook it to heroku. Now view your heroku app.

# Dependencies
``` bash
"dependencies": {
    "express": "^4.17.1",
    "install": "^0.13.0",
    "mongodb": "^3.5.5",
    "mongoose": "^5.9.7",
    "nodemon": "^2.0.2"
  }

```

# Technologies
- HTML5
- CSS
- jQuery
- Express
- MongoDB
- Mongoose
- IndexedDB
- Bootstrap

# Author
- Nadia A Alamgir 
- github: 
- website: 
- email: 