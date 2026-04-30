---
title: Disable the safety incident playbook
description: If you need to enable a tab-based experience for safety incidents in your instance, configure the property that disables the Report an incident playbook.
locale: en-US
release: yokohama
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure settings, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Disable the safety incident playbook

If you need to enable a tab-based experience for safety incidents in your instance, configure the property that disables the **Report an incident** playbook.

## Before you begin

Ensure that the application scope is selected as Health and Safety Incident Management. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

Role required: sn\_ohs\_im.admin

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

2.  In the **Flag to disable the playbook for Health and Safety Incidents** property, select **Yes**.


## Result

The following changes occur when the safety incident playbook is turned off:

-   Enables a tab-based experience for safety incidents. You can record the incident related information into these tabs:
    -   People involved
    -   Injury and illness
    -   Assets
    -   Root cause analysis
    -   Health and Safety actions
-   Enables the association of multiple injuries and illnesses to a single incident.

**Parent Topic:**[Setting up Health and Safety Incident Management](../concept/setting-up-hs-incident-mgmt.md)

