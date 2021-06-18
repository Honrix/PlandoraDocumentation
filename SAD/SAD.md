- [1. Introduction](#1-introduction)
    - [1.1 Purpose](#11-purpose)
    - [1.2 Scope](#12-scope)
    - [1.3 Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
    - [1.4 References](#14-references)
    - [1.5 Overview](#15-overview)
- [2. Architectural Representation](#2-architectural-representation)
- [3. Architectural Goals and Constraints](#3-architectural-goals-and-constraints)
- [4. Use-Case View](#4-use-case-view)
    - [4.1 Use-Case-Realizations](#41-use-case-realizations)
- [5. Logical View](#5-logical-view)
    - [5.1 Overview](#51-overview)
    - [5.2 Architecturally Significant Design Packages](52-architecturally-significant-design-packages)      
- [6. Process View](#6-process-view)
- [7. Deployment View](#7-deployment-view)
- [8. Implementation View](#8-implementation-view)
    - [8.1 Overiew](#81-overview)
    - [8.2 Layers](#82-layers)
- [9. Data View](#9-data-view)
- [10. Size and Performance](#10-size-and-performance)
- [11. Quality](#11-quality)

## 1. Introduction
### 1.1 Purpose
This document provides a comprehensive architectural overview of the Plandora system, using a number of different architectural views to depict different aspects of the system. It is intended to capture and convey the significant architectural decisions which have been made on the system.
### 1.2 Scope
This Software Architecture Document describes the Plandora App architecture. Plandora is an Android app which allows its users to save important events in their private environment such as birthdays and anniversaries and offers the functionality to manage their gift ideas. The software specifications described in this document outline the development process of the application.This Software Architecture Document describes the Plandora App architecture. Plandora is an Android app which allows its users to save important events in their private environment such as birthdays and anniversaries and offers the functionality to manage their gift ideas. The software specifications described in this document outline the development process of the application.
### 1.3 Definitions, Acronyms and Abbreviations
| Abbrevation | Description                         |
| ----------- | ----------------------------------- |
| MVC         | Model View Controller               |
| n/a         | not applicable                      |
| tbd         | to be determined                    |

### 1.4 References
- [Blog](https://plandora51897980.wordpress.com/)
- [Github (Code)](https://github.com/nf3lix/Plandora)
- [Github (Documentation)](https://github.com/Honrix/PlandoraDocumentation)
- [YouTrack](https://dhbw-karlsruhe.myjetbrains.com/youtrack/agiles/108-76/109-465)
- [Android App Quality Guidelines](https://developer.android.com/docs/quality-guidelines)
- [Material Design Guidelines](https://material.io/design)
- [CodeFactor](https://www.codefactor.io/)
- [Codacy](https://www.codacy.com/")

### 1.5 Overview
This Software Architecture Document contains the Architectural Representation, the Architectural Goals and Constraints, the Use-Case View, the Logical View, the Process View, the Deployment View, the Implementation View, the Data View, Size and Performance and Quality.

## 2. Architectural Representation
In this project we apply the MVC Pattern which means there are three important components: Models, Views and Controllers. Generally speaking, models represent the logic and the state of objects, the view stands for the user interface whereas the controller is responsible for each manipulation of data.
The appearance of each view is just like each string content stored in a separate XML file. 
![MVC](https://www.methodpark.de/blog/wp-content/uploads/2018/07/Model-View-Controller-High-Level-Diagram-768x339.png) 

Source: https://www.methodpark.de/blog/model-view-controller-mvc/

## 3. Architectural Goals and Constraints
Our goal is to apply the MVC pattern in our app which is mostly given in Android per default. In addition, we try to stick to the Android App Quality Guidelines (https://developer.android.com/docs/quality-guidelines)  and the Material Design Guidelines (https://material.io/design) as close as possible

## 4. Use-Case View
![UCD](https://github.com/Honrix/PlandoraDocumentation/blob/main/UCD/UCD_final.png)

## 5. Logical View
### 5.1 Overview
This section deals with the most important logical components

*PlandoraUser*: each user is able to create new events and to invite other users. 

*Event*: each event has an owner and (optionally) multiple attendees (PlandoraUsers). Each of them is able to create new gift ideas, but only the owner is allowed to edit the event details (such as the title).

*GiftIdea*: an gift idea can only exist with an event. Each attendee of an event can create several gift ideas which can be rated by the other attendee. Only the owner of an event and the owner of the gift idea is able to delete it.

### 5.2 Architecturally Significant Design Packages
The following image shows which classes belong to which component. 
![UML_Overview](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UML/UML%20overview.PNG)
The whole class diagram
![UML](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/SAD/Plandora%20Class%20Diagram.png)

In order to validate User Inputs (such as the sign up form, the create event form etc.) the Template Method Design Pattern was implemented.
The following image shows the whole Plandora Class Diagram before the implementation of the pattern:
![Class Diagram](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/SAD/uml13052021.png)

In order to make it easier to understand, the following image shows a smaller, more relevant section of the Plandora Class Diagram (also before the Design Pattern was implemented):
![Section of UML](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/SAD/uml_withoutValidator.png)

The following image shows the class diagram with the Validator (after the implementation of the Template Method Design Pattern):
![Template Design Pattern](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/SAD/uml_validator.png)

## 6. Process View
n/a

## 7. Deployment View
The app runs on the user's device and the backend is provided by an external service (Google Firebase). We frequently test our app on physical devices. The device with the lowest specs is a Huawei P8 Lite (Android 6, 8x1.2 GHz, 2GB RAM). 

![UML](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/SAD/SAD.png)


## 8. Implementation View
### 8.1 Overview
n/a

### 8.2 Layers
n/a

## 9. Data View
As we use Firestore, our database will be NoSQL. That means that any user and event (such as an upcoming birthday) is stored in a separate document. That’s why it’s not convenient to create a meaningful ER Diagram and why we created exemplary JSON documents.
![DB_Schema](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/UCS/Database%20Schema.png)
![DB_Schema_json](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/SAD/DB_Schema_json.PNG)

## 10. Size and Performance
The installed app has a size of 26MB, which is relatively small compared to other androis apps.
Using the [Android Profiler](https://developer.android.com/studio/profile/android-profiler), the CPU, memory, network, and battery resources can be monitored.
![Android Profiler](https://cdn.discordapp.com/attachments/760409169437130773/855368517251629056/unknown.png)

## 11. Quality
To capture our code quality and to find issues, we use the tool [Codacy](https://www.codacy.com/"). This tool is capable of reviewing code in git repositories automatically. 

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/2235bc5f530c450683e2ee8183cd6eec)](https://app.codacy.com/gh/nf3lix/Plandora?utm_source=github.com&utm_medium=referral&utm_content=nf3lix/Plandora&utm_campaign=Badge_Grade_Settings)
