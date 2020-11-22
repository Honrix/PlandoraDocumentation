- [1. Specification - Sign In and Sign Up](#1-specification-sign-in-and-sign-up)
    - [1.1 Brief Description](#11-brief-description)
- [2. Flow of Events](#2-flow-of-events)
    - [2.1 Basic Flow](#21-basic-flow)
        - [2.1.1 Activity Diagram](#211-activity-diagram)
        - [2.1.2 Mockup](#212-mockup)
    - [2.2 Alternative Flows](#21-alternative-flows)
- [3. Special Requirements](#3-special-requirements)
- [4. Precondition](#4-preconditions)
    - [4.1 App has launched](#41-app-has-launched)
    - [4.2 User not signed in](#42-user-not-signed-in)    
- [5. Postconditions](#5-postconditions)
    - [5.1 Signed in](#51-signed-in)
    - [5.2 Dashboard is shown](#51-dashboard-is-shown)      
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Specification - Show Event Details
### 1.1 Brief Description
After the application is started, the user has two options. 
One the one hand he can create a new account which requires specifying the following information: 
a unique username, an arbitrary display (which for example represents the owner of a gift idea), an email address, a secure password.
On the other hand the user can login to an existing account with its password and email address 

## 2. Flow of Events
### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Sign_in_Sign_up.png)
#### 2.1.2 Mockup
tbd
![Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/mockup/Event_Details.png)

### 2.2 Alternative Flows
#### 2.2.1 Aborting the process
At any step of this flow, the user is able to abort the process. This can either be done by closing the app or by closing the SignUpActivity premutarly. This will not affect further trys to sign in/sign up. 
## 3. Special requirements
Since we're going to use firebase, we first have to set up an authentication method which probably will be "Email address/password" (another sign-in methods available in firebase is the authentication with Google, Facebook or GitHub). Since we want to collect additional data about the user (a unique and a displayed username) we will also create a separate document for every user in Cloud Firestore.
## 4. Preconditions
### 4.1 App has launched
The app has launched (SignInActivity is shown to the user)
### 4.2 User not signed in
The user is not signed in yet. That's either because he wants to login to an existing account or he is about to create a new account. 
## 5. Postconditions
### 5.1 Signed in
After either having created a new account or having specified the correct login credentials, the user is signed in to the app.
### 5.1 Dashboard is shown
The user is navigated to the MainActivity which per default shows the dashboard including the upcoming events. 
## 6. Extension Points
tbd
## 7. Function Points
tbd
