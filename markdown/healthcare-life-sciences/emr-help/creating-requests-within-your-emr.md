---
title: Create requests within your EMR system
description: You can request service directly within the EMR system which automatically creates a service request in a ServiceNow instance
locale: en-US
release: australia
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Create requests within your EMR system

You can request service directly within the EMR system which automatically creates a service request in a ServiceNow instance

Work on task records that are automatically created when clinicians submit ServiceNow service requests from an EMR system. Incidents are the task type configured by default with the EMR Help application.

As a fulfiller, for example, if you are an IT agent or a healthcare agent, you can access the task record for a service request on the ServiceNow instance linked with the EMR system.

Incidents are the task type configured by default with the EMR Help application. Ensure an administrator has added the EMR Incident Data related list to the Incident form.

**Note:** The EMR Request Data related list of an incident form includes any EMR system-specific data. The EMR Request Data related list data is viewable only if you have the sn\_ind\_rmt\_help.viewer role and the ITIL role. This related list appears empty if you do not have the required roles.

Use EMR Help for the following:

-   [Submitting ServiceNow IT service requests from EMR systems](emr-help-issues-reporting.md)
-   [Creating healthcare cases from within your EMR](submitting-cases-from-emr-systems.md)

