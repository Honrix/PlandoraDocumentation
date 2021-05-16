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

## 1. Specification - Show Event Details
### 1.1 Brief Description
The user is able to see the provided details on an event by tapping on an event in the dashboard.
## 2. Flow of Events
This use case is part of a CRUD, which means that it is about creating, reading, updating and deleting entries. 
![CRUD](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/CRUD/Create%20Event.png)

A more detailed diagram is listed in [2.1.1](#211-activity-diagram).
### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/04_Show%20Event%20Details/Show%20Event%20Details.png)

[Feature File](https://github.com/nf3lix/Plandora/blob/master/app/src/androidTest/java/com/plandora/steps/view_event_details.feature)
#### 2.1.2 Mockup
The detail view is almost identical to "[Create Event](https://github.com/Honrix/PlandoraDocumentation/blob/main/UCS/01_Create%20Event/Create%20Event.md)" view (see: [Mockup](https://github.com/Honrix/PlandoraDocumentation/blob/main/UCS/Mockups/Create%20Event.PNG)).

![Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Mockups/Event_Details.png)
#### 2.1.3 Narrative
```
Feature: View Event Details
  The user is able to view details of an event and edit them

  Scenario: edit event details
    Given the user is on EventDetailActivity
    When the user clicks on edit event
    Then the user lands on EditDetailActivity

  Scenario: close event details
    Given the user is on EventDetailActivity
    When the user clicks on close detailview
    Then the user lands on Dashboard
```
### 2.2 Alternative Flows
#### 2.2.1 Aborting the process
At any step of this flow, the user is able to abort the process. This can either be done by closing the app or by closing the Event View.

## 3. Special requirements
n/a

## 4. Preconditions
### 4.1 User is signed in
To show event details, the user must be signed in.

### 4.2 User is attendee of an event
The user must be attendee or owner of the event to see its details. 

### 4.3 User is on Event View
To show event details, the user must be on the view to create a new event or to see the detailed information of an event. 

## 5. Postconditions
### 5.1 Event Detail View is closed
After having shown the event details, the event detail view is closed.
### 5.2 Dashboard is shown
The user is navigated to the MainActivity which per default shows the dashboard including the upcoming events. 

## 6. Extension Points
- No Extension Points

## 7. Function Points
![Function Points](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Function%20Points/Show_Event_Details_FP.PNG)

Function Points: 41.16
