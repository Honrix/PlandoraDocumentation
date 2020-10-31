- [1. Specification - Filter upcoming Events](#1-specification-filter-upcoming-events)
    - [1.1 Brief Description](#11-brief-description)
- [2. Flow of Events](#2-flow-of-events)
    - [2.1 Basic Flow](#21-basic-flow)
        - [2.1.1 Activity Diagram](#211-activity-diagram)
        - [2.1.2 Mockup](#212-mockup)
        - [2.1.3 Narrative](#213-narrative)
    - [2.2 Alternative Flows](#21-alternative-flows)
- [3. Special Requirements](#3-special-requirements)
- [4. Precondition](#4-preconditions)
- [5. Postconditions](#5-postconditions) 
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Specification - Filter upcoming Events
### 1.1 Brief Description
By default the dashboard shows all upcoming events sorted in ascending order concerning the number of remaining days. Beyond this, a search bar should be usable to filter the dashbaord for specific events. To achieve this, the user is able to apply a text based search or to filter for specific types of events (e.g. birthdays or holidays). When entering text into the search field, the dashboard should be updated instantaneously.

## 2. Flow of Events

### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Filter%20upcoming%20Events.png)

#### 2.1.2 Mockup
tbd
#### 2.1.3 Narrative
```
Feature: Filter Upcoming Events
  The user is able to filter the dashboard by specific events

  Scenario: apply text search
    Given the user clicked on search bar
    When the user enters text in search bar
    Then the dashboard is filtered by matching text

  Scenario: apply search for event types
    Given the user clicked on search bar
    When the user clicks on type label
    Then the dashboard is filtered by given type

  Scenario: search is aborted
    Given the user clicked on search bar
    When the user clicks on back button
    Then the search bar disappears
```
### 2.2 Alternative Flows
tbd
## 3. Special requirements
tbd
## 4. Preconditions
tbd
## 5. Postconditions
tbd
## 6. Extension Points
tbd
## 7. Function Points
tbd
