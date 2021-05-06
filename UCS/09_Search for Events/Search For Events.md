- [1. Specification - Search For Events](#1-specification-create-event)
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
- [5. Postconditions](#5-postconditions)
    - [5.1 Searched events are displayed](#51-searched-event-are-displayed)    
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Specification - Search For Events
### 1.1 Brief Description
In the main activity, the user is able to search and filter for events. Therefore he is asked to enter a filter condition, e.g. name, date or category.
* Available categories are: Birthday, Holiday, Anniversary, Others

### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/09_Search%20for%20Events/Search%20For%20Events.png)

#### 2.1.2 Mockup
![Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Mockups/Search%20for%20Events.png)

#### 2.1.3 Narrative
```
Feature: Search For Events
  The user is able to search for events. Therefore he is asked to enter a filter condition, e.g. the date, the name or the category.

  Scenario: search successfully done
    Given the user is on SearchForEventsActivity
    When the user enters valid data
    And the user clicks submit
    Then just searched events are displayed

  Scenario: failed to search for events
    Given the user is on SearchForEventsActivity
    When the user enters invalid data
    And the user clicks submit
    Then the user gets error message

  Scenario: search is aborted
    Given the user is on SearchForEventsActivity
    When the user clicks cancel button
    Then the user lands on Dashboard
```
### 2.2 Alternative Flows

## 3. Special requirements

## 4. Preconditions
### 4.1 Signed in
To search for events, the user must be signed in. 

## 5. Postconditions
### 5.1 Searched events are displayed
After searching for events the user is navigated back to the dashboard with normal and unfiltered view. 

## 6. Extension Points

## 7. Function Points
![Function Points]()

Function Points: 59.28
