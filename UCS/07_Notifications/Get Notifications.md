- [1. Specification - Handle pending invitations](#1-specification-handle-pending-invitations)
    - [1.1 Brief Description](#11-brief-description)
- [2. Flow of Events](#2-flow-of-events)
    - [2.1 Basic Flow](#21-basic-flow)
        - [2.1.1 Activity Diagram](#211-activity-diagram)
        - [2.1.2 Mockup](#212-mockup)
    - [2.2 Alternative Flows](#21-alternative-flows)
- [3. Special Requirements](#3-special-requirements)
- [4. Precondition](#4-preconditions)
    - [4.1 User is signed in](#41-user-is-signed-in)
- [5. Postconditions](#5-postconditions)
    - [5.1 Result is shown](#51-result-is-shown)
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Specification - Handle pending invitations
### 1.1 Brief Description
The user is able to receive notifications either inside the app or as a push notification if the app is closed/runs in the background. These notifications are giving information about upcoming events to the user.

## 2. Flow of Events
### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/07_Notifications/Get%20Notifications.png)

#### 2.1.2 Mockup
![Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Mockups/Notifications.png)

### 2.2 Alternative Flows
n/a

## 3. Special requirements
As we are going to use Googles FCM (Firebase Clous Messaging), we first have to set up the connection to the FCM API in order to send/receive notifications. Therefore, we need to implement a POST Request to the FCM API as well as the handling of the received JSON Objects (Messages).
Since the push notification should be received when an event is due in two weeks/a day, we need to set up topics to which we will send those messages. All attendees will be subscribed to the event-topic and should receive the notification.

## 4. Preconditions
### 4.1 User is signed in
To receive invitations, the user must be signed in.

## 5. Postconditions
### 5.1 Notification is shown
The notification is available for the user and can be seen on the notification box of the smartphone.


## 6. Extension Points
n/a

## 7. Function Points
![Function Points](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Function%20Points/Get_Notifications_FP.PNG)

Function Points: 31.36
