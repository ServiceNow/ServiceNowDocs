---
title: Customize a Now Assist Virtual Agent topic
description: Copy and customize a core ITSM Virtual Agent topic and use that topic to track the status of common IT-related tasks using Now Assist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-customize-itsm-llm-topic.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configure in Virtual Agent, Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Customize a Now Assist Virtual Agent topic

Copy and customize a core ITSM Virtual Agent topic and use that topic to track the status of common IT-related tasks using Now Assist.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Select a topic template.

    |Template|Usage|
    |--------|-----|
    |Check IT Ticket Status \(Template\)-LLM|Check the status and progress of IT tickets and incidents.|
    |Escalate IT Ticket \(Template\)-LLM|Escalate an IT ticket or incident that's already open or by reopening a closed one.|
    |Open IT Ticket \(Template\)-LLM|Create an IT ticket or incident.|
    |Service Disruptions \(Template\)-LLM|Check the status of outages or service disruptions.|

3.  Select a template for a topic to track the status.

    **Note:** The images show an example of the Service Disruption flow. You can follow the same actions for any core ITSM topic template.

4.  Select the Topic actions icon at the top-right corner of the screen and select **Duplicate**.

    \[Omitted image "itsm-now-assist-service-disruptions-duplicate.png"\] Alt text: Duplicate a service disruption template

5.  In the **Name** field, enter the name for the topic you want to use for the summarization.

    \[Omitted image "itsm-now-assist-service-disruption-name.png"\] Alt text: Enter a name for the duplicated Service Disruption topic

6.  Select **Save**.

7.  In the topic you've duplicated, select the **Properties** tab.

    \[Omitted image "itsm-now-assist-service-disruptions-properties.png"\] Alt text: Configure a VA topic for Now Assist in Virtual Agent

8.  Enable the following check boxes:

    -   Now Assist in Virtual Agent \(default\).
    -   Default Now Assist Panel - Platform.
9.  Select **Save**.

10. Select **Publish**.

    **Note:** If you have multiple topics to summarize the same skill, you can unpublish the ones that you do not intend to use.


