---
title: Configure HR AI voice agents
description: Enable employees to complete tasks, resolve issues, and access information through a conversational experience.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure HR AI voice agents

Enable employees to complete tasks, resolve issues, and access information through a conversational experience.

## Before you begin

Role required: sn\_voice\_aia.admin or sn\_hr\_voice\_aia.admin

Install the following plugins:

-   Now Assist for HR Service Delivery \(HRSD\) plugin \[sn\_hr\_gen\_ai\]
-   Now Assist Voice \[sn\_voice\_aia\]
-   HR Voice AI Agents \[sn\_hr\_voice\_aia\]

## Procedure

1.  Follow the steps to Create an AI voice assistant

2.  Activate the HR AI voice agents.

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** and select the AI agents tab.

    2.  Filter the agents by `Application is HR AI Voice Agents`.

    For more information on the HR-specific agents, see [HR AI voice agents](../concept/now-assist-hrsd-voice-ai-agents.md).

3.  For the following AI voice agents, perform these additional configuration steps.

<table id="choicetable_skr_2cp_3hc"><thead><tr><th align="left" id="d609096e125">

AI agent

</th><th align="left" id="d609096e128">

Steps

</th></tr></thead><tbody><tr><td id="d609096e134">

**HR Case assistant**

</td><td>

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.
2.  Locate and open **HR Case**.
3.  Select **Index selected tables**.


</td></tr><tr><td id="d609096e176">

**Employee Details Updater, Holiday Calendar, Retrieve Worker Profile, Time off Requester**

</td><td>

1.  Install the Oracle plugins:
    -   sn\_oracle\_hcm\_spk \(4.1.1 or later\)
    -   sn\_hr\_oracle\_hcm \(1.0.10 or later\)
    -   sn\_hr\_integr\_fw \(3.8.1 or later\)
    -   sn\_hr\_oracle\_adv \(1.2.1 or later\)
    -   com.glide.hub.integrations.enterprise
2.  Follow the steps to Set up the Oracle HCM Cloud spoke


</td></tr></tbody>
</table>
## What to do next

Test the execution of the HR AI Voice agents by calling the telephony number to verify that the agent functions the way you expect. For more information, see Test a voice assistant.

Assign roles to admins and users to grant them access to Voice features. See [Components installed with voice](../reference/components-installed-voice-agents.md).

**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md)

**Related topics**  


[HR AI voice agents](../concept/now-assist-hrsd-voice-ai-agents.md)

