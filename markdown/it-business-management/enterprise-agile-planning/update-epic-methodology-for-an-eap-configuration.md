---
title: Update epic methodology for an EAP configuration
description: Change the epic methodology of your Enterprise Agile Planning configuration to SAFe or Scrum based on your Agile workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/enterprise-agile-planning/update-epic-methodology-for-an-eap-configuration.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Update epic methodology for an EAP configuration

Change the epic methodology of your Enterprise Agile Planning configuration to SAFe or Scrum based on your Agile workflow.

## Before you begin

Set the Application Scope of your ServiceNow instance to Strategic Planning.

Role required: sn\_apw\_advanced.eap\_admin

## About this task

By default, the epic methodology for an EAP configuration is set to **SAFe** and all epics created for this configuration are SAFe epics. Based on how your Agile teams prefer to work, you can change the epic methodology to Scrum or retain it as SAFe.

**Note:** The epic methodology for an EAP configuration can be updated only if there are no work items associated with it. SAFe and Scrum use different work item hierarchies, so changing the methodology after adding epics, capabilities, or stories would break their existing parent-child rollup.

Consider the following before you choose an epic methodology for your configuration:

-   SAFe uses the Epic &gt; Capability &gt; Feature &gt; Story hierarchy. Scrum uses a simpler Epic &gt; Story hierarchy. For more information, see [Agile configurations in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/agile-configurations-in-eap.md).
-   If you sync epics from Strategic Planning or Jira through Agile Development 2.0, set the methodology to Scrum. For more information, see [Migrating from SAFe to EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/migrating-from-safe-to-eap.md).

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Enterprise Agile Planning** &gt; **EAP Configurations**.

2.  From the list of Enterprise agile configurations, locate the one you want to change the methodology for.

3.  Double-click the Epic methodology cell to change and update the value.

    \[Omitted image "eap-epic-methodology.png"\] Alt text: Epic methodology update for EAP configurations.

    If the Epic methodology column is not displayed in your ServiceNow instance, personalize the column settings. Use the Update Personalized List icon \(\[Omitted image "eap-personalize-list.png"\] Alt text: Update Personalized List icon\) from the list header.


