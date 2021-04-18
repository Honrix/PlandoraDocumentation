- [1. Specification - Handle pending invitations](#1-specification-handle-pending-invitations)
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

## 1. Specification - Handle pending invitations
### 1.1 Brief Description

## 2. Flow of Events
### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Handle%20pending%20invitations.png)

#### 2.1.2 Mockup
![Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/mockup/Pending%20Invitations.png)

#### 2.1.3 Narrative

### 2.2 Alternative Flows

## 3. Special requirements
n/a

## 4. Preconditions
### 4.1 User is signed in
To handle pending invitations, the user must be signed in.

### 4.2 User is invited to an event
The user must be invited to an event in order to receive an invitation. 

### 4.2 User is on Notifications Dialog
To handle a pending invitations (either accept or decline), the user must be on the Notifications Dialog. 

## 5. Postconditions
### 5.1 Pending invitation is removed from the Dialog
The pending invitation was either declined or accepted. In case it was accepted, the User is added as an attendee for the event.
In both cases, the pending invitations is removed from the Notifications Dialog.

## 6. Extension Points
tbd
## 7. Function Points

Function Points: 44.1
