---
title: Turn on the RPA bot generation skill
description: Turn on the Robotic Process Automation \(RPA\) bot generation skill to use generative AI to create automations, activities, and automation logic additions from text instructions and preview options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/turn-rpa-bot-generation-skill.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Install ServiceNow Otto for RPA Hub, Configure, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Turn on the RPA bot generation skill

Turn on the Robotic Process Automation \(RPA\) bot generation skill to use generative AI to create automations, activities, and automation logic additions from text instructions and preview options.

## Before you begin

-   Install the ServiceNow Otto for RPA Hub application to add the generative AI capability. For more information, see [Install ServiceNow Otto for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-now-assist-rpa-hub.md).
-   Perform these steps in your ServiceNow instance.
-   Ensure that the AI Search application is enabled on your instance by navigating to **All** &gt; **AI Search** &gt; **AI Search Status**. If AI search is not enabled, select **Request AI Search**.
-   Role required: sn\_nowassist\_admin.nsa\_admin or sn\_skill\_builder.admin

## About this task

**Important:** The ServiceNow Otto for RPA Hub requires a separate subscription to ServiceNow Otto for Creator.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  In the workflow list, select **Creator**.

3.  On the RPA bot generation card, select **Turn on**.

    You view a dialog box with the message "Successfully activated".

4.  On the Successfully activated dialog box, select **Back to skills**.

5.  On the RPA bot generation card, verify that the RPA bot generation skill is activated.


## Result

The following example shows that the RPA bot generation card displays the skill as active.

\[Omitted image "rpa-bot-generation-skill-activated.png"\] Alt text: RPA bot generation card that displays the skill as active.

## What to do next

After activating the RPA bot generation skill, RPA Desktop Design Studio users must relaunch the RPA Desktop Design Studio application to apply the modified settings.

**Related topics**  


[Robotic Process Automation \(RPA\) bot generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/rpa-bot-generation.md)

