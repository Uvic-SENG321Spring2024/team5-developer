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
   * [5.2 \[System Feature 2 Name\]](#52-system-feature-2-name)

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


#### **5.2 \[System Feature 2 Name\]**

Sample Text

## 6. Data Requirements

#### **6.1 Logical Data Model**

Sample Text

#### **6.2 Data Dictionary**

The system uses two large data structures, each to interface with one of the two existing pieces of software:

   1. For **Iris**, the *Complaint Object*
   2. For **SysAid**, the *Ticket Object*

Given that the system acts as a layer to mesh these two pieces of software together, any input from users must have the appropriate data type, length, and format expected by the pre-existing software. These parameters are described in the following **Data Dictionary**. The specifications for all primitives must be followed strictly to prevent errors when data is transferred to the existing software. Specifications are based on the limitations of the current software and cannot be altered by our implementation.

Note that the **Allowed Values** field is omitted for drop-down menus with a predefined set of options. These options are already present within the pre-existing software components, and will be scraped by the system to populate these menus.

The compatibility for different types of **Attachments** in both objects is already handled by the pre-existing software. These can be handled as raw data and passed directly from the system to the existing software as long as they are within the accepted file size.

#### **Complaint Object (Iris)**

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
| Attachments    | Attached documents or files relevant to the complaint                                     | Many      | “Add / Remove” buttons | 500 Mb                                 | Any filetype - handled as raw data | Attachment compatibility is handled by pre-existing software                          |
| Credit Amount  | Amount credited or refunded to the complainant                                            | Int       | $0.00                  | 32 bits                                | 0 - 232                            | —                                                                                     |
| Credit Date    | Date that the credit amount was given to the consumer                                     | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31     | —                                                                                     |
| Penalty Amount | Amount that the licensed business addressed by the complaint was fined                    | Int       | $0.00                  | 32 bits                                | 0 - 232                            | —                                                                                     |
| Penalty Date   | Date that the penalty amount was received by CPBC                                         | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31     | —                                                                                     |
| Status         | Current status of the complaint, used to mark whether the complaint is open or resolved   | String    | Drop-Down              | 8 chars                                | “Open”<br>“Resolved”               | —                                                                                     |
| Date Resolved  | Date that the complaint was marked as “Resolved”                                          | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31     | Autofilled with current date when status is set to “Resolved”                         |

#### **Ticket Object (SysAid)**

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
| Attachments    | Attached documents or files relevant to the complaint                                                  | Many      | “Add / Remove” buttons | 1000 Mb                                | Any filetype - handled as raw data        | Attachment compatibility is handled by pre-existing software                          |
| Due Date       | Date that the ticket must be resolved by                                                               | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31            | —                                                                                     |
| Street         | Street of the complainant                                                                              | String    | Text Field             | 50 chars                               | ASCII Characters                          | —                                                                                     |
| Postal Code    | Postal or ZIP code of the complainant                                                                  | String    | Text Field             | 10 chars                               | ASCII Characters                          | —                                                                                     |
| Comments       | Additional comments made by the complainant not suitable for description box                           | String    | Text Field             | 1000 chars                             | ASCII Characters                          | —                                                                                     |
| Respondent     | Name of the licensed business addressed by the complaint, retrieved from CPBC’s database               | String    | Drop-Down              | 100 chars                              | *Scraped from existing software*          | —                                                                                     |
| Business Type  | Type of business addressed by the complaint                                                            | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*          | —                                                                                     |
| Created By     | Name of the LIO that created the complaint                                                             | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*          | Will usually be filled by the name of the LIO currently signed into the system        |
| Reviewed By    | Name of the LIO supervisor that reviewed the complaint                                                 | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*          | —                                                                                     |
| Date Opened    | The date the complaint was created                                                                     | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31            | Automatically filled when a new complaint is created in Iris                          |
| Nature         | The act violated or relevant to the complaint                                                          | String    | Drop-Down              | 50 chars                               | *Scraped from existing software*          | —                                                                                     |
| Description    | Open-ended description box for use at discretion of LIOs and Investigators to add details              | String    | Text Field             | Dynamically allocated up to 3000 chars | ASCII Characters                          | Investigators use this field later to add information on how a complaint was resolved |
| Attachments    | Attached documents or files relevant to the complaint                                                  | Many      | “Add / Remove” buttons | 500 Mb                                 | Any filetype - handled as raw data        | Attachment compatibility is handled by pre-existing software                          |
| Credit Amount  | Amount credited or refunded to the complainant                                                         | Int       | $0.00                  | 32 bits                                | 0 - 232                                   | —                                                                                     |
| Credit Date    | Date that the credit amount was given to the consumer                                                  | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31            | —                                                                                     |
| Penalty Amount | Amount that the licensed business addressed by the complaint was fined                                 | Int       | $0.00                  | 32 bits                                | 0 - 232                                   | —                                                                                     |
| Penalty Date   | Date that the penalty amount was received by CPBC                                                      | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31            | —                                                                                     |
| Status         | Current status of the complaint, used to mark whether the complaint is open or resolved                | String    | Drop-Down              | 8 chars                                | “Open”<br>“Resolved”                      | —                                                                                     |
| Date Resolved  | Date that the complaint was marked as “Resolved”                                                       | Int       | YYYY-MM–DD             | 32 bits                                | 1900-01-01<br>to<br>2999-12-31            | Autofilled with current date when status is set to “Resolved”                         |

#### **6.3 Data Acquisition, Integrity, Retention, and Disposal**

Sample Text

## 7. External Interface Requirements

#### **7.1 User Interfaces**

Sample Text

#### **7.2 Hardware Interfaces**

Sample Text

#### **7.3 Software Interfaces**

Sample Text

#### **7.4 Communication Interfaces**

Sample Text

## 8. Software Quality Attributes

Sample Text

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

