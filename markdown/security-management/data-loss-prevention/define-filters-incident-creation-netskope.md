---
title: Define Filters to apply for the Incident creation
description: Define and set filter conditions to filter the incoming  Netskope DLP  incidents. Control which of these incidents should be created as DLP incidents on your ServiceNow instance.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a Profile for Netskope DLP integration, Data Loss Prevention Incident Response Integration with Netskope, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Define Filters to apply for the Incident creation

Define and set filter conditions to filter the incoming  Netskope DLP  incidents. Control which of these incidents should be created as DLP incidents on your ServiceNow instance.

## Before you begin

Role required: sn\_dlir.admin

## About this task

This type of filtering helps you to isolate DLP incidents and to limit the number of DLP incidents that you create. If additional filtering criteria are set, only incidents that match the conditions are created.

## Procedure

1.  Select the **Filter based on conditions** option and define the criteria that an incoming Netskope DLP incident must satisfy so that a DLP incident is created.

2.  Using the lists and fields of the condition builder, set the filters in the **Filter Conditions** field.

    The options in the first field in the **Filter Conditions** match the fields that are available in the **Netskope DLP incident import** table. The criteria that you enter are case-sensitive. Verify that the criteria you define match the values of the incident.

3.  Add more conditions by clicking  **AND**  or  **OR**.

    -   If  **AND**  is selected, all conditions must be matched.
    -   If  **OR**  is selected, either condition can be matched.
4.  Click **Continue** and move to the Scheduling section.


**Parent Topic:**[Create a Profile for Netskope DLP integration](create-profile-netskope-dlp-integration.md)

