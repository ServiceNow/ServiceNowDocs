---
title: Customize fields copied from Universal Request to incident
description: Customize which fields are automatically copied from a universal request to an associated incident record. This eliminates manual data entry each time you create an incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/customize-fields-copied-univ-inc.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Incident Management integration with Universal Request, Incident Management integrations, Reference, Incident Management, IT Service Management]
---

# Customize fields copied from Universal Request to incident

Customize which fields are automatically copied from a universal request to an associated incident record. This eliminates manual data entry each time you create an incident.

## Before you begin

Role required: incident\_manager or admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list` and press the Enter key.

2.  Search for and open the system property **sn\_inc\_uni\_req.incident.universal\_request.copy\_fields**.

3.  In the **Value** field, enter the universal request field name and the corresponding incident field name.

    For example, `caller_id=opened_for` means that the value of the caller\_id field from the universal request form is copied to the opened\_for field in the incident form.


**Parent Topic:**[Incident Management integration with Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/inci-mgmt-integ-with-univ-req.md)

