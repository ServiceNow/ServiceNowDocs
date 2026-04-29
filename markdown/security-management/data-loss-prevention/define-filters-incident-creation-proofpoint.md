---
title: Define filters to apply for the Incident creation
description: Define and set filter conditions to filter the incoming  Proofpoint DLP  incidents. Control which DLP incidents should be created on ServiceNow.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a Profile for Proofpoint DLP integration, Data Loss Prevention Incident Response Integration with Proofpoint, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Define filters to apply for the Incident creation

Define and set filter conditions to filter the incoming  Proofpoint DLP  incidents. Control which DLP incidents should be created on ServiceNow®.

## Before you begin

Role required: sn\_dlir.admin

## About this task

This type of filtering helps you to isolate DLP incidents and to limit the number of DLP incidents that you create. If additional filtering criteria are set, only incidents that match the conditions are created.

## Procedure

1.  Select the **Filter based on conditions** option and define the criteria that an incoming Proofpoint DLP incident must satisfy so that a security incident is created.

2.  Using the lists and fields of the condition builder, set the filters in the **Filter Conditions** field.

    The options in the first field in the **Filter Conditions** matches the fields that are available in the DLP incident. The criteria that you enter are case-sensitive. Verify that the criteria you define match the values of the incident.

    ![Define filters to apply for the Incident creation.](../../data-loss-prevention/image/dlp-proofpoint-filter.gif)

3.  Add more conditions by clicking  **AND**  or  **OR**.

    -   If  **AND**  is selected, all conditions must be matched.
    -   If  **OR**  is selected, either condition can be matched.
4.  Click **Finish**.


**Parent Topic:**[Create a Profile for Proofpoint DLP integration](../task/create-profile-proofpoint-dlp-integration.md)

