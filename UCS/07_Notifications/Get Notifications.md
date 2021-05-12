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
The user is able to receive notifications as well inside the app as on the smarthpone outside of the app. These notifications are giving information to the user.

## 2. Flow of Events
### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/07_Notifications/Get%20Notifications.png)

#### 2.1.2 Mockup
![Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Mockups/Notifications.png)

### 2.2 Alternative Flows
n/a

## 3. Special requirements
n/a

## 4. Preconditions
### 4.1 User is signed in
To receive invitations, the user must be signed in.

## 5. Postconditions
### 5.1 Invitation is accepted or declined
The received invitation was accepted or declined by the user. In case of an acception, said user is now an attendee of the event. Otherwise, the pending invitation is deleted and the user will no longer see the invitation.

## 6. Extension Points
n/a

## 7. Function Points
![Function Points](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Function%20Points/Get_Notifications_FP.PNG)

Function Points: 31.36
