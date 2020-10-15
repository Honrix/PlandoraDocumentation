- [1. Introduction](#1-introduction)
    - [1.1 Purpose](#11-purpose)
    - [1.2 Scope](#12-scope)
    - [1.3 Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
    - [1.4 References](#14-references)
    - [1.5 Overview](#15-overview)
- [2. Overall Description](#2-overall-description)
    - [2.1 Project Vision](#21-project-vision)
    - [2.2 Use Case Diagram](#22-use-case-diagram)
    - [2.3 Product perspective](#23-product-perspective)
    - [2.4 User characteristics](#24-user-characteristics)
    - [2.5 Dependencies](#25-dependencies)
- [3. Specific Requirements](#3-specific-requirements)
    - [3.1 Functionality](#31-functionality)
        - [3.1.1 Create account](#311-create-account)
        - [3.1.2 Login to account](#312-login-to-account)
        - [3.1.3 Logout](#313-logout)
        - [3.1.4 Edit account properties](#314-edit-account-properties)
        - [3.1.5 Save new events](#315-save-new-events)
        - [3.1.6 Save gift ideas in an event](#316-save-gift-ideas-in-an-event)
        - [3.1.7 Invite users to gift planning](#317-invite-users-to-gift-planning)
        - [3.1.8 View events in dashboard](#318-view-events-in-dashboard)
        - [3.1.9 View event details](#319-view-event-details)
        - [3.1.10 View invitations](#3110-view-invitations)
        - [3.1.11 Categorize Events](#3111-categorize-events)
        - [3.1.12 Discuss Gift Ideas](#3112-discuss-gift-ideas)
    - [3.2 Usability](#32-usability)
      - [3.2.1 Remember a user on a device](#321-remember-a-user-on-a-device)
      - [3.2.2 Filter events](#322-filter-events)
      - [3.2.3 Settings Menu](#323-settings-menu)
      - [3.2.4 Get notifications before each event](#324-get-notifications-before-each-event)
    - [3.3 Reliability](#33-reliability)
      - [3.3.1 Publishing of Updates](#331-publishing-of-updates)
      - [3.3.2 Availability](#332-availability)
    - [3.4 Performance](#34-performance)
    - [3.5 Supportability](#35-supportability)
    - [3.6 Design Constraints](#36-design-constraints)
    - [3.7 Online User Documentation and Help System Requirements](#37-online-user-documentation-and-help-system-requirements)
    - [3.8 Purchased Components](#38-purchased-components)
    - [3.9 Interfaces](#39-interfaces)
      - [3.9.1 User Interfaces](#391-user-interfaces)
      - [3.9.2 Hardware Interfaces](#392-hardware-interfaces)
      - [3.9.3 Software Interfaces](#393-software-interfaces)
      - [3.9.4 Communications Interfaces](#394-communications-interfaces)
    - [3.10 Licensing Requirements](#310-licensing-requirements)
    - [3.11 Legal, Copyright and other Notices](#311-legal-copyright-and-other-notices)
    - [3.12 Applicable Standards](#312-applicable-standards)
- [4. Supporting Information](#4-supporting-information)


## 1. Introduction
### 1.1 Purpose
This document gives a general overview of the project Plandora. It contains important requirements and outlines the software architecture of the app. Beyond that it will be needed to assess whether the project proceeded successfully.
### 1.2 Scope
Plandora is an Android app which allows its users to save important events in their private environment such as birthdays and anniversaries and offers the functionality to manage their gift ideas. The software specifications described in this document outline the development process of the application.
### 1.3 Definitions, Acronyms and Abbreviations
### 1.4 References
### 1.5 Overview
The following chapter contains our project vision and points out important use cases from the perspective of potential users. Moreover, the single requirements are explained in more detail. 
## 2. Overall Description
### 2.1 Project Vision
By creating the Android app Plandora, we want to enable our users to save the dates of birthdays, anniversaries and other private events. By entering annual or one-time events the users will be remembered in time and can conveniently access them from their smartphone. In this way, we want to prevent our users from missing important events and having unpleasant situations. Moreover, collecting ideas for a gift or discussing them with friends who use the app are desirable features. [Read more about our vision](https://plandora51897980.wordpress.com/2020/09/29/example-post-3/).
### 2.2 Use Case Diagram
### 2.3 Product perspective
### 2.4 User characteristics
### 2.5 Dependencies

## 3. Specific Requirements
### 3.1 Functionality
#### 3.1.1 Create account
The user is asked to create an account by entering an email address, a unique username, a display name and a password.
#### 3.1.2 Login to account
The user is able sign in with his email address and password. 
#### 3.1.3 Logout
#### 3.1.4 Edit account properties
The user is able to change his display name and password on a separate screen in the app. 
#### 3.1.5 Save new events
In the main activity, the user is able to create a new event (one-time or annual) under specification of the date, a description and the type of the event (birthday, anniversary, …).
#### 3.1.6 Save gift ideas in an event
The user is able to save gift ideas for a specific event. 
#### 3.1.7 Invite users to gift planning
To plan a gift with others, an event can be shared under specification of the email address or the unique user name of the attendees.
#### 3.1.8 View events in dashboard
The main activity contains an overview (dashboard) which displays upcoming events (ascending sorted by remaining days).
#### 3.1.9 View event details
The user is able to see the provided details on an event by tapping on an event in the dashboard.
#### 3.1.10 View invitations
A separate view shows the pending invitations to gift plannings.
#### 3.1.11 Categorize Events
_Optional feature_: the user can create custom categories (e.g. “family”, “friends”, “important”, …) which can be applied to events
#### 3.1.12 Discuss Gift Ideas
_Optional feature_: shared events offer a chat room in which the 
### 3.2 Usability
#### 3.2.1 Remember a user on a device
Once logged in, the user is not asked for his password any more until he changes his password or logs in from another device. 
#### 3.2.2 Filter events
The dashboard has a search bar which can be used to filter for specific events 
#### 3.2.3 Settings Menu
The app includes a settings menu in which some user appearances can be configured
#### 3.2.4 Get notifications before each event
The user gets a notification a couple of days before each events
### 3.3 Reliability
#### 3.3.1 Publishing of Updates
#### 3.3.2 Availability
### 3.4 Performance
### 3.5 Supportability
### 3.6 Design Constraints
### 3.7 Online User Documentation and Help System Requirements
### 3.8 Purchased Components
### 3.9 Interfaces
#### 3.9.1 User Interfaces
#### 3.9.2 Hardware Interfaces
#### 3.9.3 Software Interfaces
#### 3.9.4 Communications Interfaces
### 3.10 Licensing Requirements
### 3.11 Legal, Copyright and other Notices
### 3.12 Applicable Standards

## 4. Supporting Information
