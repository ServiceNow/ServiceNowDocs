---
title: Reusable ITSM Virtual Agent pre-built topic blocks
description: Reuse topic blocks to perform common functions in ITSM Virtual Agent conversations, such as creating an incident or performing a search.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Reusable ITSM Virtual Agent pre-built topic blocks

Reuse topic blocks to perform common functions in ITSM Virtual Agent conversations, such as creating an incident or performing a search.

Use the **Type** list on the Topics page in Virtual Agent Designer to sort by **Topic Blocks**. For detailed information about topic blocks, see [Maximizing code reuse with topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/topic-blocks-overview.md).

ITSM Virtual Agent provides the following pre-built topic blocks and templates.

**Note:** Many of these topic blocks are available with the Service Management Virtual Agent Topic Blocks plugin \(com.glideapp.cs.sm\_topic\_blocks\). For more information about plugins, see [ServiceNow Plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ServiceNowPlugins.md)

## Contextual Search

<table id="table_ih3_w5f_hmb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Input parameters

</td></tr><tr><td>

context

</td><td>

The sys\_id of a Search Context \(cxs\_context\_config\) record. Defines what sources are included in the search. For example, sources can include the knowledge base or community.

</td></tr><tr><td>

query

</td><td>

The search keyword entered by a user during a virtual agent conversation.

</td></tr><tr><td>

portal

</td><td>

The portal from which the conversation initiated, such as a service portal or human resources portal. This portal is the URL suffix, such as sp, esc, csm, and hr, from which the search results open.

</td></tr><tr><td>

kb\_knowledge\_base

</td><td>

The sys\_id of a Knowledge Base \(kb\_knowledge\_base\) record.Within context, search only these knowledge base articles.

</td></tr><tr><td class="sub-head" colspan="2">

Output parameters

</td></tr><tr><td>

results\_returned

</td><td>

True if search results are found, otherwise false​.

</td></tr><tr><td>

results\_helpful

</td><td>

True if user responds that search results are helpful, otherwise false​.

</td></tr></tbody>
</table>## Create Incident

This topic block initiates the **Open IT Ticket** conversation topic.

|Name|Description|
|----|-----------|
|Input parameters|
|caller|The name of the user creating an Incident \(incident\) record.|
|short\_description|The short description entered in the Incident \(incident\) record.|
|urgency|The urgency level indicated in the Incident \(incident\) record.|
|description|The description entered in the Incident \(incident\) record.|
|cmdb\_ci|CMDB configuration item.|
|Output parameters|
|created\_incident\_sys\_id|The return sys\_id of a newly created incident​.|

## Create MS Teams Meeting Link \(deprecated\)

This topic block is deprecated. Use [Get MS Teams Meeting Link](employee-experience-va-topicblocks.md) instead.

Users can request a Microsoft Teams meeting link using Virtual Agent. This topic block can be included in other topics. By default, this topic block runs in silent mode, and the output messages are not displayed.

Requirement: [Microsoft Teams Communication spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/msteams-comm.md) \(sn\_msteams\_com\_spk\) plugin

## Create Zoom Meeting Link

For more actions, the [Zoom Meeting Actions](employee-experience-va-topicblocks.md) topic block is also available.

Users can request a Zoom meeting link using Virtual Agent. This topic block can be included in other topics. By default, this topic block runs in silent mode, and the output messages are not displayed.

Requirement: [Zoom spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/zoom-spoke.md)\(com.sn.zoom.spoke\) plugin

## Describe Virtual Machine

Users can get details on any assigned virtual machine \(VM\) instance using the [Manage Virtual Machine topic](manage-virtual-machine.md) in Virtual Agent. Details include Provider, Region, Instance ID, and so forth.

Basic flow:

1.  User specifies which VM to describe, or Virtual Agent provides a list of available VM instances for the user to choose from.
2.  Virtual Agent provides the requested virtual machine details.
3.  To get additional details, users can select the link provided, which redirects them to the [Cloud User Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/cloudmgt-cloud-user-portal.md).

![Describe Virtual Machine topic block.](../image/DescribeVM2.png)

<table id="table_eqd_jz3_vvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input parameter:vm\_name

</td><td>

Name of the virtual machine instance.

</td></tr><tr><td>

Input parameter:vm\_sys\_id

</td><td>

Sys ID of the virtual machine instance in the cmdb\_ci\_vm\_instance table.

</td></tr><tr><td>

Output parameter:incident\_short\_description

</td><td>

Short description for the Incident record, if one is recorded.

</td></tr></tbody>
</table>## Display Password Reset URLs

If Password Reset is enabled on Virtual Agent, and the user has been authenticated, this topic block returns a password reset link. If Password Reset is not enabled, the user is directed to the service desk.

This topic block as one input parameter: **unlock\_account**. If the user has been authenticated, the value is **true**. Otherwise, the value is **false**.

For more information, see [Password Reset for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/password-reset-for-virtual-agent.md).

This topic block has one input parameter: **unlock\_account**. If the user has been authenticated, the value is **true**. Otherwise, the value is **false**.

## Request Catalog Item

For information about this topic block, see [Service Catalog topic blocks in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/request-topic-blocks-va.md).

## Search Catalog Item

For information about this topic block, see [Service Catalog topic blocks in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/request-topic-blocks-va.md).

## Start Virtual Machine

Users can start any assigned VM instance using the [Manage Virtual Machine topic](manage-virtual-machine.md). If the VM is already on or in a state where it cannot be started, Virtual Agent notifies the user.

Basic flow:

1.  User specifies which VM to start, or Virtual Agent provides a list of available VM instances for the user to choose from.
2.  Virtual Agent sends the user an actionable notification when the requested VM starts.

    Virtual Agent also notifies the user if the operation was unsuccessful.

3.  User can choose to see details, request additional instructions to log in to the virtual machine, or skip the notification.
4.  If the user requests additional login instructions, Virtual Agent provides these instructions and the user can confirm if the login was successful.

![Start Virtual Machine topic block.](../image/StartVM3.png)

<table id="table_xxg_rtn_vvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input parameter:vm\_name

</td><td>

Name of the virtual machine instance.

</td></tr><tr><td>

Output parameter:incident\_short\_description

</td><td>

Short description for the Incident record, if one is recorded.

</td></tr></tbody>
</table>## Stop Virtual Machine

Users can stop any assigned VM instance using the [Manage Virtual Machine topic](manage-virtual-machine.md). If the VM is already off or is in a state where it cannot be stopped, Virtual Agent notifies the user.

Basic flow:

1.  User specifies which VM to stop, or Virtual Agent provides a list of available VM instances for the user to choose from.
2.  Virtual Agent sends the user an actionable notification when the requested VM has stopped.

    Virtual Agent also notifies the user if the operation was unsuccessful.

3.  User can choose to see details or skip the notification.

![Stop a virtual machine chatbot dialog.](../image/StopVM1.png)

<table id="table_sfv_stn_vvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input parameter:vm\_name

</td><td>

Name of the virtual machine instance.

</td></tr><tr><td>

Output parameter:incident\_short\_description

</td><td>

Short description for the Incident record, if one is recorded.

</td></tr></tbody>
</table>## Terminate Virtual Machine

Users can terminate any assigned virtual machine \(VM\) instance using the [Manage Virtual Machine topic](manage-virtual-machine.md). If the VM is already terminated or is in a state where it cannot be terminated, Virtual Agent notifies the user.

Basic flow:

1.  User specifies which VM to terminate, or Virtual Agent provides a list of available VM instances for the user to choose from.
2.  Virtual Agent provides the details of the requested VM to terminate.
3.  Terminating a virtual machine is a permanent action, so the user must confirm the operation to continue.
4.  Virtual Agent sends the user an actionable notification when the requested virtual machine has been terminated.

![Terminate Virtual Machine topic block.](../image/TerminateVM3.png)

<table id="table_jw4_ttn_vvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input parameter:vm\_name

</td><td>

Name of the virtual machine instance.

</td></tr><tr><td>

Output parameter:incident\_short\_description

</td><td>

Short description for the Incident record, if one is recorded.

</td></tr></tbody>
</table>## Troubleshoot Cisco Webex

Users can find a solution for common Webex issues. This topic block is used in the [Collaboration Applications](itsm-va-it-issues-generic.md) topic.

If the user is not satisfied with the static help content for the issue, the fallback is AI search or contextual search. The type of search is dictated by the system property **sn\_itsm\_va.fallback\_search\_option**.​

|Name|Description|
|----|-----------|
|Input parameter|
|issue|The user application issue.|
|Output parameter|
|user\_query|Problem string used for search fallback.|

## Troubleshoot Microsoft Teams

Users can find a solution for common Microsoft Teams issues. This topic block is used in the [Collaboration Applications](itsm-va-it-issues-generic.md) topic.

If the user is not satisfied with the static help content for the issue, the fallback is AI search or contextual search. The type of search is dictated by the system property **sn\_itsm\_va.fallback\_search\_option**.​

|Name|Description|
|----|-----------|
|Input parameter|
|issue|The user application issue.|
|Output parameter|
|user\_query|Problem string used for search fallback.|

## Troubleshoot Zoom

Users can find a solution for common Zoom issues. This topic block is used in the [Collaboration Applications](itsm-va-it-issues-generic.md) topic.

If the user is not satisfied with the static help content for the issue, the fallback is AI search or contextual search. The type of search is dictated by the system property **sn\_itsm\_va.fallback\_search\_option**.​

|Name|Description|
|----|-----------|
|Input parameter|
|issue|The user application issue.|
|Output parameters|
|user\_query|Problem string used for search fallback.|
|ticket\_description|Problem string used to create an IT ticket.|

## Virtual Machine Operation AWS

Users can use the Cloud Access Interface to take action on virtual machines provisioned on Amazon AWS. The user must have the sn\_managevm\_va.cai\_vm\_user role.

This topic block is used in the [virtual machine management CAI](manage-virtual-machine.md) pre-built topics. Available actions include Stop, Start, Terminate, or Describe the virtual machine.

## Virtual Machine Operation Azure

Users can use the Cloud Access Interface to take action on virtual machines provisioned on Microsoft Azure. The user must have the sn\_managevm\_va.cai\_vm\_user role.

This topic block is used in the [virtual machine management CAI](manage-virtual-machine.md) pre-built topics. Available actions include Stop, Start, Terminate, or Describe the virtual machine.

-   **[Employee Experience topic blocks](employee-experience-va-topicblocks.md)**  
ITSM Virtual Agent helps you manage meetings in Microsoft Exchange Online. Using the Manage Meetings EXO v1.0 topic, you can schedule, reschedule, and cancel a meeting.

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

