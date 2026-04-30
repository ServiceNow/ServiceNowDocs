---
title: Customize fields copied from Universal Request to incident
description: Customize fields so that the values of some fields in the universal request automatically get copied to an incident record when an incident is associated with a universal request record. It saves your time from manually entering the information every time you create an incident.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Universal Request integration - Incident Management, Incident Management integrations, Reference, Incident Management, IT Service Management]
---

# Customize fields copied from Universal Request to incident

Customize fields so that the values of some fields in the universal request automatically get copied to an incident record when an incident is associated with a universal request record. It saves your time from manually entering the information every time you create an incident.

## Before you begin

Role required: incident\_manager or admin

## Procedure

1.  In the left navigation pane, enter `sys_properties.list` and press the Enter key.

2.  Search and open the system property **sn\_inc\_uni\_req.incident.universal\_request.copy\_fields**.

3.  In the **Value** field enter the universal request and the incident field.

    For example, `caller_id=opened_for` means that the value of the field called\_id from the universal request form is copied to the opened\_for field in the incident form.


**Parent Topic:**[Universal Request integration - Incident Management](../concept/inci-mgmt-integ-with-univ-req.md)

