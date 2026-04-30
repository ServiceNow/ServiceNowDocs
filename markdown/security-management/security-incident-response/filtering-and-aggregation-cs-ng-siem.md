---
title: Define filter and aggregation criteria
description: Define and set filter conditions to specify which incoming CrowdStrike Next-Gen SIEM detections should create security incidents. You can also define additional detection field criteria that allows an incoming detection to be appended to an open security incident instead of creating an incident.Set the filtering conditions so that security incidents are created only when the filtering conditions match.Define additional incident aggregation criteria that aggregates an incoming detection to an existing SIR security incident instead of creating similar, potentially duplicate detections. When you use field matching value criteria for each profile, this additional aggregation can reduce the number of active, overlapping security incidents by placing all related detections data on a single security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Filtering and Aggregation]
breadcrumb: [CrowdStrike Next-Gen SIEM integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define filter and aggregation criteria

Define and set filter conditions to specify which incoming CrowdStrike Next-Gen SIEM detections should create security incidents. You can also define additional detection field criteria that allows an incoming detection to be appended to an open security incident instead of creating an incident.

## Set filtering conditions

Set the filtering conditions so that security incidents are created only when the filtering conditions match.

### Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

### About this task

This type of filtering helps you to isolate security incidents and limits the number of security incidents that you create. If you set additional filtering criteria, only the required detections are ingested without having to change the query or the triggered detection configuration.

### Procedure

1.  To define the criteria that an incoming CrowdStrike Next-Gen detection must satisfy so that a security incident is created, select **Filter based on conditions**.

    The options in the first field in the Filter Conditions match the fields that are displayed on the CrowdStrike Next-Gen Sample detection Ingestion section for the detection that you ingested. These fields are dynamic and change depending on the detection that you ingest. The criteria that you enter is case-sensitive. Verify that the criteria that you define matches the values of the detection.

    Use the filter condition `detection_id` for the following fields with multiple values:

    -   composite\_id
    -   host\_names
    -   seconds\_to\_resolved
    -   seconds\_to\_triaged
    Because the filter condition can retrieve only strings, you must use the `detection_id` filter condition for the above fields to ensure that the data is filtered correctly.

2.  Using the lists and fields of the conditions builder, set the filters for the first row.

3.  To add more conditions, click **AND** or **OR**.

    -   If **AND** is selected, all conditions must be matched.
    -   If **OR** is selected, either condition can be matched.
4.  To set a second filter condition, click **New Criteria**.


## Define aggregation conditions

Define additional incident aggregation criteria that aggregates an incoming detection to an existing SIR security incident instead of creating similar, potentially duplicate detections. When you use field matching value criteria for each profile, this additional aggregation can reduce the number of active, overlapping security incidents by placing all related detections data on a single security incident.

### Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

### About this task

If a new incident matches all the values that are selected in the aggregation field conditions in the mapping step, the incident is automatically added to the most recently opened security incident with the same field values. As a user with the sn\_si.ingestion\_profile\_admin role working with security incidents, you can view all the added aggregate incidents on a related list on a security incident.

All the aggregated incidents on a security incident are displayed on the CrowdStrike Next-Gen SIEM Aggregated Incidents related list. This list details the associated timestamps and aggregated field values. This information helps you understand why incidents are added to the existing security incidents.

### Procedure

1.  To define additional incident field criteria that allows an incoming CrowdStrike Next-Gen SIEM detection to be appended to an open security incident instead of creating a new incident, select the **Aggregation Conditions**.

2.  In the **Incident fields with matching values** field, enter the field values that you want to match on existing security incidents in your ServiceNow AI Platform instance.

    All field values that you selected in the multi selection input field must match so that the aggregation criteria is met and that this incoming incident can be appended to an existing security incident. This selection implies it is an `AND` condition where fields, such as Observables and Configuration Items that may have multiple field values, are mapped to them. If only a subset of the values is matched, the CrowdStrike Next-Gen SIEM Incident aggregation conditions are not met and a new security incident is created.

3.  To add multiple field matching conditions, click **Add New Criteria**

    The aggregation occurs if any one of the multi selection field conditions that you define are met. This selection implies the `OR` condition.

4.  To update the work note for a new incident when it is added to a security incident, select **Log work note for new Incident**.

    The work note logs that a new incident is added and includes a link to the incident details. The log work note also updates more details that you add to the work note field in your mapping section.

5.  To configure the schedule, click **Continue**.


### What to do next

Set a schedule to retrieve the incident data and ingested incidents that match the criteria in the profile.

