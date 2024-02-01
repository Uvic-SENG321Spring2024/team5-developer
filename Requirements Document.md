<p = align="center">
   <img src="https://www.consumerprotectionbc.ca/wordpress/wp-content/themes/consumerprotectionbc/images/logo.png" width="30%">
<p>

<h1 align="center"> Requirements Document - Consumer Protection BC </h1>

## Revision History

| Name | Date | Reason for Changes | Version |
| ----------- | ----------- | ------------- | ---------- | 
| Initial Draft | 2024-01-30 | Document Created | 1.0 |
|  |  | | |
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

## 2. Business Requirements

#### **2.1 Background**

#### **2.2 Business Opportunity**

#### **2.3 Business Objectives**

#### **2.4 Success Metrics**

#### **2.5 Product Vision Statement**

## 3. Scope and Limitations

#### **3.1 Major Features**

#### **3.2 Project Scope**

#### **3.3 Limitations and Exclusions**

## 4. Context Description

#### **4.1 User Classes and Characteristics**

Based on information collected during interviews with Consumer Protection BC, three main user classes have been identified. These user classes (LIOs, LIO Supervisors, and Investigatory Departments) form the core team responsible for managing and resolving consumer complaints.

1. **Licensing and Information Officers (LIOs):** LIOs drive the complaint resolution process by interacting with consumers, managing complaints, and ensuring secure and accurate handling of consumer details.
   - ***Usage Frequency:*** High
   - ***Usage Description:*** LIOs primarily use the system for complaint intake and management, inputting consumer details, and initiating the resolution process.
   - ***Technical Expertise:*** Moderate. LIOs are responsible for interacting with the complaint module of Iris and must ensure accurate input of consumer details.
   - ***Privilege Level:*** LIOs have access to all personal information and complaint details within Iris. They have limited access to fields handled by LIO supervisors.

2. **LIO Supervisors:** LIO Supervisors oversee the system, assign complaints to different Investigatory Departments, manage workflow, and have higher-level access.
   - ***Usage Frequency:*** Moderate
   - ***Usage Description:*** Supervisors primarily interact with the system by assigning tickets created by LIOs to the appropriate department, done within Iris.
   - ***Technical Expertise:*** Moderate. Supervisors interact with the software system on a lower frequency than LIOs, but must review information present in the system to make workflow decisions.
   - ***Privilege Level:*** Supervisors have similar access levels as LIOs, but have the added ability to review and assign tickets to the relevant Investigatory Department.

3. **Investigatory Departments:** Investigators handle complaint resolution by examining the laws covered by CPBC. They utilize information from the system for investigations and complete tickets by providing information about how a complaint was resolved.
   - ***Usage Frequency:*** High during complaint resolution
   - ***Usage Description:*** Investigators are assigned to examine and resolve complaints that they receive in ticket form through SysAid. They also interact with Iris by completing additional fields relating to how a complaint was eventually resolved.
   - ***Technical Expertise:*** Moderate. The primary job of Investigators lies outside the system in examining complaints and how they relate to relevant laws. However, Investigators must be able to understand the ticketing system and reliably provide it with accurate information.
   - ***Privilege Level:*** Investigators can only see tickets assigned to their specific department, and have only view-access to information relevant to their investigation. They have write-access for resolution-related fields to allow tickets to be closed.

Based on the objectives of the system, none of the classes—Licensing and Information Officers (LIOs), LIO Supervisors, and Investigators—should be prioritized over another. All three user classes interact with the system as a vital part in the complaint resolution process, and therefore failing to address the needs of one class over another will prevent the system from meeting its objectives.

#### **4.2 Operating Environment**

#### **4.3 Design and Implmentation Constraints**

#### **4.4 Assumptions and Dependencies**

## 5. Appendix

#### **5.1 Glossary of Terms**

| Term | Definition |
| ---- | ---------- |
|      |            |
|      |            |
|      |            |

#### **5.2 References**
