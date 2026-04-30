---
title: Define filters to apply for the Incident creation
description: Define and set filter conditions to filter the incoming  DLP  alerts. Determine the alerts that should be created as DLP incidents in ServiceNow.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a profile for ICAP DLP integration, Internet Content Adaption Protocol \(ICAP\) integration for DLP IR, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Define filters to apply for the Incident creation

Define and set filter conditions to filter the incoming  DLP  alerts. Determine the alerts that should be created as DLP incidents in ServiceNow.

## Before you begin

Role required: sn\_dlir.admin

## About this task

Filtering helps you to isolate DLP alerts and to limit the number of DLP alerts that you create. If additional filtering criteria are set, only alerts that match the conditions are created.

## Procedure

1.  Select **Post Incident Ingestion Filter** check box to apply the post incident ingestion filters and retrieve the incidents that match the filter criteria.

2.  Select the **Filter based on conditions** option and define the criteria that an incoming ICAP DLP incident must satisfy so that a DLP incident is created.

3.  Set the filters in the **Filter Conditions** field.

    The options in the drop down **Filter Conditions** match the fields that are available in the **ICAP DLP incident import** table. The criteria that you enter are case-sensitive. Verify that the criteria you define match the values of the incident.

4.  Add more conditions by clicking  **AND**  or  **OR**.

    -   If  **AND**  is selected, all conditions must be matched.
    -   If  **OR**  is selected, either condition can be matched.

## What to do next

To configure the schedule, click **Continue**.

**Parent Topic:**[Create a profile for ICAP DLP integration](create-profile-for-icap.md)

