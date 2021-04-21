- [1. Specification - Invite Users to Events](#1-specification-invite-users-to-events)
    - [1.1 Brief Description](#11-brief-description)
- [2. Flow of Events](#2-flow-of-events)
    - [2.1 Basic Flow](#21-basic-flow)
        - [2.1.1 Activity Diagram](#211-activity-diagram)
        - [2.1.2 Mockup](#212-mockup)
        - [2.1.3 Narrative](#213-narrative)
    - [2.2 Alternative Flows](#21-alternative-flows)
- [3. Special Requirements](#3-special-requirements)
- [4. Precondition](#4-preconditions)
    - [4.1 User is signed in](#41-user-is-signed-in)
    - [4.2 Dashboard is shown](#42-dashboard-is-shown)
- [5. Postconditions](#5-postconditions)
    - [5.1 Result is shown](#51-result-is-shown)
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Specification - Invite Users to Events
### 1.1 Brief Description
The owner of an event is able to invite other Plandora users, who are allowed to display the event details and to share their gift ideas.
The perspective of the invited user is discribed in [UC: Handle pending Invitations](https://github.com/Honrix/PlandoraDocumentation/blob/main/UCS/Handle%20pending%20invitations.md).

## 2. Flow of Events

### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Invite%20User.png)

#### 2.1.2 Mockup
tbd

#### 2.1.3 Narrative
tbd

### 2.2 Alternative Flows
n/a

## 3. Special requirements
n/a

## 4. Preconditions
### 4.1 User is signed in
To invite another Plandora user to an event, the user must be signed in.

### 4.2 User is attendee of an event
To invite another Plandora user, you must be owner of the event. 

### 4.3 User is on Event View
To invite another user, you must be on the view to create a new event or to see the detailed information of an event. 

## 5. Postconditions
### 5.1 Gift Idea is added to event
The invited user got an in-app notification (see UC: Handle Pending Invitations).

## 6. Extension Points
tbd

## 7. Function Points
![Function Points](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/fp/Invite_user_FP.PNG)
Function Points: 48.02
