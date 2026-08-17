---
title: Configure HR AI voice agents
description: Enable employees to complete tasks, resolve issues, and access information through a conversational experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-hrsd/configure-voice-agents.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure HR AI voice agents

Enable employees to complete tasks, resolve issues, and access information through a conversational experience.

## Before you begin

Role required: sn\_aia\_admin, sn\_voice\_aia.admin, or sn\_hr\_voice\_aia.admin

Verify you have the following applications installed:

-   [Case and Knowledge Management \[com.sn\_hr\_core\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/activate-case-and-knowledge-management-scoped.md)
-   ServiceNow Otto for Platform \[sn\_genai\_platform\].
-   [ServiceNow Otto for HRSD \[sn\_hr\_gen\_ai\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

## About this task

HR AI voice agents are conversational agents designed to handle routine employee inquiries and HR transactions through voice interactions. To enable AI voice agent functionality, you must complete configuration steps on the ServiceNow® AI Platform. Then, you will activate the specific HR AI voice agents you want to deploy. If you will enable AI voice agents that use data from third-party apps like Oracle HCM, configure the integration. After activation, you can test agent functionality by calling the assigned telephony number. This validates voice interaction quality, agent responses, and integration workflows before end-user rollout.

## Procedure

1.  Perform these steps to configure AI voice agents on the ServiceNow® AI Platform:

    1.  [Install AI voice agents plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-ai-voice-agents-plugins.md):

        -   ServiceNow Otto for Voice \[sn\_voice\_aia\] delivers AI voice capabilities
        -   HR Voice AI Agents \[sn\_hr\_voice\_aia\] contains AI voice agents for HR Service Delivery
    2.  [Configure authentication factors for AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configuring-authentication-factors-for-ai-voice-agents.md).

    3.  [Integrate with a third-party Contact Center as a Service \(CCaaS\) provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md).

    4.  [Create an AI voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-an-ai-voice-service.md).

2.  Activate the HR AI voice agents:

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** and select the AI agents tab.

    2.  Filter the agents by `Application is HR AI Voice Agents`.

    For more information on the HR-specific agents, see [HR AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-voice-ai-agents.md).

3.  For the following AI voice agents, perform these additional configuration steps.

<table id="table_kss_zbp_bkc"><thead><tr><th>

AI agent

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

HR Case assistant

</td><td>

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.
2.  Locate and open **HR Case**.
3.  Select **Index selected tables**.


</td></tr><tr><td>

Employee Details Updater, Holiday Calendar, Retrieve Worker Profile, Time off Requester

</td><td>

1.  Install the Oracle plugins:
    -   sn\_oracle\_hcm\_spk \(4.1.1 or later\)
    -   sn\_hr\_oracle\_hcm \(1.0.10 or later\)
    -   sn\_hr\_integr\_fw \(3.8.1 or later\)
    -   sn\_hr\_oracle\_adv \(1.2.1 or later\)
    -   com.glide.hub.integrations.enterprise
2.  Follow the steps to [Set up the Oracle HCM Cloud spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/set-up-the-oracle-hcm-spoke.md)


</td></tr></tbody>
</table>4.  Test the execution of the HR AI Voice agents by calling the telephony number to verify that the agent functions the way you expect: [Test a voice assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/test-a-voice-assistant.md).


## What to do next

Assign roles to admins and users to grant them access to Voice features. See [Components installed with voice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/components-installed-voice-agents.md).

**Parent Topic:**[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

**Related topics**  


[HR AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-voice-ai-agents.md)

