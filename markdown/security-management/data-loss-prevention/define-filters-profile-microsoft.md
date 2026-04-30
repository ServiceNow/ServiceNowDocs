---
title: Define filters to apply for the Incident creation
description: Define and set filter conditions to filter the incoming  Microsoft DLP  events. Control which of these events should be created as DLP IR incidents on your ServiceNow instance.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a new incident profile for Microsoft DLP integration, Data Loss Prevention Incident Response with Microsoft, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Define filters to apply for the Incident creation

Define and set filter conditions to filter the incoming  Microsoft DLP  events. Control which of these events should be created as DLP IR incidents on your ServiceNow instance.

## Before you begin

Role required: sn\_dlir.admin\(Create, edit, and delete\)

sn\_dlir.analyst - View \(read-only\)

## About this task

This type of filtering helps you to isolate Microsoft DLP  events to limit the number of DLP IR incidents that you create. If the filtering criteria is set, only events that match the conditions are created as DLP incidents.

## Procedure

1.  Select the **Filter based on conditions** option.

2.  Using the lists and fields of the condition builder, set the filters in the **Filter Conditions** field.

    Define the criteria that an incoming Microsoft DLP event must satisfy so that a DLP incident is created.

    The options in the first field in the **Filter Conditions** match the fields that are available in the Microsoft DLP event. The criteria that you enter are case-sensitive. Verify that the criteria you define match the values of the event.

    ![Define filters to apply for the Incident creation.](../../data-loss-prevention/image/filtering-microsoftdlp.gif)

3.  Add more conditions by clicking  **AND**  or  **OR**.

    -   If  **AND**  is selected, all conditions must be matched.
    -   If  **OR**  is selected, either condition can be matched.
4.  Click **Continue** and move to the Match Content Configuration section.

    Earlier, UserID was mapped only to the Source User field but, the UserID field is currently available as a lookup attribute for all Purview events, including Endpoint events.


**Parent Topic:**[Create a new incident profile for Microsoft DLP integration](create-profile-microsoft-dlp-integration.md)

