---
title: Create incident or security incident from an alert
description: When an alert must be escalated and assigned to someone who can resolve the underlying issue, you can open an incident.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View alert information, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create incident or security incident from an alert

When an alert must be escalated and assigned to someone who can resolve the underlying issue, you can open an incident.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

If Security Incident Response is activated, a security incident can be created.

You can manually create incidents and security incidents from the Alert form. To prevent duplicate tasks, the system checks the conditions of all task templates before creating an incident.

You can customize the created incident using the **EvtMgmtCustomIncidentPopulator.populateFieldsFromAlert** script include. The customization includes mapping fields from the alert to the incident or aborting the incident creation according to customized conditions. For more information, see [Custom alert fields](../concept/populate-custom-alert-fields.md).

You can populate incident fields using custom alert fields values that where populated from additional information fields. Use the **EvtMgmtCustomIncidentPopulator** script include to copy the values to the incident after copying the data to the alert. For more information, see [Custom alert fields](../concept/populate-custom-alert-fields.md).

**Note:** If Security Incident Response is activated, the base system includes an alert action rule called **Create security incidents for critical alerts**. This alert action rule creates security incidents when critical security events are reported.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  Click the alert **Number**.

3.  To create an incident:

    -   To create an incident, click **Quick Incident**.
    -   To create a security incident, click **Create Security Incident**. You must install the Security \(secops\) plugin to enable this option.
4.  Click **Update**.


## Result

The created incident appears in the **Task** field of the Alert form.

**Parent Topic:**[View alert information](t_EMViewAlert.md)

**Related topics**  


[Security incidents created from events and alerts](https://www.servicenow.com/docs/access?context=c_ScIncdUseAlrts&version=australia&pubname=australia-security-management&ft:locale=en-US)

