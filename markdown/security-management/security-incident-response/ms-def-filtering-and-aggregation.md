---
title: Define filter and aggregation criteria
description: Define filter and aggregation conditions to control which Microsoft Defender incidents generate new security incidents and whether incoming incidents should be merged into existing ones. These conditions ensure accurate incident grouping and prevent unnecessary duplication.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-01-05"
reading_time_minutes: 3
breadcrumb: [Microsoft Defender integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define filter and aggregation criteria

Define filter and aggregation conditions to control which Microsoft Defender incidents generate new security incidents and whether incoming incidents should be merged into existing ones. These conditions ensure accurate incident grouping and prevent unnecessary duplication.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## About this task

Filtering helps you isolate security incidents and limit the number of security incidents that you create. If you set additional filtering criteria, only the required incidents are ingested without having to change the query or the triggered incident configuration.

Aggregation Conditions define additional incident field criteria that enable an incoming incident to be appended to an open security incident instead of creating one.

## Procedure

1.  If you aren’t continuing from the previous section of the Mapping criteria, access the profile you’re defining.

    1.  Navigate to **All** &gt; **Microsoft Defender Integration** &gt; **Defender Incident Profiles**.

    2.  Select the profile that you’re continuing to define.

    3.  Select **Filtering and Aggregation** in the progress bar.

2.  Select **Filter based on conditions** check box to define the criteria that an incoming Microsoft Defender incident must satisfy so that a security incident is created.

3.  In the **Filter Conditions** search field, specify the filter conditions that must be met.

    These conditions must match the fields that are displayed on the Microsoft Defender Sample Incident Ingestion section for the Incident that you ingested. These fields are dynamic and change depending on the Incident that you ingest. The criteria that you enter are case-sensitive. Verify that the criteria you define match the values of the Incident.

    Use the filter condition `incident_id` for the following fields with multiple values:

    -   Severity
    -   LastModifiedBy
    -   LastUpdateDateTime
    -   Keywords
    Because the filter condition can retrieve only strings, you must use the `incident_id` filter condition for the preceding fields to confirm that the data is filtered correctly.

4.  Select **AND** or **OR**.

    -   If **AND** is selected, all conditions must be matched.
    -   If **OR** is selected, either condition can be matched.
5.  To set a second filter condition, select **New Criteria**.

    ![Define filter and aggregation criteria](../image/ms-def-fil-and-agg.png)

6.  Select **Aggregation Conditions** check box to define additional incident field criteria that enables an incoming incident to be appended to an open security incident instead of creating one.

7.  In the **Incident fields with matching values** field, enter the field values that you want to match on existing security incidents in your ServiceNow AI Platform instance.

    All field values that you selected in the multi selection input field must match so that the aggregation criterion is met and that this incoming incident can be appended to an existing security incident. This selection implies it’s an `AND` condition where fields, such as Observables and Configuration Items that may have multiple field values, are mapped to them. If only a subset of the values is matched, the Microsoft Incident aggregation conditions aren’t met and a new security incident is created.

8.  Select **Add New Criteria** to add multiple field matching conditions.

    The aggregation occurs if any one of the multi selection field conditions that you define are met. This selection implies the `OR` condition.

9.  Select **Log work note for new Incident** to update the work note for a new incident when it’s added to a security incident.

    The work note logs the creation of a new incident and includes a link to its details. The log work note also updates more details that you add to the work note field in your mapping section.

10. Select **Continue**.


## What to do next

Set a schedule to retrieve the incident data and ingested incidents that match the criteria in the profile. For more information, see [Schedule incident retrieval](ms-defender-schedule-inc.md).

