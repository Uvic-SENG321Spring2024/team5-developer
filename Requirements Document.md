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
| Iteration II Draft | 2024-02-16 | Initial layout for Iteration II | 2.0 |

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
   * [4.3 Design and Implmentation Constraints](#43-design-and-implmentation-constraints)
   * [4.4 Assumptions and Dependencies](#44-assumptions-and-dependencies)

- [5. System Features](#5-system-features)
   * [5.1 \[System Feature 1 Name\]](#51-system-feature-1-name)
   * [5.2 Assign a Complaint](#52-assign-a-complaint)

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

#### **5.1 \[System Feature 1 Name\]**

Sample Text

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

Table 5.2.2: Functional Requirements for “assign a complaint” feature.

#### 5.2.2 Associated Use Cases
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

#### 5.2.1 Use Case Diagram: Assigning a Complaint

<p = align="center">
<img width="830" alt="Assign  use case diagram" src="https://github.com/Uvic-SENG321Spring2024/team5-developer/assets/101749612/f331deab-c1d9-481b-81b8-9ce8a33e8f5c">
</p>

## 6. Data Requirements

#### **6.1 Logical Data Model**

Sample Text

#### **6.2 Data Dictionary**

Sample Text

#### **6.3 Data Acquisition, Integrity, Retention, and Disposal**

Sample Text

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



## 9. Appendix

#### **9.1 Glossary of Terms**

| Term | Definition |
| ---- | ---------- |
| CPBC | Consumer Protection British Columbia. |
| Investigator | The CPBC employee who examines and determines a resolution for the consumer complaint they are assigned to. Each investigator is part of a specific department, where each department handles a specific category of complaints. |
| Iris | Software system used to input and store consumer complaints and their resolution status. |
| LIO | Licensing Information Officer; the CPBC employee who first logs a consumer complaint. |
| SysAid | Software system used to keep track of tickets and assign them to the relevant staff. |
| Ticket | A task that needs to be completed in order for a complaint to be resolved. |

