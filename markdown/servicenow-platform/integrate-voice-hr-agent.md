---
title: Integrating ServiceNow Voice for HR
description: The ServiceNow Voice for HR Agent Workspace provides seamless interactive voice response \(IVR\) and calling experiences for your employees and agents by integrating a cloud contact center provider with the robust capabilities of the Agent Workspace for HR Case Management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrating ServiceNow Voice for HR

The ServiceNow Voice for HR Agent Workspace provides seamless interactive voice response \(IVR\) and calling experiences for your employees and agents by integrating a cloud contact center provider with the robust capabilities of the Agent Workspace for HR Case Management.

The ServiceNow Voice for HR provides the following capabilities:

-   An inbound contact flow to define the employee experience in an IVR.
-   An outbound contact flow to connect with employee contacts from the phone number field displayed in any of the ServiceNow application interfaces.
-   Operation handlers to configure automated interactions for employee service cases.

## Employee experience with ServiceNow Voice for HR

The following example provides an overview of how an employee uses ServiceNow Voice for HR to resolve their HR requests and issues.

An employee calls the general HR phone number with a request. The employee provides information via the interactive voice response \(IVR\). Using the provided information, ServiceNow Voice for HR tries to identify the caller.

If the caller is identified as an existing employee in HR Agent Workspace, Voice reads a personal greeting to the employee and offers automated interactions to enable the employee to independently address their request. If the employee cannot resolve their request using the IVR, the system routes the call to a live agent.

If the caller is not identified, the call is routed to a live agent.

## Agent experience with ServiceNow Voice for HR

Once installed, ServiceNow Voice appears as a pop-up in the HR Agent Workspace where agents can do the following:

-   Indicate availability to receive calls on the agent softphone

    ![Agent marks themselves as available and receives incoming calls](../image/voice-hr-agent3.png)

-   Preview caller information before accepting an inbound call.

    ![When the softphone receives an incoming call, HR Agent Workspace displays the caller information](../image/voice-hr-agent2.png)

-   View the call transcript, hear the recording, and review the call analysis in the interaction related list.

    ![Each interaction record contains data related to the call that can be referenced in the future](../image/voice-hr-agent5.png)

-   Make outbound calls to connect with a employee and automatically capture interaction details to simplify data entry

## Configuration

ServiceNow Voice for HR \(sn\_cti\_hr\_cnt\) is activated from the store and requires the following dependency applications:

<table id="table_fmc_lzj_5mb"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNow Voice with Amazon Connect \[sn\_cti\_amzn\_cct\]

</td><td>

Integrates the ServiceNow instance with the Amazon Connect server. For information about the components installed with this application, see [Components installed with Amazon Connect Integration with ServiceNow Voice](../reference/instld-with-amazn-cnct-integ.md)

</td></tr><tr><td>

Agent Workspace for HR Case Management\[sn\_hr\_agent\_ws\]

</td><td>

Enables call recording, transcription, and sentiment analysis for ServiceNow Voice with Workspace experience.

</td></tr><tr><td>

ServiceNow Voice for HR Agent Workspace\[sn\_cti\_hr\_cnt\]

</td><td>

Provides the framework that supports the integration with your third-party phone system.

</td></tr></tbody>
</table>You must install the dependency applications first, then install ServiceNow Voice for HR. For more information, see [Install ServiceNow Voice for HR](../../human-resources/task/install-voice-hr.md).

ServiceNow Voice for HR creates an interaction record for every call between an employee and an HR agent with the IMS prefix. These records contain related lists of details relating to the employee and interaction. To maximize the full feature capability, add the Interaction record to the HR Agent workspace. For more information, see [Add Interaction Related Records to HR Agent workspace](../task/add-interaction-related-records.md).

-   **[Install ServiceNow Voice for HR](../../human-resources/task/install-voice-hr.md)**  
You can install ServiceNow Voice for HR if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Add Interaction Related Records to HR Agent workspace](../task/add-interaction-related-records.md)**  
ServiceNow Voice for HR creates an interaction record for every call between an employee and an HR agent, which contain related lists of details relating to the employee and interaction. To maximize the full feature capability, add the Interaction record to the HR Agent workspace.

**Parent Topic:**[Integrating Voice with other applications](integrate-ccc-other-apps.md)

