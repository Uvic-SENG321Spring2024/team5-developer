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

1. **Licensing and Information Officers (LIOs):**
   - ***Usage Frequency:***
   - ***Usage Description:***
   - ***Technical Expertise:***
   - ***Privilege Level:***

2. **LIO Supervisors:**
   - ***Usage Frequency:***
   - ***Usage Description:***
   - ***Technical Expertise:***
   - ***Privilege Level:***

3. **Investigatory Departments:**
   - ***Usage Frequency:***
   - ***Usage Description:***
   - ***Technical Expertise:***
   - ***Privilege Level:***

#### **4.2 Operating Environment**

#### **4.3 Design and Implmentation Constraints**

#### **4.4 Assumptions and Dependencies**

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
