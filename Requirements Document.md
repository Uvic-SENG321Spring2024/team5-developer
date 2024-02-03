<p = align="center">
   <img src="https://www.consumerprotectionbc.ca/wordpress/wp-content/themes/consumerprotectionbc/images/logo.png" width="30%">
<p>

<h1 align="center"> Requirements Document - Consumer Protection BC </h1>

## Revision History

| Name | Date | Reason for Changes | Version |
| ----------- | ----------- | ------------- | ---------- | 
| Initial Draft | 2024-01-30 | Document created | 1.0 |
| Overview | 2024-01-31 | Overview section created | 1.1 |
|  |  | | |
|  |  | | |

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

- [5. Appendix](#5-appendix)
   * [5.1 Glossary of Terms](#51-glossary-of-terms)
   * [5.2 References](#52-references)

## 1. Overview

As the provincial not-for-profit in charge of business regulation and licensing, Consumer Protection BC uses consumer complaints to ensure a fair marketplace. Customers across the province are able to contact CPBC with their concerns about unfair business practices and in turn, the CPBC can conduct inspections and investigations.

The current complaint system is inefficient and prone to human error. It consists of two software programs called Iris and SysAid, where Iris is used to input and store complaints received from a consumer, and SysAid is used to create tickets in order for complaints to be resolved by CPBC staff. By using two systems to manage one consumer complaint, complaints are resolved unsatisfactorily slow. 

A simplification of the complaint process would lead to higher consumer satisfaction, an increase in the number of complaints successfully resolved each quarter, and higher work satisfaction from CPBC staff. By building a product that can effectively interface with both Iris and SysAid - CPBC’s required internal software - fallible manual processes can be reduced. Consumer complaints essential to the CPBC and its role in maintaining a safe marketplace will be resolved faster and with fewer oversights.


## 2. Business Requirements

#### **2.1 Background**

#### **2.2 Business Opportunity**

#### **2.3 Business Objectives**

#### **2.4 Success Metrics**

#### **2.5 Product Vision Statement**

## 3. Scope and Limitations

#### **3.1 Major Features**
The current system contains two major features: the complaints module and the ticketing system. The complaints module, located within the Iris program, allows LIOs to log, manage, and resolve complaints filed by consumers. These complaints are then stored within Iris’ database indefinitely, and may be accessed at a future time. The ticketing system, SysAid, allows LIOs to internally track and update progress on complaints filed within Iris.

The new product will interconnect these two features into one accessible interface. This interface will allow LIOs to file, manage, track, and resolve complaints and tickets using only one system. Complaints and tickets will remain accessible within Iris and SysAid respectively.

#### **3.2 Project Scope**
The objectives of the new interface are to:
- Reduce the time spent by LIOs navigating between complaints and tickets modules.
- Improve efficiency while finding and referencing past and current filed complaints.
- Accurately manage complaints currently under investigation.
- Indefinitely store and access previously filed complaints.
- Assign investigators and LIOs to complaints.
- Assign investigators and LIOs to tickets.
- Keep track of progress on current tickets.
- Notify LIOs and investigators when tickets are updated and resolved.

#### **3.3 Limitations and Exclusions**
The following limitations are imposed on the system:
- No source code is available for the SysAid ticketing module.
- Source code for the Iris complaints module cannot be modified.
- Since data is confidential, developers must have the necessary permissions to access the two systems.
- The system must operate on Windows operating system.

## 4. Context Description

#### **4.1 User Classes and Characteristics**

Based on information collected during interviews with Consumer Protection BC, three main user classes have been identified. These user classes—LIOs, LIO Supervisors, and Investigatory Departments—form the core team responsible for managing and resolving consumer complaints.

1. **Licensing and Information Officers (LIOs):** LIOs drive the complaint resolution process by interacting with consumers, managing complaints, and ensuring secure and accurate handling of consumer details.
   - ***Usage Frequency:*** High
   - ***Usage Description:*** LIOs primarily use the system for complaint intake and management, inputting consumer details, and initiating the resolution process.
   - ***Technical Expertise:*** Moderate. LIOs are responsible for interacting with the complaint module of Iris and must ensure accurate input of consumer details.
   - ***Privilege Level:*** LIOs have access to all personal information and complaint details within Iris. They have limited access to fields handled by LIO Supervisors.

2. **LIO Supervisors:** LIO Supervisors oversee the system, assign complaints to different Investigatory Departments, manage workflow, and have higher-level access.
   - ***Usage Frequency:*** Moderate.
   - ***Usage Description:*** Supervisors primarily interact with the system by assigning tickets created by LIOs to the appropriate department, done within Iris.
   - ***Technical Expertise:*** Moderate. Supervisors interact with the software system on a lower frequency than LIOs, but must review information present in the system to make workflow decisions.
   - ***Privilege Level:*** Supervisors have similar access levels as LIOs, but have the added ability to review and assign tickets to the relevant Investigatory Department.

3. **Investigatory Departments:** Investigators handle complaint resolution by examining the laws covered by CPBC. They utilize information from the system for investigations and complete tickets by providing information about how a complaint was resolved.
   - ***Usage Frequency:*** High during complaint resolution.
   - ***Usage Description:*** Investigators are assigned to examine and resolve complaints that they receive in ticket form through SysAid. They also interact with Iris by completing additional fields relating to how a complaint was eventually resolved.
   - ***Technical Expertise:*** Moderate. The primary job of Investigators lies outside the system in examining complaints and how they relate to relevant laws. However, Investigators must be able to understand the ticketing system and reliably provide it with accurate information.
   - ***Privilege Level:*** Investigators can only see tickets assigned to their specific department, and have only view-access to information relevant to their investigation. They have write-access for resolution-related fields to allow tickets to be closed.

Based on the objectives of the system, none of the classes—Licensing and Information Officers (LIOs), LIO Supervisors, and Investigators—should be prioritized over another. All three user classes interact with the system as a vital part in the complaint resolution process, and therefore failing to address the needs of one class over another will prevent the system from meeting its objectives.

#### **4.2 Operating Environment**
The environment in which the product operates is as follows:
- The software must run on a Windows machine and be accessible from a desktop. No mobile functionality is needed. 
- The software must coexist and directly interface with the complaint module within Iris.
- The software must also coexist and directly interface with SysAid’s ticketing system. 

#### **4.3 Design and Implmentation Constraints**
Through the design and implementation of the product, developers have a few limitations when implementing the product. Firstly, developers are required to make the product only run on a Windows machine and nothing else. The product has to communicate between Iris and SysAid, two different applications. It must communicate the information inputted into Iris to SysAid because Consumer Protection BC requires it to keep both applications due to Iris not having a ticketing system. Finally, account permissions and overall security of information being sent from Iris to SysAid must be kept secure, private and maintained through the automated process of transferring information.

#### **4.4 Assumptions and Dependencies**
The ways that Iris and SysAid function as individual systems and how they are utilized is one assumption that may affect requirements if it is incorrect. The current understanding of their usage is that information is manually input into each system using pre-defined fields. Iris consists of a database of previous and current complaints that can be updated by users, and collects more granular information about the complaint in specific fields. SysAid is used primarily for its ticketing capabilities and notification system, since Iris does not have the capability to notify investigators when they are assigned to a complaint. It collects more generic information, and also allows LIOs to define the impact and priority of the complaint. If the assumptions about how the two different systems are used in conjunction with each other are incorrect or change, it may result in requirements needing to be adjusted.

The only part of Iris’ system that the product will interact with is the complaint module, and the only part of SysAid’s system that will be interfaced with is the ticketing system. If this information is inaccurate, it will change the requirements.

## 5. Appendix

#### **5.1 Glossary of Terms**

| Term | Definition |
| ---- | ---------- |
| CPBC | Consumer Protection British Columbia. |
| Iris | Software system used to input and store consumer complaints and their resolution status. |
| LIO | Licensing Information Officer; the CPBC employee who first logs a consumer complaint. |
| SysAid | Software system used to keep track of tickets and assign them to the relevant staff. |
| Ticket | A task that needs to be completed in order for a complaint to be resolved. |

#### **5.2 References**
