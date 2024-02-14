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
| Final | 2024-02-04 | Final edit | 1.3 |

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

## 1. Overview

Consumer Protection BC (CPBC), a government organization in charge of business regulation and licensing, uses consumer complaints to ensure a fair marketplace. Consumers across the province are able to contact CPBC with their concerns about unfair business practices and in turn, the CPBC can conduct inspections and investigations.

The current complaint system is inefficient and prone to human error. It consists of two software programs called Iris and SysAid, where Iris is used to input and store complaints received from a consumer, and SysAid is used to create tickets in order for complaints to be resolved by CPBC staff. By using two systems to manage each consumer complaint, complaints are resolved unsatisfactorily slow. 

A simplification of the complaint process would lead to an increase in the number of complaints successfully resolved each quarter, higher consumer satisfaction, and higher work satisfaction from CPBC staff. By building a product that can effectively interface with both Iris and SysAid - CPBC’s required internal software - fallible manual processes can be reduced. Consumer complaints that are essential to CPBC and its role in maintaining a safe marketplace will be resolved faster and with fewer oversights.

The following document outlines CPBC's business objectives and requirements, the scope of this project, user classes for the product, and all assumptions and dependencies.

## 2. Business Requirements

#### **2.1 Background**
The existing procedure for submitting a complaint to CPBC is characterized by a significant reliance on manual processes, making it susceptible to human errors. The complaint submission process involves the utilization of two distinct software systems: Iris, where the LIO's file consumer complaints, and SysAid, where the complaint ticket is generated manually by employees. However, a notable discrepancy exists between these two systems, emphasizing the necessity for a more cohesive and streamlined approach. Implementing a refined process would not only alleviate stress for both users and employees but also mitigate errors by incorporating automation into the system. This integration aims to enhance efficiency and foster a more seamless experience in managing and resolving complaints.

#### **2.2 Business Opportunity**

The system that the CPBC is currently using is highly prone to inefficiencies and human error. Moreover, the current ticketing system is underutilized due to its inefficiency.  

Customer Requirements:
- Organizing the consumer complaint process to reduce the time taken for filing.
- Minimize human error introduced by transferring data back and forth between two systems.
- Simplify the user experience for the staff to improve overall satisfaction.
- Ensure access permissions align with the security needs of the company.

#### **2.3 Business Objectives**

The proposed product is expected to address several challenges for CPBC in a measurable manner. The primary business objectives targeted by the solution include:

- Enhancing Process Efficiency: This will be quantified by the time required to both submit a complaint and generate a corresponding ticket.
- Minimizing Human Errors: The aim is to decrease the frequency of errors during the complaint handling process.
- Elevating Customer Satisfaction: This will be assessed through post-complaint filing surveys, focusing on improving the overall user experience.
- Streamlining User Access Permissions: The solution will maintain a user list with corresponding permissions, ensuring access is tailored to individual qualifications.

#### **2.4 Success Metrics**

- Accuracy of Complaint Handling:
   * Indicator: 80% of complaints accurately handled and resolved.
   * Impact: Ensures consumer satisfaction and regulatory compliance.
 
- Efficiency in Workflow:
   * Indicator: Reduction in the time taken to process and resolve complaints by 40%.
   * Impact: Increases overall efficiency, minimizes delays, and enhances responsiveness.
 
- User Satisfaction:
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

The new product's long-term vision is to streamline complaint filing and fulfillment, addressing the underutilization of the current system. By integrating Iris and SysAid, we aim to reduce complaint processing time. Users will interact with the new, unified system instead of navigating both Iris and SysAid, ensuring a more efficient and user-friendly experience. The following diagram illustrates this proposed process:

<p align="center">
   <img width="523" alt="Product Diagram" src="https://github.com/Uvic-SENG321Spring2024/team5-developer/assets/101749612/dd522fe6-d7f7-4aad-b2c9-13b2ad79119c">
</p>

## 3. Scope and Limitations

#### **3.1 Major Features**

The current system contains two major features: the complaints module and the ticketing system. The complaints module, located within the Iris program, allows LIOs to log, manage, and resolve complaints filed by consumers. These complaints are then stored within Iris’ database indefinitely, and may be accessed at a future time. The ticketing system, SysAid, allows LIOs to internally track and update progress on complaints filed within Iris.

The new product will interconnect these two features into one interface. This interface will allow LIOs to file, manage, track, and resolve complaints and tickets using only one system. Complaints and tickets will remain accessible within Iris and SysAid respectively.

#### **3.2 Project Scope**

The objectives of the new interface are to:
- Reduce the time spent by LIOs navigating between complaints and tickets modules.
- Improve efficiency while finding and referencing past and current filed complaints.
- Accurately manage complaints currently under investigation.
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

#### **4.3 Design and Implmentation Constraints**

When designing and implementing of the product, developers have a few limitations when implementing the product. Firstly, the developer must create a product to run on a Windows machine. The product has to communicate between Iris and SysAid, two different systems. It must communicate the information inputted into Iris to SysAid. Consumer Protection BC requires it to keep both applications due to Iris not having a ticketing system. Finally, account permissions and overall security of information being sent from Iris to SysAid must be kept secure, private and maintained through the automated process of transferring information.

#### **4.4 Assumptions and Dependencies**

The project’s dependency on two pre-existing third-party software systems could affect the defined requirements. 

One assumption being made is how Iris and SysAid function and how they are utilized by CPBC. The current understanding of their usage is that information is manually input into each system using pre-defined fields. Iris's complaint module consists of a database of previous and current complaints that can be updated by LIOs. The information that LIOs upload into Iris is more granular, and there are specific fields that can be filled out. SysAid is used for its ticketing capabilities and notification system, since Iris does not have the capability to notify investigators when they are assigned to a complaint. SysAid collects more generic information-- many of the details that get a specific field in Iris do not have a corresponding field in SysAid and are instead included in the Description field. However, SysAid allows LIOs to define the impact and priority of the complaint. If the assumptions about how the two different systems are used in conjunction with each other are incorrect or change, it may result in requirements needing to be adjusted.

The only part of Iris’ system that the product will interact with is the complaint module. If this information is inaccurate, it will change the requirements.

Additionally, CPBC has access to the source code for Iris, but they do not have source code for SysAid. The product will need to automate the process of putting information into both Iris and SysAid. The dependency on SysAid and any limitations caused by a lack of access to source code may also necessitate changes to the requirements.

## 5. Appendix

#### **5.1 Glossary of Terms**

| Term | Definition |
| ---- | ---------- |
| CPBC | Consumer Protection British Columbia. |
| Iris | Software system used to input and store consumer complaints and their resolution status. |
| LIO | Licensing Information Officer; the CPBC employee who first logs a consumer complaint. |
| SysAid | Software system used to keep track of tickets and assign them to the relevant staff. |
| Ticket | A task that needs to be completed in order for a complaint to be resolved. |

