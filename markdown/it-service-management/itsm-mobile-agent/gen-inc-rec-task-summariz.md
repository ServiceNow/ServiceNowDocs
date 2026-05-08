---
title: Generating task summarization for incident records
description: Generate incident record and task summarization using GenAI task summarization capabilties which help reduce the effort required to draft work notes.
locale: en-US
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing incidents and tasks using My Work applet, ITSM Mobile Agent, IT Service Management]
---

# Generating task summarization for incident records

Generate incident record and task summarization using GenAI task summarization capabilties which help reduce the effort required to draft work notes.

You can summarize the incident record and activity information when adding work notes to an incident record or while reassigning an incident.

When adding work notes to an incident record, you can use the **Summarize** option that uses the GenAI task summarization capabilities to summarize an incident record and activity information, such as the issue details or actions taken.

The summarize feature is available for the following applets:

-   My team
-   Major incidents
-   My work

![Summarize option for incident record](../image/itsm-ma-summarize-option.png)

After the information summary is generated, you can edit and add the information as work notes. Some of the information that is included but not limited to:

-   Incident record details such as issue or short description
-   Activities such as action taken or existing work notes or comments
-   Affected CIs and impacted services

You can also customize the information summary \(prompt\) from Now Assist for ITSM admin console. For more information, see [Customize a Now Assist for IT Service Management \(ITSM\) skill](../../now-assist-itsm/task/cust-now-assist-itsm-skill.md).

![Incident record summarized as work notes](../image/itsm-ma-summarize-worknote.png)

For more information on Now Assist for mobile, see Now Assist for Mobile.

## Activation of incident record summarization skill

To enable the summarization feature in ITSM Mobile Agent application, you must activate or customize the incident summarization skill from the Now Assist for ITSM admin console. For more information on activating and customizing the incident summarization skill, see [Customize a Now Assist for IT Service Management \(ITSM\) skill](../../now-assist-itsm/task/cust-now-assist-itsm-skill.md).

If you have already configured the incident summarization skill in the Now Assist for ITSM application console and then installed ITSM Mobile Agent application, you must do the following actions:

1.  On the Input form actions table, filter the action records by **Label** with `Summarize`, and **Application** with `ITSM Mobile Agent`. The summarization records such as `Incident summarize action` and `Incident summarize action (Reassign)` are displayed.
2.  Select the records and set the **Active** field to `true`.

