---
title: Restrict access to an incident
description: Restrict access to an incident that contains sensitive information so that only authorized agents can access it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/restrict-incident-access.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Incident Management integration with Universal Request, Incident Management integrations, Reference, Incident Management, IT Service Management]
---

# Restrict access to an incident

Restrict access to an incident that contains sensitive information so that only authorized agents can access it.

## Before you begin

Role required: admin or user

## About this task

Both agents and users can mark an incident as restricted. Users can mark an incident as restricted while creating it. An agent can also mark an incident as restricted while triaging it or while working on it. Incidents marked as restricted can be accessed only by the following agents:

-   Routing agents who are members of the assignment group and have the sensitive agent role.
-   All primary ticket agents.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **All**.

2.  Open the incident record to restrict.

3.  On the form, select **Restrict**.

    The restricted fields are hidden, and the form is read-only.

    **Note:** Only agents with the access role can mark the incident as unrestricted.

4.  Select **Update**.


**Parent Topic:**[Incident Management integration with Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/inci-mgmt-integ-with-univ-req.md)

