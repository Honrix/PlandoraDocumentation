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
    - [4.1 User is signed in](#41-user-is-signed-in)
    - [4.2 Dashboard is shown](#42-dashboard-is-shown)
- [5. Postconditions](#5-postconditions)
    - [5.1 Result is shown](#51-result-is-shown)
- [6. Extension Points](#6-extension-points)
- [7. Function Points](#7-function-points)

## 1. Specification - Filter upcoming Events
### 1.1 Brief Description
By default the dashboard shows all upcoming events sorted in ascending order concerning the number of remaining days. Beyond this, a search bar should be usable to filter the dashbaord for specific events. To achieve this, the user is able to apply a text based search or to filter for specific types of events (e.g. birthdays or holidays). When entering text into the search field, the dashboard should be updated instantaneously.

## 2. Flow of Events

### 2.1 Basic Flow
#### 2.1.1 Activity Diagram
![Activity Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/03_Filter%20upcoming%20Events/Filter%20upcoming%20Events.png)

[Feature File](https://github.com/nf3lix/Plandora/blob/master/app/src/androidTest/java/com/plandora/steps/filter_upcoming_events.feature)
#### 2.1.2 Mockup
![Filter Events Mockup](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Mockups/Filter_View.png)
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
At any single step of this flow, the user is able to abort the process by clicking the back button.

## 3. Special requirements
n/a

## 4. Preconditions
### 4.1 User is signed in
To filter upcoming events, the user must be signed in.
### 4.2 Dashboard is shown
The dashboard including all upcoming events is shown to the user.
## 5. Postconditions
### 5.1 Result is shown
After applying the filter, all important events a shown in the dashboard. If the process was aborted prematurely, the complete dashboard is shown
## 6. Extension Points
tbd
## 7. Function Points
![Function Points](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Function%20Points/Filter_Upcoming_Events_FP.PNG)

Function Points: 22.80
