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
The project’s dependency on two pre-existing third-party software applications could affect the defined requirements. 

The ways that Iris and SysAid function as individual systems and how they are utilized is one assumption that may affect requirements if it is incorrect. The current understanding of their usage is that information is manually input into each system using pre-defined fields. Iris consists of a database of previous and current complaints that can be updated by users, and collects more granular information about the complaint in specific fields. SysAid is used primarily for its ticketing capabilities and notification system, since Iris does not have the capability to notify investigators when they are assigned to a complaint. It collects more generic information, and also allows LIOs to define the impact and priority of the complaint. If the assumptions about how the two different systems are used in conjunction with each other are incorrect or change, it may result in requirements needing to be adjusted.

The only part of Iris’ system that the product will interact with is the complaint module, and the only part of SysAid’s system that will be interfaced with is the ticketing system. If this information is inaccurate, it will change the requirements.

Additionally, CPBC has access to the source code for Iris, but they do not have source code for SysAid. The product will need to automate the process of putting information into both Iris and SysAid. The dependency on SysAid and any limitations caused by a lack of access to source code may also necessitate changes to the requirements.


## 5. Appendix

#### **5.1 Glossary of Terms**

| Term | Definition |
| ---- | ---------- |
|      |            |
|      |            |
|      |            |

#### **5.2 References**
