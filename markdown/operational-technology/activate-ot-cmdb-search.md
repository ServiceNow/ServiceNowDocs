---
title: Activate the OT CMDB Search feature
description: If you have the admin role, you can configure the Operational Technology \(OT\) Manager Foundation so that teams can use the OT Configuration Management Database \(CMDB\) search feature in the Industrial Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, OT Manager Foundation, Operational Technology]
---

# Activate the OT CMDB Search feature

If you have the admin role, you can configure the Operational Technology \(OT\) Manager Foundation so that teams can use the OT Configuration Management Database \(CMDB\) search feature in the Industrial Workspace.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure the OT Manager Foundation. This console contains everything that you must install the plugins and configure the generative AI skills. For additional information, see [Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

|OTM features|Skills|
|------------|------|
|Gen AI skills for OTM|Analytics Query Generator|

## Procedure

1.  Install the OT Manager Foundation plugin \(sn\_otm\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for OT Manager Foundation](../concept/supporting-information-for-now-assist-otm.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin**.

3.  Select the **Now Assist Skills** tab.

4.  In the **Platform** category, find the Analytics Query Generator skill.

5.  On the Analytics Query Generator tile, select **Turn on**.

    **Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

6.  In the Turn on skill confirmation window, select **Turn on** to activate the skill.

7.  Enable the Search CMDB agentic workflow in the Now Assist panel.

    **Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    2.  Under the **Agentic workflows** tab, select the **Search CMDB** agentic workflow.

    3.  In the **Select a UI display** screen next to the **Now Assist panel** option, select the **Display** toggle so that the conversation with the agent is displayed in the Now Assist panel.

8.  To ensure the CMDB search AI agent is active and running, ensure the **Status** toggle is on.

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    2.  Under the **AI agents** tab, select the **CMDB CI search AI agent**.

    3.  In the **Toggle display** screen, select the **Status** toggle if the toggle isn't already selected.


**Parent Topic:**[Configuring the OT Manager Foundation](../concept/configuring-na-otm.md)

