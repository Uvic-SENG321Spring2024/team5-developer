<p = align="center">
   <img src="https://www.consumerprotectionbc.ca/wordpress/wp-content/themes/consumerprotectionbc/images/logo.png" width="30%">
<p>

<h1 align="center"> Requirements Document - Consumer Protection BC </h1>

## Revision History

| Name | Date | Reason for Changes | Version |
| ----------- | ----------- | ------------- | ---------- | 
| Initial Draft | 2024-01-30 | Document created | 1.0 |
| Overview | 2024-01-31 | Overview section created | 1.1 |
| Rough Draft | 2024-02-02 | Added sections 2 - 4 | 1.2 |
| Iteration I Final | 2024-02-04 | Final edit | 1.3 |
| Client Review | 2024-02-13 | Edits according to feedback from clients | 1.3.1 |
| Iteration II Started | 2024-02-16 | Initial layout for Iteration II | 2.0 |
| Rough Draft | 2024-02-17 | Added sections 5 - 8 | 2.1 |
| Revision | 2024-02-18 | Group review on sections 5 - 8 | 2.2 |
| Iteration II Final | 2024-02-18 | Iteration II Completed | 2.3 |

## Table of Contents

- [1. Overview](#1-overview)

- [2. Business Requirements](#2-business-requirements)
   * [2.1 Background](#21-background)
   * [2.2 Business Opportunity](#22-business-opportunity)
   * [2.3 Business Objectives](#23-business-objectives)
   * [2.4 Success Metrics](#24-success-metrics)
   * [2.5 Product Vision Statement](#25-product-vision-statement)

- [3. Scope and Limitations](#3-scope-and-limitations)
   * [3.1 Major Features](#31-major-features)
   * [3.2 Project Scope](#32-project-scope)
   * [3.3 Limitations and Exclusions](#33-limitations-and-exclusions)

- [4. Context Description](#4-context-description)
   * [4.1 User Classes and Characteristics](#41-user-classes-and-characteristics)
   * [4.2 Operating Environment](#42-operating-environment)
   * [4.3 Design and Implementation Constraints](#43-design-and-implementation-constraints)
   * [4.4 Assumptions and Dependencies](#44-assumptions-and-dependencies)

- [5. System Features](#5-system-features)
   * [5.1 Create a Complaint](#51-create-a-complaint)
   * [5.2 Assign a Complaint](#52-assign-a-complaint)
   * [5.3 Update the Status of a Complaint](#53-update-the-status-of-a-complaint)
   * [5.4 View a Complaint](#54-view-a-complaint)

- [6. Data Requirements](#6-data-requirements)
   * [6.1 Logical Data Model](#61-logical-data-model)
   * [6.2 Data Dictionary](#62-data-dictionary)
   * [6.3 Data Acquisition, Integrity, Retention, and Disposal](#63-data-acquisition-integrity-retention-and-disposal)

- [7. External Interface Requirements](#7-external-interface-requirements)
   * [7.1 User Interfaces](#71-user-interfaces)
   * [7.2 Hardware Interfaces](#72-hardware-interfaces)
   * [7.3 Software Interfaces](#73-software-interfaces)
   * [7.4 Communication Interfaces](#74-communication-interfaces)

- [8. Software Quality Attributes](#8-software-quality-attributes)

- [9. Appendix](#9-appendix)
   * [9.1 Glossary of Terms](#91-glossary-of-terms)
   * [9.2 List of Figures](#92-list-of-figures)
   * [9.3 List of Tables](#93-list-of-tables)

## 1. Overview

Consumer Protection BC (CPBC), a government organization in charge of business regulation and licensing, uses consumer complaints to ensure a fair marketplace. Consumers across the province are able to contact CPBC with their concerns about unfair business practices and in turn, the CPBC can conduct inspections and investigations.

The current complaint system is inefficient and prone to human error. It consists of two software programs called Iris and SysAid, where Iris is used to input and store complaints received from a consumer, and SysAid is used to create tickets in order for complaints to be resolved by CPBC staff. By using two systems to manage each consumer complaint, complaints are resolved unsatisfactorily slow. 

A simplification of the complaint process would lead to an increase in the number of complaints successfully resolved each quarter, higher consumer satisfaction, and higher work satisfaction from CPBC staff. By building a product that can effectively interface with both Iris and SysAid - CPBC’s required internal software - fallible manual processes can be reduced. Consumer complaints that are essential to CPBC and its role in maintaining a safe marketplace will be resolved faster and with fewer oversights.

The following document outlines CPBC's business objectives and requirements, the scope of this project, user classes for the product, and all assumptions and dependencies.

## 2. Business Requirements

#### **2.1 Background**
The existing procedure for submitting a complaint to CPBC is characterized by a significant reliance on manual processes, making it susceptible to human errors. The complaint submission process involves the utilization of two distinct software systems: Iris, where the LIO's file consumer complaints, and SysAid, where the complaint ticket is generated manually by employees. However, a notable discrepancy exists between these two systems, emphasizing the necessity for a more cohesive and streamlined approach. Implementing a refined process would not only alleviate stress for both users and employees but also mitigate errors by incorporating automation into the system.

#### **2.2 Business Opportunity**

For the employees of CPBC, integrating current complaint management systems such as IRIS and SysAid offers a chance to streamline government consumer protection processes effectively. Through automated permissions management, improved user experience, and comprehensive data analytics we can enhance efficiency and transparency, benefiting government agencies, businesses, and consumers. This presents an ideal avenue for technology providers to seize upon the rising demand for innovative solutions within the public sector.

#### **2.3 Business Objectives**

The proposed product is expected to address several challenges for CPBC in a measurable manner. The primary business objectives targeted by the solution include:

- Increase Process Efficiency by 25%. This will be quantified by tracking the time required to both submit a complaint and generate a corresponding ticket.
- Reduce Human Errors by 40%. This will be quantified by the number of errors (typos or misunderstandings) that are submitted to the existing error log.
- Increase Customer Satisfaction by 40%. This will be quantified by the positivity of surveys filled out after submitting a complaint.


#### **2.4 Success Metrics**

- Accuracy of Complaint Handling:
   * Indicator: 80% of complaints accurately handled and resolved.
   * Impact: Ensures consumer satisfaction and regulatory compliance.
 
- Efficiency in Workflow:
   * Indicator: Reduction in the time taken to process and resolve complaints by 40%.
   * Impact: Increases overall efficiency, minimizes delays, and enhances responsiveness.
 
- Employee Satisfaction:
   * Indicator: Consumer satisfaction ratings through surveys increased by 90%.
   * Impact: Reflects the success of the system in meeting user needs and expectations.
 
- Compliance with Regulations:
   * Indicator: Adherence to federal and provincial employee rights regulations.
   * Impact: Mitigates legal risks and ensures ethical business practices.
 
- Security and Access Control:
   * Indicator: Effective implementation of access permissions and data security measures.
   * Impact: Protects sensitive information, ensures data integrity, and builds stakeholder trust.
 
The success of the project is intertwined with these indicators, which collectively contribute to achieving positive outcomes and meeting organizational objectives. The greatest impact on success lies in a holistic approach that considers both internal and external factors, aligning the project with the organization's overarching goals and regulatory requirements.

#### **2.5 Product Vision Statement**

The new product's vision is to revolutionize government consumer protection processes by seamlessly integrating existing complaint management systems, fostering efficiency, transparency, and accountability. Through innovative technology solutions, the new product aspire to empower government agencies by creating a harmonized ecosystem where complaints are swiftly addressed, trust is bolstered, and satisfaction is paramount. The following diagram illustrates this proposed process:

#### 2.5.1 Product Diagram

<p align="center">
   <img width="523" alt="Product Diagram" src="https://github.com/Uvic-SENG321Spring2024/team5-developer/assets/101749612/dd522fe6-d7f7-4aad-b2c9-13b2ad79119c">
</p>

## 3. Scope and Limitations

#### **3.1 Major Features**

The current system contains two major features: the complaints module and the ticketing system. The complaints module, located within the Iris program, allows LIOs to log, manage, and resolve complaints filed by consumers. These complaints are then stored within Iris’ database indefinitely, and may be accessed at a future time. The ticketing system, SysAid, allows LIOs to internally track and update progress on complaints filed within Iris.

The new product will interconnect these two features into one interface. This interface will allow LIOs to file, manage, track, and resolve complaints and tickets using only one system. Complaints and tickets will remain accessible within Iris and SysAid respectively.

#### **3.2 Project Scope**

The purpose of the new product is to connect Iris' complaints database and SysAid's ticketing system into one interface. This interface will reduce time spent by each LIO when creating, assigning, updating, and resolving complaints. Additionally, this interface will notify each assignee of a complaint when the complaint they are assigned to is updated or resolved.

#### **3.3 Limitations and Exclusions**

The following limitations are imposed on the system:
- No source code is available for the SysAid ticketing module.
- Source code for the Iris complaints module cannot be modified.
- Since data is confidential, developers must have the necessary permissions to access the two systems.

The system has no exclusions.

## 4. Context Description

#### **4.1 User Classes and Characteristics**

Based on information collected during interviews with Consumer Protection BC, three main user classes have been identified. These user classes—Licensing Information Officers (LIOs), LIO Supervisors, and Investigators—form the core team responsible for managing and resolving consumer complaints.

1. **Licensing Information Officers (LIOs):** LIOs drive the complaint resolution process by interacting with consumers, managing complaints, and ensuring secure and accurate handling of consumer details.
   - ***Usage Frequency:*** High
   - ***System Interactions:*** LIOs primarily use the system for complaint intake and management, inputting consumer details, and initiating the resolution process.
   - ***Technical Expertise:*** Moderate. LIOs are responsible for interacting with the complaint module of Iris and must ensure accurate input of consumer details.
   - ***Privilege Level:*** LIOs have access to all personal information and complaint details within Iris. They have limited access to fields handled by LIO Supervisors.

2. **LIO Supervisors:** LIO Supervisors supervise LIOs, oversee the system, assign complaints to different Investigators, and have higher-level access.
   - ***Usage Frequency:*** Moderate.
   - ***System Interactions:*** Supervisors primarily interact with the system by assigning tickets created by LIOs to investigators, done within Iris.
   - ***Technical Expertise:*** Moderate. Supervisors interact with the software system on a lower frequency than LIOs, but must review information present in the system to make workflow decisions.
   - ***Privilege Level:*** Supervisors have similar access levels as LIOs, but have the added ability to review and assign tickets to an appropriate Investigator.

3. **Investigators:** Investigators exist within several departments. They handle complaint resolution by examining the laws covered by CPBC. They utilize information from the system for investigations and complete tickets by providing information about how a complaint was resolved.
   - ***Usage Frequency:*** High during complaint resolution.
   - ***System Interactions:*** Investigators are assigned to examine and resolve complaints that they receive as a ticket through SysAid. They also interact with Iris by completing additional fields relating to how a complaint was eventually resolved.
   - ***Technical Expertise:*** Moderate. The primary job of Investigators lies outside the system in examining complaints and how they relate to relevant laws. However, Investigators must be able to understand the ticketing system and reliably provide it with accurate information.
   - ***Privilege Level:*** Investigators can only see tickets assigned to their specific department, and have only view-access to information relevant to their investigation. They have write-access for resolution-related fields to allow tickets to be closed.

While all three user classes interact with the system as a vital part in the complaint resolution process, LIOs will be held as a *prioritized user class* throughout development. This is because LIOs are the primary point of contact with the new system, and as such should be considered first when developing new features.

**Consumer Exclusion:** 

Note that consumers do not constitute a user class within the system. Consumers do not interact with the system interface, and no features will be developed with their needs in mind. Therefore, while consumers will be affected by the system, they will not be directly considered in its development. 

#### **4.2 Operating Environment**

The environment in which the product operates is as follows:
- The software must run on a Windows machine and be accessible from a desktop computer provided by the company. No mobile functionality is needed. 
- The software must coexist and directly interface with the complaint module within Iris.
- The software must also coexist and directly interface with the SysAid ticketing system. 

#### **4.3 Design and Implementation Constraints**

When designing and implementing of the product, developers have a few limitations when implementing the product. Firstly, the developer must create a product to run on a Windows machine. The product has to communicate between Iris and SysAid, two different systems. It must communicate the information inputted into Iris to SysAid. Consumer Protection BC requires it to keep both applications due to Iris not having a ticketing system. Finally, account permissions and overall security of information being sent from Iris to SysAid must be kept secure, private and maintained through the automated process of transferring information.

#### **4.4 Assumptions and Dependencies**

The project’s dependency on two pre-existing third-party software systems could affect the defined requirements. 

One assumption being made is how Iris and SysAid function and how they are utilized by CPBC. The current understanding of their usage is that information is manually input into each system using pre-defined fields. Iris's complaint module consists of a database of previous and current complaints that can be updated by LIOs. The information that LIOs upload into Iris is more granular, and there are specific fields that can be filled out. SysAid is used for its ticketing capabilities and notification system, since Iris does not have the capability to notify investigators when they are assigned to a complaint. SysAid collects more generic information-- many of the details that get a specific field in Iris do not have a corresponding field in SysAid and are instead included in the Description field. However, SysAid allows LIOs to define the impact and priority of the complaint. If the assumptions about how the two different systems are used in conjunction with each other are incorrect or change, it may result in requirements needing to be adjusted.

The only part of Iris’ system that the product will interact with is the complaint module. If this information is inaccurate, it will change the requirements.

Additionally, CPBC has access to the source code for Iris, but they do not have source code for SysAid. The product will need to automate the process of putting information into both Iris and SysAid. The dependency on SysAid and any limitations caused by a lack of access to source code may also necessitate changes to the requirements.

## 5. System Features
#### 5.0.0: Use Case Diagram
<p align="center">
   <img width="795" alt="Use Case Diagram" src="https://github.com/Uvic-SENG321Spring2024/team5-developer/assets/101749612/591238b6-916f-42e1-944b-b259049b77e6">
   <br>
   <i>Figure 5.0.0: Use case diagram for the system. This diagram shows the abilities of each user. The LIOs can create, update, and view a complaint. Supervisors can create, assign, update, and view a complaint. Investigators can update and view a complaint. The diagram also illustrates the communications between the 3 users and the pre-existing Iris and SysAid databases.</i>
</p>



#### **5.1 Create a Complaint**

The “create a complaint” feature is a high-priority feature. An LIO uses the “create a complaint” feature to create a new complaint in Iris and a corresponding ticket in SysAid. The LIO must be able to input all of the relevant complaint information into the system.

#### 5.1.1 Functional Requirements

Table 5.1.1 describes the functional requirements for the "create a complaint" feature:
| ID      | Requirement                                                |
|---------|------------------------------------------------------------|
| REQ-1   | The system shall allow an LIO to create a new complaint. <br><br> **Rationale:** The client's RFP states that LIOs create complaints. <br> **Acceptance Test:** An LIO is able to access and use the "create a complaint" feature.|
| REQ-2   | The system shall allow a Supervisor to create a new complaint. <br><br> **Rationale:** The client's RFP states that Supervisors create complaints. <br> **Acceptance Test:** A Supervisor is able to access and use the "create a complaint" feature.  |
| REQ-3   | The system shall not allow an Investigator to create a new complaint. <br><br> **Rationale:** Investigators do not create complaints, determined through elicitation with the client. <br> **Acceptance Test:** There is no possible way for an investigator to access or use the "create a complaint" feature.   |
| REQ-4   | The system shall open a new complaint in the Iris database when an LIO or Supervisor creates a complaint. <br><br> **Rationale:** The client's RFP states that the system will still interface with Iris, and during the initial client interview it was stated that complaints must still be stored within Iris. <br> **Acceptance Test:** When an LIO or Supervisor creates a complaint, the complaint is added to and is visible in Iris' database.  |
| REQ-5   | The system shall create a ticket in the SysAid database when an LIO or Supervisor creates a complaint. <br><br> **Rationale:** The client's RFP states that the system will still interface with SysAid. <br> **Acceptance Test:** When an LIO or Supervisor creates a complaint, a ticket containing the same information is created and visible in SysAid.  |
| REQ-6   | The system shall allow an LIO or Supervisor to fill in the following required complaint information fields: Complainant Information, Respondent, Business Type, Act Violated, Description, File Attachments <br><br> **Rationale:** The client's RFP states that complaints filed into Iris and tickets created in SysAid have fillable fields, therefore the system must have input fields for complaints. <br> **Acceptance Test:** Information input into the "create a complaint" feature is visible in the corresponding complaint in Iris.  |
| REQ-7   | The system shall allow an LIO or Supervisor to add file attachments which do not exceed 25 MB in size. <br><br> **Rationale:** Attaching files is a functionality that was broguht up during the initial client elicitation interview. <br> **Acceptance Test:** Can not attach files which exceed 25 MB in size. The linked attachments must be visible in the corresponding complaint in Iris. |
| REQ- 8  | If an LIO or Supervisor attaches a file attachment which exceeds 25 MB in size, the system shall not attach the oversized file to the complaint.  <br><br> **Rationale:** Attaching files which exceed 25 MB in size may cause the Iris database to run out of storage space. <br> **Acceptance Test:** Attaching a file which exceeds 25 MB in size does not allow the LIO or Supervisor to complete the complaint creation process. |
| REQ-9   | If an LIO or Supervisor inputs improperly formatted information into a complaint information field, the system shall notify the LIO or Supervisor that the inputted information is improperly formatted. <br><br> **Rationale:** The client-provided System Details document shows the specific accepted input type and format of each fillable field in Iris and SysAid.<br> **Acceptance Test:** An error message is received when an LIO or Supervisor puts information into the system in the wrong format.  |
| REQ-10   | If an LIO or Supervisor inputs improperly formatted information into a complaint information field, the system shall not create a new complaint until the inputted information fields are properly formatted. <br><br> **Rationale:** The business objective “Reduce Human Errors by 40%” in section 2.3 refers to reducing submission errors. <br> **Acceptance Test:** The system will not accept complaint submissions with complaint input information formatting errors.|
| REQ-11    | If the Complainant has previously filed a complaint, the system shall allow the LIO or Supervisor to autofill the Complainant Information. <br><br> **Rationale:** The client-provided System Details document states that there is a database of previous complainants.  <br> **Acceptance Test:** When creating a complaint for a complainant who has previously filed a complaint, the LIO or Supervisor does not need to fill in the complainant’s information; instead, it is automatically filled into each complaint information field.

#### 5.1.2 Associated Use Cases

Table 5.1.2 outlines the primary use case associated with the "create a complaint" feature:

| Use Case 1        | LIO Creating Complaint                     |
|-------------------|--------------------------------------------|
|**Primary Actor**  | LIO                                         |
|**Description**    | The LIO creates a new complaint after a consumer provides the LIO with the necessary information to investigate a BC Consumer Protection law or regulation violation.|
|**Trigger**        | Consumer contacts BC Consumer Protection to file a complaint. |
|**Preconditions**  | 1. LIO's identity is authenticated within the system. |
|**Postconditions** | 1. The complaint and its contents are stores in the Iris database. <br> 2. The corresponding ticket for the complaint is stored in the SysAid database. |
|**Normal Flow**    | 1. LIO inputs the following information into the complaint: Complainant Information, Respondent, Business Type, Created By, Reviewed By, Nature, Description, File Attachments, Impact, Priority<br> 2. LIO confirms information and creates the complaint.|
|**Alternate Flow** | If the Complainant has filed a complaint before: The system autofills the Complainant Information section of the complaint.|
|**Exceptions**     | For all input fields: If the input format is incorrect, the system notifies the LIO and does not create a complaint until issues are resolved.|
|**Priority**       | High |

#### 5.1.1: Use Case Diagram for Creating Complaint
  
<p align="center">
  <img width="698" alt="create" src="https://github.com/Uvic-SENG321Spring2024/team5-developer/assets/101749612/b60f418f-06f6-4f14-9347-07ec84b771fb">
   <br><i>Figure 5.2.1: Use case diagram for creating a new complaint </i>
</p>

Figure 5.1.1 is a visual representation of the use case defined in Table 5.1.2.

### 5.2 Assign a Complaint

The “assign” feature is a high-priority feature. Supervisors use the “assign” feature to assign an Investigator to a complaint under investigation.  

#### 5.2.1 Functional Requirements  

Table 5.2.1 describes the functional requirements for the “assign a complaint” feature:

| ID      | Requirement                                                |
|---------|------------------------------------------------------------|
| REQ-12  | The system shall allow a Supervisor to assign an Investigator to a complaint. <br><br>**Rationale:** The client elicitation interviews state that only Supervisors can assign Investigators to a complaint. <br> **Acceptance Test:** Supervisors may use the “assign” feature to assign an Investigator to a complaint.|
| REQ - 13 | The system shall not allow an LIO to assign an Investigator to a complaint. <br><br> **Rationale:** The client elicitation interviews state that only Supervisors can assign Investigators to a complaint. <br> **Acceptance Test:** No possible way for an LIO to assign an Investigator to a complaint. |
| REQ - 14 | The system shall not allow an Investigator to assign an Investigator to a complaint. <br><br> **Rationale:** The client elicitation interviews state that only Supervisors can assign Investigators to a complaint. <br> **Acceptance Test:** No possible way for an Investigator to assign an Investigator to a complaint. |
| REQ - 15 | When a Supervisor assigns an Investigator to a complaint, the system shall assign the specified Investigator to the corresponding ticket within the SysAid database. <br><br> **Rationale:** The client’s System Details document states that SysAid has an Assigned To field that must be filled with the assigned Investigator. <br> **Acceptance Test:** After a Supervisor assigns an Investigator to a complaint, the Investigator must be assigned to the corresponding ticket in the SysAid database. |
| REQ - 16 | When a Supervisor assigns an Investigator to a complaint, the system shall assign the specified Investigator to the corresponding complaint within the Iris database. <br><br> **Rationale:** The client’s System Details document states that Iris has an Investigator field that must be filled with the assigned Investigator. <br> **Acceptance Test:** After a Supervisor assigns an Investigator to a complaint, the Investigator must be assigned to the corresponding complaint in the Iris database. |
| REQ - 17 | If a Supervisor assigns an unknown Investigator to a complaint, the system shall notify the Supervisor that the Investigator cannot be found. <br><br> **Rationale:** The complaint should not be assigned to a non-existent Investigator. <br> **Acceptance Test:** Inputting an unknown Investigator prompts an error to the Supervisor. |
| REQ - 18 | If a Supervisor assigns an unknown Investigator to a complaint, the system shall not assign the unknown Investigator to the specified complaint. <br><br> **Rationale:** The complaint should not be assigned to a non-existent Investigator. <br> **Acceptance Test:** The unknown Investigator is not assigned to the ticket in the SysAid database. The unknown Investigator is not assigned to the complaint in the Iris database. |

#### 5.2.2 Associated Use Cases

Table 5.2.2 outlines the primary use case for the “assign a complaint” feature.

| Use Case 2 | Supervisor Assigning Complaint |
|-------------------|--------------------------------------------|
**Primary Actor** | Supervisor
**Description** | The Supervisor assigns a complaint to an Investigator.
**Trigger** | A complaint has been filed but is unassigned.
**Preconditions** | - Supervisor’s identity is authenticated within the system <br> - There exists a complaint without an assigned Investigator.
**Postconditions** | - The complaint in Iris has the updated information. <br> - The ticket in SysAid has the updated information. <br> - The Investigator has been notified of a new assigned ticket.
**Normal Flow** | - Supervisor views an existing complaint. <br> - Supervisor inputs the assigned Investigator into the Investigator field of the complaint. <br> - The system automatically fills in the Department field of the complaint with the department associated with the assigned Investigator. <br> - Supervisor confirms the change.
**Alternate Flow** | None
**Exceptions** | - If the Investigator being assigned does not exist: The system notifies the Supervisor, does not assign the unknown Investigator to the complaint, and does not allow the change to be confirmed or saved.
**Priority** | High

#### 5.2.1 Use Case Diagram for Assigning Complaint

<p = align="center">
   <img width="507" alt="assign" src="https://github.com/Uvic-SENG321Spring2024/team5-developer/assets/101749612/dd6b9ac3-8779-4b2a-a61e-6ac42e99e276">
   <br>
   <i>Figure 5.2.1: Use case diagram for assigning a complaint </i>
</p>

Figure 5.2.1 is a visual representation of the use case defined in Table 5.2.2.

### 5.3 Update the Status of a Complaint

The “update the status of a complaint” feature is a high-priority feature. An LIO will be able to use the feature to add new information to a complaint. An Investigator will be able to use the feature to document the investigation and resolution of a complaint.  

#### 5.3.1 Functional Requirements

Table 5.3.1 describes the functional requirements for the “update the status of a complaint” feature:  

| ID      | Requirement                                                |
|---------|------------------------------------------------------------|
| REQ-19 | The system shall allow the following user-classes to update the status of a complaint: LIO, Supervisor, and Investigator. <br><br> **Rationale:** Elicitation with client defined LIOs, Supervisors, and Investigators as primary users of the system. <br> **Acceptance Test:**  LIOs, Supervisors, and Investigators can access the "update a complaint" feature. |
| REQ-20 | The system shall allow an LIO, Supervisor, or Investigator to update the following complaint information fields of a complaint: <br> - Complainant's First Name <br> -  Complainant's Last Name <br> -  Complainant's Email Address <br> -  Complainant's Phone Number <br> -  Complainant's Address (including: Street, City, Province, Postal Code, Country) <br> - Complainant Comments <br> - Respondent (licensed business) <br> - Business Type <br> - Act Violated <br> - Description <br> - File Attachments <br> - Resolution Status <br> - Amount Credited or Refunded to Consumer <br> - Date of Credit or Refund to Consumer <br> - Penalty Amount for Respondent <br> - Penalty Payment Received Date <br> - Status of Complaint (Open, Resolved) <br><br> **Rationale:** The information fields listed above are required to create a complaint within the Iris database and a corresponding ticket within the SysAid database. <br> **Acceptance Test:** An LIO, Supervisor, or Investigator is able to update the complaint by editing each complaint information field. |
| REQ-21 | The system shall update the corresponding complaint’s contents in the Iris database when a complaint is updated. <br><br> **Rationale:** The client's Request for Proposal states complaints must be stored within the Iris database.<br> **Acceptance Test:** The corresponding complaint in Iris contains the updated information. |
| REQ-22 | The system shall update the corresponding ticket’s status in the SysAid database when a complaint is updated. <br><br> **Rationale:** The client's Request for Proposal states tickets which correspond to a complaint must be stored within the SysAid database. <br> **Acceptance Test:** The corresponding ticket in SysAid contains the updated information. |
| REQ-23 | If an LIO or Supervisor inputs improperly formatted information while updating a complaint information field, the system shall notify the LIO or Supervisor that the information is improperly formatted. <br><br> **Rationale:** The business objective “Reduce Human Errors by 40%” in section 2.3 refers to reducing submission errors. <br> **Acceptance Test:** An error message is displayed when a field is changed to have incorrectly formatted information. |
| REQ-24| If an LIO or Supervisor inputs improperly formatted information into a complaint information field, the system shall not update the complaint until the information fields are properly formatted. <br><br> **Rationale:** The business objective “Reduce Human Errors by 40%” in section 2.3 refers to reducing submission errors. <br> **Acceptance Test:** When a field is changed to have incorrectly formatted information, the system will not allow the changes to be saved.

<p align="center">
   <i>
      Table 5.3.2: Functional Requirements
   </i>
</p>

#### 5.3.2 Associated User Stories

The following user stories describe the functional requirements associated with the “update” feature:
- As an LIO, I want to update an existing complaint’s contents with additional information that was provided by the Complainant.
- As an Investigator, I want to update a complaint I am investigating with my final resolution for the complaint.

### 5.4 View a Complaint

The “view” complaint is a high-priority feature. An Investigator needs to be able to view the contents of a complaint to inform their investigations. An LIO needs to be able to view the complaint resolution.  

#### 5.4.1 Functional Requirements

Table 5.4.1 describes the functional requirements for the “view a complaint” feature:
| ID      | Requirement                                                |
|---------|------------------------------------------------------------|
| REQ-25 | The system shall allow the following user-classes to view the contents of a complaint: LIO, Supervisor, and Investigator. <br><br> **Rationale:** Elicitation with client defined LIOs, Supervisors, and Investigators as primary users of the system.<br> **Acceptance Test:** LIOs, Supervisors, and Investigators can access the "view a complaint" feature. |
| REQ-26 | When an Investigator is selecting a complaint to view, the system shall strictly display complaints that are assigned to the Investigator. <br><br> **Rationale:** Elicitation with clients revealed that each Investigator does not require access to complaints they are not assigned to. <br> **Acceptance Test:** An Investigator is not able to view complaints that they are not assigned to. |
| REQ-27 | When an Investigator is selecting a complaint to view, the system shall prioritize displaying complaints that are currently under investigation over complaints that have already been resolved. <br><br> **Rationale:** One of the client's business objectives is to increase efficiency, therefore only displaying relevant complaints will reduce time spent by Investigators searching for relevant complaints.<br> **Acceptance Test:** Complaints which are in-progress are prioritized and displayed before complaints that have been resolved. |
| REQ-28 | When an Investigator is selecting a complaint to view, the system shall prioritize displaying complaints that need urgent resolution over complaints that don’t require urgent resolution. <br><br> **Rationale:** Complaints that require urgent resolution should be easier to find in order to minimize the risk of them being sidelined or forgotten. <br> **Acceptance Test:** The complaints displayed to an Investigator should be sorted by urgency priority, with higher urgency complaints appearing first. |

<p align="center">
   <i>
      Table 5.4.2: Functional Requirements
   </i>
</p>

#### 5.4.2 Associated User Stories

The following user stories describe the functional requirements associated with the “view” feature:
- As an Investigator, I want to view the contents of a complaint that I am assigned to so I can determine the resolution for the complaint.
- As a Supervisor, I want to view the contents of a complaint to determine the current resolution status of the investigation for the complaint.
- As an LIO, I want to view the contents of a complaint to ensure the complaint contains all the necessary information provided by the Complainant.

## 6. Data Requirements

#### **6.1 Logical Data Model**

#### 6.1.1 Entity Relationship Diagram

<p align="center">
   <img width="523" alt="ERD" src="https://github.com/Uvic-SENG321Spring2024/team5-developer/assets/25752638/ec07ec2d-984d-4818-83e8-7f416a357f49">
   <br><i>Figure 6.1.1: ERD diagram. </i>
</p>

Figure 6.1.1 depicts the data relationships between the entities in the system. The multiplicity of each relationship is shown with a number or letter on the lines that connect entities and relationships, with "1" representing "one" and "M" representing "many." A line with "1 to M" or "M to 1" shows a one-to-many relationship, "M to M" is many-to-many, and "1 to 1" is one-to-one.

"Complaint Entry" refers to the entity that Supervisors create, assign, or update, LIOs create or update, and Investigators update. It is the layer that separates LIOs, Supervisors, and Investigators from Iris and SysAid. The Complaint Entry will accept input from LIOs, Supervisors, and Investigators. Then, the Complaint Entry interfaces with both Iris and SysAid to generate a native Iris complaint and a native SysAid ticket.

#### **6.2 Data Dictionary**

The system uses two large data structures, each to interface with one of the two existing pieces of software:

   1. For **Iris**, the *Complaint Object*
   2. For **SysAid**, the *Ticket Object*

Given that the system acts as a layer to mesh these two pieces of software together, any input from users must have the appropriate data type, length, and format expected by the pre-existing software. These parameters are described in the following **Data Dictionary**. The specifications for all primitives must be followed strictly to prevent errors when data is transferred to the existing software. Specifications are based on the limitations of the current software and cannot be altered by our implementation.

Note that the **Allowed Values** field is omitted for drop-down menus with a predefined set of options. These options are already present within the pre-existing software components, and will be scraped by the system to populate these menus.

The compatibility for different types of **Attachments** in both objects is already handled by the pre-existing software. These can be handled as raw data and passed directly from the system to the existing software as long as they are within the accepted file size.

#### 6.2.1 Complaint Object (Iris)

| Data Element   | Field Description                                                                         | Data Type                                                                                                        | Input Format | Length | Allowed Values | Additional Notes                             |
| ------------   | ----------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------ | ------ | -------------- | -------------------------------------------- |
| Complainant    | Holds all personal information of the consumer making the complaint                       | \+ First Name<br>\+ Last Name<br>\+ Email<br>\+ Phone<br>\+ Address<br>\+ Comments                               | —            | —      | —              | —                                            |
| Address        | Holds all details of the physical address of the complainant                              | \+ Street<br>\+ City<br>\+ Province<br>\+ Postal Code<br>\+ Country                                              | —            | —      | —              | —                                            |
| Resolution     | Holds all details related to the resolution of the complaint                              | \+ Credit Amount<br>\+ Credit Date<br>\+ Penalty Amount<br>\+ Penalty Date<br>\+ Status<br>\+ Date Resolved      | —            | —      | —              | —                                            |
| First Name     | First name of the complainant                                                             | String    | Text Field             | 50 chars                               | ASCII Characters                   | —                                                                                     |
| Last Name      | Last name of the complainant                                                              | String    | Text Field             | 50 chars                               | ASCII Characters                   | —                                                                                     |
| Email          | Email address of the complainant                                                          | String    | Text Field             | 50 chars                               | ASCII Characters                   | —                                                                                     |
| Phone          | Phone number of the complainant                                                           | String    | Text Field             | 15 chars                               | ASCII Characters                   | —                                                                                     |
| Country        | Country of the complainant                                                                | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*   | —                                                                                     |
| Province       | Province of the complainant                                                               | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*   | —                                                                                     |
| City           | City of the complainant                                                                   | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*   | —                                                                                     |
| Street         | Street of the complainant                                                                 | String    | Text Field             | 50 chars                               | ASCII Characters                   | —                                                                                     |
| Postal Code    | Postal or ZIP code of the complainant                                                     | String    | Text Field             | 10 chars                               | ASCII Characters                   | —                                                                                     |
| Comments       | Additional comments made by the complainant not suitable for description box              | String    | Text Field             | 1000 chars                             | ASCII Characters                   | —                                                                                     |
| Respondent     | Name of the licensed business addressed by the complaint, retrieved from CPBC’s database  | String    | Drop-Down              | 100 chars                              | *Scraped from existing software*   | —                                                                                     |
| Business Type  | Type of business addressed by the complaint                                               | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*   | —                                                                                     |
| Created By     | Name of the LIO that created the complaint                                                | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*   | Will usually be filled by the name of the LIO currently signed into the system        |
| Reviewed By    | Name of the LIO supervisor that reviewed the complaint                                    | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*   | —                                                                                     |
| Date Opened    | The date the complaint was created                                                        | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31     | Automatically filled when a new complaint is created in Iris                          |
| Nature         | The act violated or relevant to the complaint                                             | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*   | —                                                                                     |
| Description    | Open-ended description box for use at discretion of LIOs and Investigators to add details | String    | Text Field             | Dynamically allocated up to 3000 chars | ASCII Characters                   | Investigators use this field later to add information on how a complaint was resolved |
| Attachments    | Attached documents or files relevant to the complaint                                     | Many      | “Add / Remove” buttons | 25 Mb                                  | Any filetype - handled as raw data | Attachment compatibility is handled by pre-existing software                          |
| Credit Amount  | Amount credited or refunded to the complainant                                            | Int       | $0.00                  | 32 bits                                | 0 - 2<sup>32</sup>                 | —                                                                                     |
| Credit Date    | Date that the credit amount was given to the consumer                                     | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31     | —                                                                                     |
| Penalty Amount | Amount that the licensed business addressed by the complaint was fined                    | Int       | $0.00                  | 32 bits                                | 0 - 2<sup>32</sup>                 | —                                                                                     |
| Penalty Date   | Date that the penalty amount was received by CPBC                                         | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31     | —                                                                                     |
| Status         | Current status of the complaint, used to mark whether the complaint is open or resolved   | String    | Drop-Down              | 8 chars                                | “Open”<br>“Resolved”               | —                                                                                     |
| Date Resolved  | Date that the complaint was marked as “Resolved”                                          | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31     | Autofilled with current date when status is set to “Resolved”                         |

<br>

#### 6.2.2 Ticket Object (SysAid)

| Data Element   | Field Description                                                                                      | Data Type | Input Format           | Length                                 | Allowed Values                            | Additional Notes                                                                      |
| -------------- | ------------------------------------------------------------------------------------------------------ | --------- | ---------------------- | -------------------------------------- | ----------------------------------------- | ------------------------------------------------------------------------------------- |
| Category       | Category that the associated complaint falls under                                                     | String    | Drop-Down              | 15 chars                               | *Scraped from existing software*          | LIOs will always fill this drop-down with the “complaint” option                      |
| Status         | Current status of the ticket, used to mark whether the ticket is unaddressed, in progress or completed | String    | Drop-Down              | 12 chars                               | “Request”<br>“In Progress”<br>“Completed” | —                                                                                     |
| Impact         | Severity of the complaint. Up to the discretion of LIOs                                                | String    | Drop-Down              | 8 chars                                | “Low”<br>“Medium”<br>“High”               | —                                                                                     |
| Priority       | Priority of the complaint. Up to the discretion of LIOs                                                | String    | Drop-Down              | 8 chars                                | “Low”<br>“Medium”<br>“High”               | —                                                                                     |
| Title          | Name of the ticket                                                                                     | String    | Text Field             | 50 chars                               | ASCII Characters                          | —                                                                                     |
| Description    | Details about the task associated with the ticket                                                      | String    | Text Field             | Dynamically allocated up to 3000 chars | ASCII Characters                          | —                                                                                     |
| Request User   | Name of the LIO that created the ticket                                                                | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*          | —                                                                                     |
| Assigned To    | Name of the investigator assigned to the ticket by an LIO supervisor                                   | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*          | —                                                                                     |
| Attachments    | Attached documents or files relevant to the complaint                                                  | Many      | “Add / Remove” buttons | 50 Mb                                   | Any filetype - handled as raw data        | Attachment compatibility is handled by pre-existing software. SysAid is noted to have a larger filesize limit                          |                      
| Due Date       | Date that the ticket must be resolved by                                                               | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31            | —                                                                                     |

#### **6.3 Data Acquisition, Integrity, Retention, and Disposal**

Data Acquisition
- LIOs collect data via phone and email interactions with consumers, adhering to ethical standards and ensuring the secure acquisition of information. 
- LIOs confirm the accuracy and completeness of the data obtained, minimizing the risk of errors or inaccuracies. 
- By prioritizing ethical practices and implementing stringent security measures, the system maintains the trust and reliability of the acquired data, laying a solid foundation for effective complaint resolution and analysis.

Data Retention and Disposal
- Once the complaints have been resolved, the data is securely retained within Iris database in accordance with established retention policies. 
- Historical complaint records remain accessible for reference purposes, aiding in trend analysis, regulatory compliance, and quality assurance efforts.
- While the data is not disposed of, encryption and access controls are in place to protect it from unauthorized access or misuse, thereby upholding the trust and integrity of the complaint management system.

Data Integrity:
- The system must validate incoming data on a regular basis and make sure it is free from errors or inconsistencies.
- Sensitive data stored in the system should be encrypted to prevent unauthorized access or tampering.
- Encryption algorithms and key management protocols should comply with industry standards and best practices.


## 7. External Interface Requirements

#### **7.1 User Interfaces**

This section will be completed in the next iteration.

#### **7.2 Hardware Interfaces**

The product will run on a Windows machine which has at least Windows 11 Operating System. It will connect to the current Database, which will store the past, current and future data.

#### **7.3 Software Interfaces**

The product connects the SysAid and Iris systems, per each complaint made. As each complaint is created in Iris, then the data of the complaint is used to raise a ticket in SysAid, and afterwards when there is an update the data is updated to Iris.

#### **7.4 Communication Interfaces**

The product must communicate between SysAid and Iris on a windows machine. Iris must communicate a ticket in an electronic form to SysAid through the product and vice versa.  
When an electronic form is sent  to SysAid from Iris, the product must notify SysAid that a form was sent and give confirmation to Iris of a successful notification to SysAid. The same procedure must happen when the two systems are flipped, an electronic form is sent to Iris from SysAid.

## 8. Software Quality Attributes

#### 8.1.1 Criteria for Non-Functional Requirements

| Non-Functional Requirements | Acceptance Criteria |
| --------------------------- | ------------------- |
| Security | Each complaint must be secure and be seen by managers, the LIO’s that created the complaint and investigators the complaint is assigned to. Personal data must never be exposed. |
| Reusability | The product must be able to be reused 100% of the time when the product is up and running to make each complaint that the LIO wants without disruptions and complications. |
| Availability | The product must be available to communicate complaints 99.99% of the time of a year (less than 52 minutes of downtime in a year) when an LIO is requested to make a complaint. |
| Performance | The product must be able to have 1000 LIO’s create complaints concurrently while having no problem communicating the ticket between SysAid and Iris when an LIO is processing a ticket. |
| Efficiency | The product must be able to communicate information 99.99% of the time (less than 52 minutes of downtime in a year) between SysAid and Iris when an LIO submits a complaint. |
| Interoperability | The product must have a 99.99% (less than 52 minutes of downtime in a year) ability to exchange and make use of the information between Iris and SysAid. |
| Traceability | The product must be able to track where a complaint came from to where it was sent once assigned to an Investigator, within a minute. |
| Maintainability | The product must be able to deploy new features within 6 hours. |
| Usability | The product must be ascertainable within a week for managers to use when communicating the tickets between the LIO that made the complaint to the Investigator the complaint was assigned too. |

## 9. Analysis Models (Data Flow Diagrams, Sequence Diagram, Storyboard, Swimlane diagram, Decision Tree Diagram )

<p align="center">
   <img width="523" alt="DFD" src="https://github.com/Uvic-SENG321Spring2024/team5-developer/blob/437e69ee6729677c7805949a772135eb12395ffc/Analysis%20Models/DFD%20Level%200.png">
</p>


## 10. Appendix

#### **10.1 Glossary of Terms**

| Term | Definition |
| ---- | ---------- |
| CPBC | Consumer Protection British Columbia. |
| Investigator | The CPBC employee who examines and determines a resolution for the consumer complaint they are assigned to. Each investigator is part of a specific department, where each department handles a specific category of complaints. |
| Iris | Software system used to input and store consumer complaints and their resolution status. |
| LIO | Licensing Information Officer; the CPBC employee who first logs a consumer complaint. |
| SysAid | Software system used to keep track of tickets and assign them to the relevant staff. |
| Ticket | A task that needs to be completed in order for a complaint to be resolved. |

#### **10.2 List of Figures**
* 2\. Business Requirements
    * [2.5.1 Product Diagram](#251-product-diagram)
* 5\. System Features
    * 5\.0 Create a Complaint
        * [5.0.0 Use Case Diagram: Overall use Case Diagram](#500-use-case-diagram)
    * 5\.1 Create a Complaint
        * [5.1.1 Use Case Diagram: Creating a Complaint](#511-use-case-diagram-for-creating-complaint)
    * 5\.2 Assign a Complaint
        * [5.2.1 Use Case Diagram: Assigning a Complaint](#521-use-case-diagram-for-assigning-complaint)
* 6\. Data Requirements
    * [6.1.1 Entity Relationship Diagram](#611-entity-relationship-diagram)

#### **10.3 List of Tables**
* 5\. System Features
    * 5\.1 Create a Complaint
        * [5.1.1 Functional Requirements](#511-functional-requirements)
        * [5.1.2 Associated Use Cases](#512-associated-use-cases)
    * 5\.2 Assign a Complaint
        * [5.2.1 Functional Requirements](#521-functional-requirements)
        * [5.2.2 Associated Use Cases](#522-associated-use-cases)
    * 5\.3 Update the Status of a Complaint
        * [5.3.1 Functional Requirements](#531-functional-requirements)
    * 5\.4 View a Complaint
        * [5.4.1 Functional Requirements](#541-functional-requirements)
* 6\. Data Requirements
    * [6.2.1 Complaint Object (Iris)](#621-complaint-object-iris)
    * [6.2.2 Ticket Object (SysAid)](#622-ticket-object-sysaid)
* 8\. Software Quality Attributes
    * [8.1.1 Criteria for Non-Functional Requirements](#811-criteria-for-non-functional-requirements)
