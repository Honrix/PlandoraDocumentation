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
Therefore the owner is asked to specify the unique username or email of the corresponding user.
The perspective of the invited user is discribed in [UC: Handle pending Invitations](https://github.com/Honrix/PlandoraDocumentation/blob/main/UCS/08_Handle%20Pending%20Invitations/Handle%20pending%20invitations.md).

## 2. Flow of Events

### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/06_Invite%20Users%20to%20Events/Invite%20User.png)

#### 2.1.2 Mockup
![Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Mockups/Invite%20Users.png)

#### 2.1.3 Narrative
```
Feature: Invite User to Event
  The owner of an event is able to invite other users who are allowed to share their gift ideas. 
    Therefore he is asked to specify the unique username or email of the corresponding user.

  Scenario: invitation successfully created
    Given the InviteUserDialog in EventDetailsActivityis displayed
    When user enters valid username or email
    And the user clicks submit
    Then the Invite User Dialog is disposed
    Then the invitation was sent

  Scenario: unable to find user
    Given the InviteUserDialog in EventDetailsActivityis displayed
    When the user enters invalid username or email
    And the user clicks submit
    Then the user gets error message
    Then the Invite User Dialog is disposed

  Scenario: invitation is aborted
    Given the InviteUserDialog in EventDetailsActivityis displayed
    When the user clicks back button
    Then the Invite User Dialog is disposed
```

### 2.2 Alternative Flows
#### 2.2.1 Aborting the process
At any step of this flow, the user is able to abort the process. This can either be done by closing the app or by closing the Event View.

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
The invited user got an in-app notification (see [UC: Handle pending Invitations](https://github.com/Honrix/PlandoraDocumentation/blob/main/UCS/08_Handle%20Pending%20Invitations/Handle%20pending%20invitations.md)).

## 6. Extension Points
- Handling invalid user input (e.g. invitation of users that do not exist)

## 7. Function Points
![Function Points](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Function%20Points/Invite_user_FP.PNG)

Function Points: 48.02
