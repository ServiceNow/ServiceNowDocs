---
title: Activate the OT CMDB Search feature
description: If you have the admin role, you can configure the Operational Technology \(OT\) Manager Foundation so that teams can use the OT Configuration Management Database \(CMDB\) search feature in the Industrial Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-manager/activate-ot-cmdb-search.html
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
breadcrumb: [Configuring the OT Manager Foundation, Configure, Operational Technology Manager, Operational Technology]
---

# Activate the OT CMDB Search feature

If you have the admin role, you can configure the Operational Technology \(OT\) Manager Foundation so that teams can use the OT Configuration Management Database \(CMDB\) search feature in the Industrial Workspace.

## Before you begin

Role required: admin

## About this task

Use the AI Admin Hub console to configure the OT Manager Foundation. The console helps you install plugins and configure generative AI skills. For more information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md).

The following table lists the features and skills that you can access from the AI Admin Hub console.

|OTM features|Skills|
|------------|------|
|Gen AI skills for OTM|Analytics Query Generator|

## Procedure

1.  Install the OT Manager Foundation plugin \(sn\_otm\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for OT Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/supporting-information-for-now-assist-otm.md).
    -   For information about the installation process, see [Install plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **All** &gt; **AI Admin Hub**.

3.  Select the **AI Skills** tab.

4.  Expand the **Data &amp; Analytics** category and select **Analytics**.

5.  Find the Analytics Query Generator skill.

6.  On the Analytics Query Generator tile, select **Turn on**.

    **Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

7.  In the Turn on skill confirmation window, select **Turn on** to enable the skill.

8.  Complete the following steps to display the Search CMDB agentic workflow and your conversation with the agent in the ServiceNow Otto panel.

    **Important:** This agentic workflow is turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    2.  In the **Agentic workflows** tab, select the **Search CMDB** agentic workflow.

    3.  Open the **Select a UI display** section.

    4.  Next to the **ServiceNow Otto panel** option, select the **Display** toggle.

9.  Complete the following steps to verify the **Status** toggle is on and confirm the CMDB search AI agent is active and running.

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    2.  In the **AI agents** tab, select the **CMDB CI search AI agent**.

    3.  Open the **Toggle display** section.

    4.  Select the **Status** toggle if the toggle isn't already selected.


**Parent Topic:**[Configuring the OT Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/configuring-na-otm.md)

