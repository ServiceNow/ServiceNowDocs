---
title: Set the filtering conditions for security incidents
description: Set the filtering conditions so that security incidents are created only when the filtering conditions match.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-06-30"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Next-Gen SIEM integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set the filtering conditions for security incidents

Set the filtering conditions so that security incidents are created only when the filtering conditions match.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

This type of filtering helps you to isolate security incidents and limits the number of security incidents that you create. If you set additional filtering criteria, only the required detections are ingested without having to change the query or the triggered detection configuration.

## Procedure

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


