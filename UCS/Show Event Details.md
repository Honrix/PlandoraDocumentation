- [1. Specification - View Event Details](#1-specification-view-event-details)
    - [1.1 Brief Description](#11-brief-description)
- [2. Flow of Events](#2-flow-of-events)
    - [2.1 Basic Flow](#21-basic-flow)
        - [2.1.1 Activity Diagram](#211-activity-diagram)
        - [2.1.2 Mockup](#212-mockup)
        - [2.1.3 Narrative](#213-narrative)
    - [2.2 Alternative Flows](#21-alternative-flows)
- [3. Special Requirements](#3-special-requirements)
- [4. Precondition](#4-preconditions)
    - [4.1 Signed in](#41-signed-in)
    - [4.2 Dashboard is displayed](#42-dashboard-is-displayed)    
- [5. Postconditions](#5-postconditions)
    - [5.1 Dashboard is displayed](#51-dashboard-is-displayed)    
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Specification - Create Event
### 1.1 Brief Description
The user is able to see the provided details on an event by tapping on an event in the dashboard.
## 2. Flow of Events
This use case is part of a CRUD, which means that it is about creating, reading, updating and deleting entries. 
![CRUD](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/CRUD/Create%20Event.png)

A more detailed diagram is listed in [2.1.1](#211-activity-diagram).
### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Show%20Event%20Details.png)
#### 2.1.2 Mockup
The detail view is almost identical to "create event" ([look here](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/mockup/Create%20Event.PNG))
#### 2.1.3 Narrative
### 2.2 Alternative Flows
## 3. Special requirements
## 4. Preconditions
### 4.1 Signed in
To create a new event, the user must be signed in. 
### 4.2 Dashboard is displayed
To create a new event, the dashboard in the MainActivity must be open.
## 5. Postconditions
### 5.1 Dashboard is displayed
After creating a new event the user is navigated back to the dashboard. 
## 6. Extension Points
## 7. Function Points
