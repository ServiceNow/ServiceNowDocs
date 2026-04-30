---
title: Define filter and aggregation criteria
description: Define and set filter conditions to specify which incoming Cortex XSIAM Incidents should create security incidents. You can also define additional Incident field criteria that allows an incoming Incident to be appended to an open security incident instead of creating an incident.Set filter conditions for which Palo Alto Cortex XSIAM incidents create security incidents in ServiceNow.Select Aggregation Conditions to define additional incident field criteria that allows an incoming incident to be appended to an open security incident instead of creating a new one.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-11-11"
reading_time_minutes: 2
breadcrumb: [Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define filter and aggregation criteria

Define and set filter conditions to specify which incoming Cortex XSIAM Incidents should create security incidents. You can also define additional Incident field criteria that allows an incoming Incident to be appended to an open security incident instead of creating an incident.

## Set filtering conditions

Set filter conditions for which Palo Alto Cortex XSIAM incidents create security incidents in ServiceNow.

### Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

### About this task

Filtering helps you isolate security incidents and limits the number of security incidents that you create. If you set additional filtering criteria, only the required incidents are ingested without having to change the query or the triggered incident configuration.

### Procedure

1.  Select **Filter based on conditions** to define the criteria that an incoming XSIAM incident must satisfy so that a security incident is created.

    The options in the first field in the Filter Conditions match the fields that are displayed on the Cortex XSIAM Sample Incident Ingestion section for the Incident that you ingested. These fields are dynamic and change depending on the Incident that you ingest. The criteria that you enter is case-sensitive. Verify that the criteria that you define matches the values of the Incident.

    Use the filter condition `incident_id` for the following fields with multiple values:

    -   Severity
    -   creation\_time
    -   alert\_categories
    -   alert\_count
    Because the filter condition can retrieve only strings, you must use the `incident_id` filter condition for the above fields to ensure that the data is filtered correctly.


## Define aggregation conditions

Select Aggregation Conditions to define additional incident field criteria that allows an incoming incident to be appended to an open security incident instead of creating a new one.

### Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

### Procedure

1.  Select **Aggregation Conditions** check box.

2.  In the **Incident fields with matching values** field, enter the field values that you want to match on existing security incidents in your ServiceNow AI Platform instance.

    All field values that you selected in the multi selection input field must match so that the aggregation criteria is met and that this incoming incident can be appended to an existing security incident. This selection implies it is an `AND` condition where fields, such as Observables and Configuration Items that may have multiple field values, are mapped to them. If only a subset of the values is matched, the Cortex XSIAM Incident aggregation conditions are not met and a new security incident is created.

3.  Select **Add New Criteria** to add multiple field matching conditions.

    The aggregation occurs if any one of the multi selection field conditions that you define are met. This selection implies the `OR` condition.

4.  Select **Log work note for new Incident** to update the work note for a new incident when it is added to a security incident.

    The work note logs that a new incident is added and includes a link to the incident details. The log work note also updates more details that you add to the work note field in your mapping section.

    ![Define filtering and aggregation conditions](../image/xsiam-filtering-aggregation.png)

5.  Select **Continue**.


### What to do next

Set a schedule to retrieve the incident data and ingested incidents that match the criteria in the profile. For more information, see [Schedule incident retrieval](../task/pan-xsiam-schedule-inc-retrieval.md).

