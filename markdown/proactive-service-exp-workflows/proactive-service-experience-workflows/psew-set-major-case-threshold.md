---
title: Setting major case threshold for auto generated cases
description: Set the threshold value for major cases generated from incidents in the system properties.
locale: en-US
release: australia
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Auto-creation of cases, Proactive Service Experience Workflow, Use, Product Support for Technology]
---

# Setting major case threshold for auto generated cases

Set the threshold value for major cases generated from incidents in the system properties.

## Before you begin

-   Role required: admin
-   Selected application scope: Proactive Service Experience Workflows

## About this task

A default threshold value has been predefined to generate major cases from incidents. This value may be too low or your organization may not be using the CSM major case management feature. In such cases, you can modify the threshold value in the system properties after the Proactive Service Experience Workflows has been enabled.

## Procedure

1.  In the Application Navigator, type, `sys_properties.list`.

2.  Search in the text field for `major_case_affected_threshold` system property.

3.  Click the system property to open the record.

4.  Change the threshold number in the Value field.

    **Note:** The lower the integer value, the higher number of cases needed to trigger a major case. If a higher number is specified, the inverse is true.

5.  Click **Update**.


**Parent Topic:**[Auto-creation of cases and updates from incidents](../concept/psew-auto-creation-case.md)

