---
title: Automatically add skills to incidents or interactions in Workforce Optimization for ITSM
description: Define conditions for incidents or interactions and add skills required for those conditions using skill determination rules. When new incidents and interactions that are created meet these conditions, the skill determination business rule automatically adds the skills to those records. In the Workforce Optimization for ITSM Channels and Work scheduler applications, the work items get automatically assigned to the right agents based on the skills.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Routing work based on skills in Workforce Optimization for ITSM, Skills Management in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Automatically add skills to incidents or interactions in Workforce Optimization for ITSM

Define conditions for incidents or interactions and add skills required for those conditions using skill determination rules. When new incidents and interactions that are created meet these conditions, the skill determination business rule automatically adds the skills to those records. In the Workforce Optimization for ITSM Channels and Work scheduler applications, the work items get automatically assigned to the right agents based on the skills.

## Before you begin

Role required: skill\_admin or admin

## About this task

The following business rules are used in Workforce Optimization for ITSM skill determination:

-   **Skill determination for incident** evaluates new incidents for the conditions defined in the skill determination rules set for all incidents and adds those skills to the incident records.
-   **Skill determination for interaction** evaluates new interactions for the conditions defined in the skill determination rules set for all interactions and adds those skills to the interaction records.

The table below shows the skill determination rules available for Workforce Optimization for ITSM.

**Note:** To add language detection skills, you must set dynamic translation APi. for more information, see [Dynamic Translation API](https://www.servicenow.com/docs/access?context=dyn-translation-apis&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Skill Determination Rule|Source Table|Type|Description|
|------------------------|------------|----|-----------|
|Language Detection Incident|Incident \[incident\]|Advanced|The business rule evaluates new incidents for the language entered in the incident short description and adds that language as a required skill for those incidents.|
|Language Detection Interaction|Interaction \[interaction\]|Advanced|The business rule evaluates new interactions for the language entered in the interaction short description and adds that language as a required skill for those interactions.|
|SAP Skills|Incident \[incident\]|Simple|The business rule evaluates new incidents for the **Service** field that starts with 'SAP', 'sap', or 'Sap' and adds **SAP** and **Backoffice** skills as required skills for those incidents.|
|VPN Incident|Incident \[incident\]|Simple|The business rule evaluates new incidents for the **Short description** field that contains 'VPN', 'vpn', or 'Vpn' and adds **Router and Switch** and **Network** skills as required skills for those incidents.|
|VPN Interaction|Interaction \[interaction\]|Simple|The business rule evaluates new interactions for the **Short description** field that contains 'VPN', 'vpn', or 'Vpn' and adds **Router and Switch** and **Network** skills as required skills for those incidents.|
|Windows|Incident \[incident\]|Simple|The business rule evaluates new incidents for the **Configuration item** field that contains 'Windows', 'windows', or 'WINDOWS' and adds **Windows Installation/Setting** and **Windows Servers** skills as required skills for those incidents.|

## Procedure

1.  Navigate to **All** &gt; **Skills** &gt; **Skill Determination Rules**.

2.  Add the desired rule for an incident or an interaction.

    For information, see [Create Skill Determination rules to assign skills to work items](https://www.servicenow.com/docs/access?context=conf-simple-skill-determination-rule&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


**Parent Topic:**[Routing work based on skills in Workforce Optimization for ITSM](../concept/skill-determination-configurable-wfo-itsm.md)

