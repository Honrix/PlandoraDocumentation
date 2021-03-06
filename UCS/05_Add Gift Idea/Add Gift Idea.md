- [1. Specification - Add Gift Idea](#1-specification-add-gift-idea)
    - [1.1 Brief Description](#11-brief-description)
- [2. Flow of Events](#2-flow-of-events)
    - [2.1 Basic Flow](#21-basic-flow)
        - [2.1.1 Activity Diagram](#211-activity-diagram)
        - [2.1.2 Mockup](#212-mockup)
    - [2.2 Alternative Flows](#21-alternative-flows)
- [3. Special Requirements](#3-special-requirements)
- [4. Precondition](#4-preconditions)
    - [4.1 User is signed in](#41-user-is-signed-in)
    - [4.2 Dashboard is shown](#42-dashboard-is-shown)
- [5. Postconditions](#5-postconditions)
    - [5.1 Result is shown](#51-result-is-shown)
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Specification - Add Gift Idea
### 1.1 Brief Description
The user is able to add gift ideas including a description to an event.

## 2. Flow of Events
This use case is part of a CRUD, which means that it is about creating, reading, updating and deleting entries. 
![CRUD](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/CRUD/Add%20Gift%20Idea%20CRUD.png)
### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/05_Add%20Gift%20Idea/Add%20Idea.png)

#### 2.1.2 Mockup
![Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Mockups/Add%20Gift%20Ideas.png)

### 2.2 Alternative Flows
#### 2.2.1 Aborting the process
At any step of this flow, the user is able to abort the process. This can either be done by closing the app or by closing the Event View.

## 3. Special requirements
n/a

## 4. Preconditions
### 4.1 User is signed in
To create a new event, the user must be signed in.

### 4.2 User is attendee of an event
The user must attendee or owner of the event. 

### 4.2 User is on Event View
To add a new idea, the user must be on the view to create a new event or to see the detailed information of an event. 

## 5. Postconditions
### 5.1 Gift Idea is added to event
An added idea is displayed in the event details and stored in firestore.

## 6. Extension Points
- Handling of invaid user input

## 7. Function Points
![Function Points](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Function%20Points/Add_Gift_Idea_FP.PNG)

Function Points: 41.16
