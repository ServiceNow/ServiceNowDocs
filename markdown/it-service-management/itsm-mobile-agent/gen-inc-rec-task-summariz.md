---
title: Generating task summaries for incident records
description: Generate incident record and task summaries with generative AI task summarization capabilities that help reduce the effort required to draft work notes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/gen-inc-rec-task-summariz.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing incidents and tasks using the My Work applet, ITSM Mobile Agent, IT Service Management]
---

# Generating task summaries for incident records

Generate incident record and task summaries with generative AI task summarization capabilities that help reduce the effort required to draft work notes.

You can summarize the incident record and activity information when adding work notes to an incident record or while reassigning an incident.

When adding work notes to an incident record, you can use the **Summarize** option that uses the generative AI task summarization capabilities. These capabilities summarize an incident record and activity information, such as the issue details or actions taken.

The summarize feature is available for the following applets:

-   My team
-   Major incidents
-   My work

\[Omitted image "itsm-ma-summarize-option.png"\] Alt text: Summarize option for incident record

After the information summary is generated, you can edit and add the information as work notes. The summary can include the following information:

-   Incident record details such as issue or short description
-   Activities such as action taken or existing work notes or comments
-   Affected CIs and impacted services

You can also customize the information summary \(prompt\) from the ServiceNow Otto for ITSM admin console. For more information, see [Customize a ServiceNow Otto for IT Service Management \(ITSM\) skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-itsm-skill.md).

\[Omitted image "itsm-ma-summarize-worknote.png"\] Alt text: Incident record summarized as work notes

For more information on ServiceNow Otto for mobile, see [ServiceNow Otto for Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/now-assist-mobile-landing.md).

## Activation of incident record summarization skill

To enable the summarization feature in the ITSM Mobile Agent application, you must activate or customize the incident summarization skill from the ServiceNow Otto for ITSM admin console. For more information on activating and customizing the incident summarization skill, see [Customize a ServiceNow Otto for IT Service Management \(ITSM\) skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/now-assist-for-it-service-management-itsm/cust-now-assist-itsm-skill.md).

If you have already configured the incident summarization skill in the ServiceNow Otto for ITSM admin console and then installed the ITSM Mobile Agent application, complete the following actions:

1.  On the Input form actions table, filter the action records by **Label** with `Summarize`, and **Application** with `ITSM Mobile Agent`. The summarization records such as `Incident summarize action` and `Incident summarize action (Reassign)` are displayed.
2.  Select the records and set the **Active** field to `true`.

