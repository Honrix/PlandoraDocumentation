- [1. Specification - Create Event](#1-specification-create-event)
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
    - [5.2 New Event was created or the process was aborted](#52-new-event-was-created-or-the-process-was-aborted)    
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Specification - Create Event
### 1.1 Brief Description
In the main activity, the user is able to search for events which makes it easier to find certain events (for example by name).
## 2. Flow of Events
This use case is part of a CRUD, which means that it is about creating, reading, updating and deleting entries. 
![CRUD](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/CRUD/Create%20Event.png)

A more detailed diagram is listed in [2.1.1](#211-activity-diagram).
### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/01_Create%20Event/Create%20Event.png)

[Feature File](https://github.com/nf3lix/Plandora/blob/master/app/src/androidTest/java/com/plandora/steps/create_event.feature)

#### 2.1.2 Mockup
![Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Mockups/Create%20Event.PNG)

#### 2.1.3 Narrative
```
Feature: Create Event
  The user is able to create a new event. Therefore he is asked to specify the date, a
  title, the category and whether the event is annual or one-time.

  Scenario: event successfully created
    Given the user is on CreateEventActivity
    When the user enters valid data
    And the user clicks submit
    Then a new event is created
    Then the user lands on Dashboard

  Scenario: failed to create event
    Given the user is on CreateEventActivity
    When the user enters invalid data
    And the user clicks submit
    Then the user gets error message

  Scenario: event creation is aborted
    Given the user is on CreateEventActivity
    When the user clicks back button
    Then the user lands on Dashboard
    Then the data already entered is stored as draft
```
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
### 5.2 New Event was created or the process was aborted
A new event will be visible in the dashboard. If the process was aborted, the information filled in until then are saved in the local storage as a draft.
## 6. Extension Points
## 7. Function Points
![Function Points](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Function%20Points/Create_Event_FP.PNG)

Function Points: 60.76
