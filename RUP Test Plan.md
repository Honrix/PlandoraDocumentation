# Test plan

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

### 1.5	 References
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
By testing source code, we ensure our application to run smoothly. The goal is to make sure, that our application does not run into any unexpected errors.
### 2.2	Evaluation Mission
The mission of this test plan is to prevent errors in production and ensure an outstanding software quality.
### 2.3	Test Motivators
Our testing is motivated by 
- quality risks 
- technical risks, 
- use cases 
- functional requirements

## 3.	Target Test Items
The listing below identifies those test items (software, hardware, and supporting product elements) that have been identified as targets for testing. 
This list represents what items will be tested. 

Items for Testing:
- SpringBoot-Web Backend
- Angular Frontend

## 4.	Outline of Planned Tests
### 4.1	Outline of Test Inclusions
Testing the backend with unit tests and some e2e tests. 
End2End testing the forntend application.
### 4.2	Outline of Other Candidates for Potential Inclusion
Stress Testing the application and its servers.
Findung security holes.
### 4.3 Outline of Test Exclusions
n/a

## 5.	Test Approach
### 5.1 Initital Test-Idea Catalogs and Other Reference Sources
**n/a**
### 5.2	Testing Techniques and Types
#### 5.2.1 Data and Database Integrity Testing
|| |
|---|---|
|Technique Objective  	| The backend should be started. Several request should be made to determine the correct functionality of the backend. |
|Technique 		|  Data should be mocked. A productive capable environment (similar database technology) should be used. |
|Oracles 		| Endpoints return the correct and expected data as well as the expected response codes. |
|Required Tools 	| SpringBoot-Test (Unit testing & E2E testing framework), Postman (Newman) |
|Success Criteria	| expected responses, passing tests |
|Special Considerations	|     -          |

#### 5.2.2 Function Testing
|| |
|---|---|
|Technique Objective  	| Every interaction with the frontend should function as intended. |
|Technique 		| Unit Tests and Gherkin tests should test the technology. For testing the frontend we use a mock backend.  |
|Oracles 		| (Fake-)Backend returns expected data, information is shown as expected |
|Required Tools 	| Gherkin, Chai, Mocha |
|Success Criteria	| Expected behavior and passing tests |
|Special Considerations	|     -          |

#### 5.2.3 Business Cycle Testing
**n/a**

#### 5.2.4 User Interface Testing
**n/a**

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
GitLab Actions will provide console log which is printed by the appropriate testing frameworks
### 7.2	Reporting on Test Coverage
Coverage returned by Istanbul

Frontend:
![](https://gitlab.com/kzynn/partyplayer-ui/badges/master/coverage.svg)
![](https://gitlab.com/kzynn/partyplayer-ui/badges/master/pipeline.svg)
Backend:
![](https://gitlab.com/kzynn/partyplayer/badges/master/coverage.svg)
![](https://gitlab.com/kzynn/partyplayer/badges/master/pipeline.svg)

### 7.3	Perceived Quality Reports
n/a
### 7.4	Incident Logs and Change Requests
n/a
### 7.5	Smoke Test Suite and Supporting Test Scripts
n/a
### 7.6	Additional Work Products
#### 7.6.1	Detailed Test Results
GitLab pipeline tests

#### 7.6.2	Additional Automated Functional Test Scripts
**n/a**
#### 7.6.3	Test Guidelines
Easy tests should be tested for functionality. Due to timing constraints,the quality of a test might suffer. E.G. not all possible inputs can be tested.
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
| Production Server | 1 | API provider / Frontend provider / Database|
| GitLab CI/CD |  | Testing, building and deploying application |

### 9.2	Base Software Elements in the Test Environment
The following base software elements are required in the test environment for this Test Plan.

| Software Element Name | Version | Type and Other Notes |
|---|---|---|
| Linux | latest | Operating System |
| NodeJS | latest | Famework |
| MySQL | latest | Database |

### 9.3	Productivity and Support Tools
The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type | Tool Brand Name                              |
|-----------------------|----------------------------------------------|
| Code Hoster           | [gitlab.com](https://gitlap.com/partyplayer/) |
| CI Service            |  [gitlab.com](https://gitlap.com/partyplayer/) |

### 9.4	Test Environment Configurations
n/a 

## 10.	Responsibilities, Staffing, and Training Needs
### 10.1	People and Roles
This table shows the staffing assumptions for the test effort.

Human Resources


| Role | Minimum Resources Recommended (number of full-time roles allocated) |	Specific Responsibilities or Comments |
|---|---|---|
| Test Manager | 1 | Provides management oversight. <br> Responsibilities include: <br> planning and logistics <br> agree mission <br> identify motivators<br> acquire appropriate resources<br> present management reporting<br> advocate the interests of test<br>evaluate effectiveness of test effort |
| Test Designer | 2 | Defines the technical approach to the implementation of the test effort. <br> Responsibilities include:<br> define test approach<br> define test automation architecture<br> verify test techniques<br> define testability elements<br> structure test implementation|
| Tester | 4 |	Implements and executes the tests.<br> Responsibilities include:<br> implement tests and test suites<br> execute test suites<br> log results<br> analyze and recover from test failures<br> document incidents|
| Test System Administrator | 1 | Ensures test environment and assets are managed and maintained.<br> Responsibilities include:<br> 	administer test management system<br> install and support access to, and recovery of, test environment configurations and test labs | 
| Database Administrator, Database Manager | 1 | Ensures test data (database) environment and assets are managed and maintained.<br> Responsibilities include:<br> support the administration of test data and test beds (database). |
| Implementer | 4 | Implements and unit tests the test classes and test packages.<br> Responsibilities include:<br> creates the test components required to support testability requirements as defined by the designer |

### 10.2	Staffing and Training Needs
**n/a**
## 11.	Iteration Milestones

| Milestone | Planned Start Date | Actual Start Date | Planned End Date | Actual End Date |
|---|---|---|---|---|
| Have Unit Tests | 01.04.2020 | since start of development | 4.6.2020 | 4.6.2020   |
| 50% coverage | 12.5.2020 | 12.5.2020   | 25.05.2020   | **tbd**   |
| Tests integrated in CI | Beginning | Beginning | Beginning | Beginning |
| Postman Testing | 27.05.2020 | 27.05.2020 | End of semester | 25.06.2020 |


## 12.	Risks, Dependencies, Assumptions, and Constraints
| Risk | Mitigation Strategy	| Contingency (Risk is realized) |
|---|---|---|
| Unexpected failures in production | Cover as much scenarios as possible, Logging | Look into logs and fix the bug, Roll back version if necessary |
## 13. Management Process and Procedures

