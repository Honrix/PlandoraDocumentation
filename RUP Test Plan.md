# Test plan

# Table of Contents

- [Introduction](#1introduction)
    - [Purpose](#11purpose)
    - [Scope](#12scope)
    - [Intended Audience](#13intended-audience)
    - [Document Terminology and Acronyms](#14document-terminology-and-acronyms)
    - [References](#15references)
- [Evaluation Mission and Test Motivation](#2evaluation-mission-and-test-motivation)
    - [Background](#21background)
    - [Evaluation Mission](#22evaluation-mission)
    - [Test Motivators](#23test-motivators)
- [Target Test Items](#3target-test-items)
- [Outline of Planned Tests](#4outline-of-planned-tests)
    - [Outline of Test Inclusions](#41outline-of-test-inclusions)
    - [Outline of other candidates for Potential Inclusion](#42outline-of-other-candidates-for-potential-inclusion)
    - [Outline of Test Exclusions](#43-outline-of-test-exclusions)
- [Test Approach](#5test-approach)
    - [Initital Test-Idea Catalogs and Other Reference Sources](#51-initital-test-idea-catalogs-and-other-reference-sources)
    - [Testing Techniques and Types](#52testing-techniques-and-types)
        - [Data and Database Integrity Testing](#521-data-and-database-integrity-testing)
        - [Function Testing](#522-function-testing)
        - [Business Cycle Testing](#523-business-cycle-testing)
        - [User Interface Testing](#524-user-interface-testing)
        - [Performance Profililng](#525-performance-profiling)
        - [Load Testing](#526-load-testing)
        - [Stress Testing](#527-stress-testing)
        - [Volume Testing](#528volume-testing)
        - [Security and Access Control Testing](#529security-and-access-control-testing)
        - [Failover and Recovery Testing](#5210failover-and-recovery-testing)
        - [Configuration Testing](#5211configuration-testing)
        - [Installation Testing](#5212installation-testing)
- [Entry and Exit Testing](#6entry-and-exit-criteria)
    - [Test Plan](#61test-plan)
        - [Test Plan Entry Criteria](#611test-plan-entry-criteria)
        - [Test Plan Exit Criteria](#612test-plan-exit-criteria)
        - [Suspension and Resumption Criteria](#613-suspension-and-resumption-criteria)
    - [Test Cycles](#62test-cycles)
        - [Test Cycle Entry Criteria](#621test-cycle-entry-criteria)
        - [Test Cycle Exit Criteria](#622test-cycle-exit-criteria)
        - [Test Cycle Abnormal Termination](#623-test-cycle-abnormal-termination)
- [Deliverables](#7deliverables)
    - [Test Evaluation Summaries](#71test-evaluation-summaries)
    - [Reporting on Test Coverage](#72reporting-on-test-coverage)
    - [Perceived Quality Reports](#73perceived-quality-reports)
    - [Incident Logs and Change Requests](#74incident-logs-and-change-requests)
    - [Smoke Test Suite and Supporting Test Scripts](#75smoke-test-suite-and-supporting-test-scripts)
    - [Additional Work Products](#76additional-work-products)
        - [Detailed Test Results](#761detailed-test-results)
        - [Additional Automated Functional Test Scripts](#762additional-automated-functional-test-scripts)
        - [Test Guidelines](#763test-guidelines)
        - [Traceability Matrices](#764traceability-matrices)
- [Testing Workflow](#8testing-workflow)
- [Environmental Needs](#9environmental-needs)
    - [Base System Hardware](#91base-system-hardware)
    - [Base Software Elements in the Test Environment](#92base-software-elements-in-the-test-environment)
    - [Productivity and Support Tools](#93productivity-and-support-tools)
    - [Test Environment Configurations](#94test-environment-configurations)
- [Responsibilities, Staffing, and Training Needs](#10responsibilities-staffing-and-training-needs)
    - [People and Roles](#101people-and-roles)
    - [Staffing and Training Needs](#102staffing-and-training-needs)
- [Iteration Milestones](#11iteration-milestones)
- [Risks, Dependencies, Assumptions, and Constraints](#12risks-dependencies-assumptions-and-constraints)
- [Management Process and Procedures](#13-management-process-and-procedures)


## 1.	Introduction
### 1.1	Purpose
The purpose of the Iteration Test Plan is to gather all the information necessary to plan and control the test effort for the given iteration. It describes the approach to the testing of the software and is the top-level plan generated and used by the managers to direct the test effort.
This Test Plan document for Plandora supports the following objectives:
-	Identifies the items that should be targeted by the tests.
-	Identifies the motivation for and ideas behind the test areas to be covered.
-	Outlines the testing approach that will be used.
-	Identifies the required resources and provides an estimate of the test efforts.
-	Lists the deliverable elements of the test project.

### 1.2	Scope
This document describes the used tests, as well as the testing workflow. We use User Interface Test, Unit Tests and Feature Tests. Additionally, we test the Plandora app manually.

### 1.3	Intended Audience
This document is intended for internal use primarily. Further, this document will be handed in at the end of the semester and is posted on our Plandora-Blog.

### 1.4	Document Terminology and Acronyms
- **SRS**	Software Requirements Specification
- **SAD**   Software Architecture Document
- **n/a**	not applicable
- **tbd**	to be done

### 1.5	References
| Reference        | 
| ------------- |
| [Blog](https://plandora51897980.wordpress.com/) |
| [Github (Code)](https://github.com/nf3lix/Plandora) |
| [Github (Documentation)](https://github.com/Honrix/PlandoraDocumentation) |
| [YouTrack](https://dhbw-karlsruhe.myjetbrains.com/youtrack/agiles/108-76/109-465) |
| [SAD](https://github.com/Honrix/PlandoraDocumentation/blob/d398b9d82d75a2fbb670323a40499e69f588c9c9/SAD.md) | 
| [SRS](https://github.com/Honrix/PlandoraDocumentation/blob/545a622c3f6d3e2fe66e95fb0eeb2636c487ef7a/SRS.md) |
| [Use Cases](https://github.com/Honrix/PlandoraDocumentation/tree/main/UCS) |
            
## 2.	Evaluation Mission and Test Motivation
### 2.1	Background

### 2.2	Evaluation Mission

### 2.3	Test Motivators

## 3.	Target Test Items

## 4.	Outline of Planned Tests
### 4.1	Outline of Test Inclusions

### 4.2	Outline of Other Candidates for Potential Inclusion

### 4.3 Outline of Test Exclusions


## 5.	Test Approach
### 5.1 Initital Test-Idea Catalogs and Other Reference Sources
**n/a**

### 5.2	Testing Techniques and Types

#### 5.2.1 Data and Database Integrity Testing
**n/a**

#### 5.2.2 Function Testing
Unit Tests
|                        |                                                                             |
|------------------------|-----------------------------------------------------------------------------|
| Technique Objective    | Logic and processes in the app should be simulated                          |
| Technique              | JUnit Tests with Mockito                                                    |
| Oracles                | User interacts with the app (for example enters valid data in a text field) |
| Required Tools         | JUnit, Mockito                                                              |
| Success Criteria       | All tests pass without errors and the expected behavior can be observed     |
| Special Considerations |                                                                             |

Instrumented Unit Tests
|                        |                                                                             |
|------------------------|-----------------------------------------------------------------------------|
| Technique Objective    | Logic that depends on the device should be simulated on a physical device or an emulator                          |
| Technique              | Instrumented Unit Tests                                                     |
| Oracles                | Internal processes that depend on Android Framework APIs |
| Required Tools         | Android JUnit Test Runner                                                   |
| Success Criteria       | All tests pass without errors                                               |
| Special Considerations |                                                                             |

#### 5.2.3 Business Cycle Testing
**n/a**

#### 5.2.4 User Interface Testing
|                        |                                                                            |
|------------------------|----------------------------------------------------------------------------|
| Technique Objective    | Simulating UI interactions by a user                                       |
| Technique              | UI testing                                                                 |
| Oracles                | Interactions with UI components (e.g. button click) triggers action        |
| Required Tools         | Cucumber, Espresso                                                         |
| Success Criteria       | All tests pass without errors and the expected behaviour can be observed   |
| Special Considerations | -                                                                          |

#### 5.2.5 Performance Profiling 
**n/a**

#### 5.2.6 Load Testing
**n/a**

#### 5.2.7 Stress Testing
**n/a**

#### 5.2.8	Volume Testing
**n/a**

#### 5.2.9	Security and Access Control Testing
**n/a**

#### 5.2.10	Failover and Recovery Testing
**n/a**

#### 5.2.11	Configuration Testing
**n/a**

#### 5.2.12	Installation Testing
**n/a**

## 6.	Entry and Exit Criteria
### 6.1	Test Plan
#### 6.1.1	Test Plan Entry Criteria
#### 6.1.2	Test Plan Exit Criteria
#### 6.1.3 Suspension and Resumption Criteria
### 6.2	Test Cycles
#### 6.2.1	Test Cycle Entry Criteria
#### 6.2.2	Test Cycle Exit Criteria
#### 6.2.3 Test Cycle Abnormal Termination

## 7.	Deliverables
### 7.1	Test Evaluation Summaries

### 7.2	Reporting on Test Coverage

### 7.3	Perceived Quality Reports
n/a
### 7.4	Incident Logs and Change Requests
n/a
### 7.5	Smoke Test Suite and Supporting Test Scripts
n/a
### 7.6	Additional Work Products
#### 7.6.1	Detailed Test Results


#### 7.6.2	Additional Automated Functional Test Scripts
The Test Scripts can be found [here](https://github.com/nf3lix/Plandora/tree/master/app/src/androidTest/java/com/plandora)

#### 7.6.3	Test Guidelines

#### 7.6.4	Traceability Matrices
**n/a**

## 8.	Testing Workflow
While implementing code, we are continuously implementing tests (UI-Tests, Unit Tests and Feature Tests). These tests are automaticly deployed by a GitHub CI-Tool which ensures to schedule testing and review older tests.
Furthermore, before pushing to master we are manually testing the implemented code on real devices.

The following diagram shows the testing workflow:
![Testing Workflow](https://raw.githubusercontent.com/Honrix/PlandoraDocumentation/main/Testing%20Workflow.png)

## 9.	Environmental Needs
This section presents the non-human resources required for the Test Plan.
### 9.1	Base System Hardware
The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource | Quantity | Name and Type |
|---|---|---|
| CI/CD server | 1 | Travis CI Cloud |
| local test machine | 3 | Computer (Felix, Henry, Vanessa) |
| Android test device | 3 | Android Device (Felix, Henry, Vanessa) |

### 9.2	Base Software Elements in the Test Environment
The following base software elements are required in the test environment for this Test Plan.
| Software Element Name | Type |
|---|---|
| Android Studio | Test Runner / IDE |
| IntelliJ | Test Runner / IDE |
| Cucumber | human readable test definitions |


### 9.3	Productivity and Support Tools
The following tools will be employed to support the test process for this Test Plan.
| Tool Category or Type | Tool Brand Name |
|---|---|
| Repository | 	[github.com](https://github.com/) |
| Test Coverage Monitor	| [codacy](https://app.codacy.com/) |
| CI/CD Service	| [Travis CI](https://travis-ci.org/) |
| Metrics Tool | [codacy](https://app.codacy.com/) |

### 9.4	Test Environment Configurations
n/a 

## 10.	Responsibilities, Staffing, and Training Needs
### 10.1	People and Roles
| Role | Person Assigned |	Specific Responsibilities or Comments |
|---|---|---|
| Test Manager | Felix | Manages the testing of Plandora. <br><br> Responsibilities include: <br> planning and logistic, agree mission, identify motivators, acquire appropriate resources, present management reporting, advocate the interests of test, evaluate effectiveness of test effort |
| Test Designer | Felix | Defines the technical approach to the implementation of the tests for Plandora. <br><br> Responsibilities include: <br> define test approach, the test automation architecture, verify test techniques, define testability elements and structure test implementation|
| Tester | Felix, Henry, Vanessa |	Every team member implements and executes the tests.<br><br> Responsibilities include:<br> implement tests and test suites, execute test suites, log results, analyze and recover from test failures, document incidents|
| Test System Administrator | Henry | Ensures test environment and assets are managed and maintained (e.g. GitHub CI) | 
| Database Administrator, Database Manager | **tbd** | **tbd** |
| Implementer | Felix, Vanessa | Implements the required test components.|


### 10.2	Staffing and Training Needs
**n/a**

## 11.	Iteration Milestones
| Milestone | Planned Start Date | Actual Start Date | Planned End Date | Actual End Date |
|---|---|---|---|---|
| Run Cucumber Tests | 27.10.2020 | 27.10.2020 | 07.12.2020 | 01.12.2020   |
| Having Unit Tests | 27.04.2021 | 29.04.2021   | 04.05.2021   | **tbd**   |
| Having UI Tests | 27.04.2021 | 07.04.2021 | 04.05.2021 | 07.04.21 |
| Having CI in Github | 27.04.2021 | **tbd** | 04.05.2021 | **tbd** |
| 50% Unit Test Coverage | 04.05.2021 | **tbd** | 18.05.2021 | **tbd** |


## 12.	Risks, Dependencies, Assumptions, and Constraints
| Risk | Mitigation Strategy	| Contingency (Risk is realized) |
|---|---|---|
| Unexpected failures in production | Cover as much scenarios as possible, Logging | Look into logs and fix the bug, Roll back version if necessary |
## 13. Management Process and Procedures

