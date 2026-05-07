---
title: Configure Advanced Work Assignment for Public Sector Digital Services
description: Use the Advanced Work Assignment \(AWA\) for Public Sector Digital Services feature to automatically assign work items to agents based on their availability, capacity, and skills. AWA for Public Sector Digital Services pushes work to qualified agents using work item queues, routing conditions, and assignment criteria that you define. Agents see their assignments in their Agent Workspace inbox.Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign social benefits requests to designated agents.Change the default Social Benefit Requests service channel attributes in Advanced Work Assignment to control how public sector social benefit requests are routed and assigned to government agents.Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign license/permit requests to designated agents.Change the default License and Permit Requests service channel attributes in Advanced Work Assignment to control how public sector license and permit requests are routed and assigned to government agents.Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign information requests, such as public records requests, to designated agents.Change the default Information Requests service channel attributes in Advanced Work Assignment to control how public sector information requests are routed and assigned to government agents.Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign public sector service requests, such as non-emergency requests, to designated agents.Change the default Service Requests service channel attributes in Advanced Work Assignment to control how public sector service requests are routed and assigned to government agents.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Case Routing and Assignment, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Advanced Work Assignment for Public Sector Digital Services

Use the Advanced Work Assignment \(AWA\) for Public Sector Digital Services feature to automatically assign work items to agents based on their availability, capacity, and skills. AWA for Public Sector Digital Services pushes work to qualified agents using work item queues, routing conditions, and assignment criteria that you define. Agents see their assignments in their Agent Workspace inbox.

## Plugins

The Advanced Work Assignment for Public Sector Digital Services feature is available with the Customer Service plugin \(com.sn\_customerservice\).

To use the chat feature with AWA for Public Sector Digital Services, you must also activate the Agent Chat plugin \(com.glide.interaction.awa\).

For more information, see [Activate related plugins for Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-related-plugins&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Inbox layouts

Three chat inbox layouts are included with the Chat service channel.

|Chat Layout|Included Fields|
|-----------|---------------|
|Default Chat Layout|Short description|
|Business Contact Chat Layout|Short description, Business, Business Contact, and Case Type|
|Constituent Chat Layout|Short description, Constituent, Case Type|

Two case inbox layouts are included with the Case service channel.

|Case Layout|Included Fields|
|-----------|---------------|
|Default Case Layout|Short description, Business Contact, Account, Priority, Category|
|Consumer Case Layout|Short description, Constituent, Case Type|

## Variable work item sizing

Organizations may like to size cases based on the complexity of the case, time and effort required to complete work. This helps in estimating agent utilization accurately. Advance work assignment currently treats every case as one unit of work. However, sometimes, certain cases may require more work than others. These cases may account for a greater share of an agent’s capacity. Work item sizing allows to size the case differently based on the case attributes. For more information, see [Service channel capacity and utilization](https://www.servicenow.com/docs/access?context=awa-service-channel-capacity&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Agent affinity

Agent Affinity is an Advanced Work Assignment enhancement that enables you to streamline the routing of work items. Advanced Work Assignment automatically assigns work items based on historical, task-based, or account team affinity. For more information about agent affinity, see [Using Agent Affinity](https://www.servicenow.com/docs/access?context=awa-agent-affinity-concept&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

**Related topics**  


[Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)

## Automatically route social benefit requests using Advanced Work Assignment

Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign social benefits requests to designated agents.

The Social Benefits Playbook application provides the following items that are used in AWA to automatically route and assign social benefits requests:

-   **Social Benefits Request service channel** - The default service channel for routing incoming public sector social benefits requests to specific government agents. This service channel includes related attributes that define the default conditions for determining the items handled in the channel, work queue associated with agent assignment groups, agent inbox layouts, and more.
-   **Public Sector Social Benefits Request assignment group** - The default assignment group that identifies the agents handling public sector social benefits requests. Agent assignments are based on agent availability, capacity, and skills.
-   **Public Sector Social Benefits Requests queue** - The default queue to which public sector social benefits requests are routed.
-   **Inbox layouts** - The default card layouts for social benefits request items displayed in the agent inbox view of CSM Configurable Workspace:
    -   Constituent Social Benefits Layout: Includes **Short description**, **Constituent**, and **Case Type** fields.
    -   Business Social Benefits Layout: Includes **Short description**, **Business**, **Business Contact**, and **Case Type** fields.

As an admin, you can enable and disable Advanced Work Assignment for Social Benefits Request cases, as well as change the default attributes for the Social Benefits Requests service channel, such as the related assignment group and queue settings. For details, see [Configure Social Benefit Requests service channel](awa-psds-overview.md#).

## Configure Social Benefit Requests service channel

Change the default Social Benefit Requests service channel attributes in Advanced Work Assignment to control how public sector social benefit requests are routed and assigned to government agents.

### Before you begin

-   [Activate the Advanced Work Assignment plugin \(com.glide.awa\)](https://www.servicenow.com/docs/access?context=awa-activate&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   [Activate the Agent Chat plugin \(com.glide.interaction.awa\)](https://www.servicenow.com/docs/access?context=awa-related-plugins&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   [Install the Social Benefits Playbook application](../task/install-psds-social-benefits-playbook.md).

Role required: admin, awa\_admin

### About this task

You can modify the context and attributes for [service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) in AWA. For the Social Benefit Requests service channel, use the Public Sector Requests assignment group to specify the agents handling social benefit requests. You can also add advanced conditions to filter the routing conditions in the Social Benefit Request service channel, or change queue settings, such as assignment rules.

### Procedure

1.  Configure the Social Benefit Requests service channel by modifying the default attributes as needed.

<table id="choicetable_rw4_m3w_s4b"><thead><tr><th align="left" id="d34504e456">

Options

</th><th align="left" id="d34504e459">

Steps

</th></tr></thead><tbody><tr><td id="d34504e465">

**Enable the Social Benefit Request service channel**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** **Presence States**.
2.  Select the **Available** record.
3.  If prompted, move to the **Global** application to edit the record.
4.  In the Presence State form, go to the**Service Channels** field and move the Social Benefit Request channel to the **Selected** column.
5.  Select **Update**.


</td></tr><tr><td id="d34504e522">

**Add members \(agents\) to the Public Sector Requests assignment group**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Management** &gt; **Groups**.
2.  Select the Social Benefit Requests group.
3.  In the Group form, navigate to the **Group Members** related list and review the list of example members.

Use the examples to determine the government agents, managers, and their associated roles to be added to the assignment group.

**Note:** Agents and managers added to this assignment group must also have the awa\_agent role.

4.  In the **Group Members** related list, click **Edit** to add members to the group.
5.  Select **Edit**.
6.  Select one or more names in the **Collection** list and move them to the **Group Members** list.
7.  Select **Save**.


</td></tr><tr><td id="d34504e604">

**Configure the Social Benefit Requests queue**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.
2.  Select the Social Benefit Requests queue.

3.  Change other settings as needed, for example the assignment rule that determines Assignment Eligibility.

4.  Select **Update**.
For more information on queue settings, see [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td id="d34504e656">

**Change Inbox card layouts for Social Benefit request items in CSM Configurable Workspace**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Service Channels** and select the Social Benefit Request channel.
2.  Select the **Inbox Layouts** related link.
3.  Select the layout and edit the fields to be updated.
4.  Select **Update**.
For more information on changing inbox card layouts, see [Create or modify an inbox layout](https://www.servicenow.com/docs/access?context=awa-modify-inbox-layout&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr></tbody>
</table>
## Automatically route license and permit requests using Advanced Work Assignment

Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign license/permit requests to designated agents.

The License and Permit Playbook application provides the following items that are used in AWA to automatically route and assign license/permit requests:

-   **License and Permit Request service channel** - The default service channel for routing incoming public sector license/permit requests to specific government agents. This service channel includes related attributes that define the default conditions for determining the items handled in the channel, work queue associated with agent assignment groups, agent inbox layouts, and more.
-   **Public Sector License and Permit Request assignment group** - The default assignment group that identifies the agents handling public sector license/permit requests. Agent assignments are based on agent availability, capacity, and skills.
-   **Public Sector License and Permit Requests queue** - The default queue to which public sector license/permit requests are routed.
-   **Inbox layouts** - The default card layouts for license/permit request items displayed in the agent inbox view of CSM Configurable Workspace:
    -   Constituent License/Permit Layout: Includes **Short description**, **Constituent**, and **Case Type** fields.
    -   Business License/Permit Layout: Includes **Short description**, **Business**, **Business Contact**, and **Case Type** fields.

As an admin, you can enable and disable Advanced Work Assignment for License/Permit Request cases, as well as change the default attributes for the License/Permit Requests service channel, such as the related assignment group and queue settings. For details, see [Configure License and Permits Requests service channel](awa-psds-overview.md#).

## Configure License and Permits Requests service channel

Change the default License and Permit Requests service channel attributes in Advanced Work Assignment to control how public sector license and permit requests are routed and assigned to government agents.

### Before you begin

-   [Activate the Advanced Work Assignment plugin \(com.glide.awa\)](https://www.servicenow.com/docs/access?context=awa-activate&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   [Activate the Agent Chat plugin \(com.glide.interaction.awa\)](https://www.servicenow.com/docs/access?context=awa-related-plugins&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   [Install the License and Permit Request Playbook application](../task/install-psds-license-permit-request-playbook.md).

Role required: awa\_admin, admin

### About this task

You can modify the context and attributes for [service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) in AWA. For the License and Permit Requests service channel, use the Public Sector Requests assignment group to specify the agents handling license and permit requests. You can also add advanced conditions to filter the routing conditions in the License and Permit Request service channel, or change queue settings, such as assignment rules.

### Procedure

1.  Configure the License and Permits Requests service channel by modifying the default attributes as needed.

<table id="choicetable_rw4_m3w_s4b"><thead><tr><th align="left" id="d34504e915">

Options

</th><th align="left" id="d34504e918">

Steps

</th></tr></thead><tbody><tr><td id="d34504e924">

**Enable the License and Permit Request service channel**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** **Presence States**.
2.  Select the **Available** record.
3.  If prompted, move to the **Global** application to edit the record.
4.  In the Presence State form, go to the**Service Channels** field and move the License and Permit Request channel to the **Selected** column.
5.  Select **Update**.


</td></tr><tr><td id="d34504e981">

**Add members \(agents\) to the Public Sector Requests assignment group**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Management** &gt; **Groups**.
2.  Select the License and Permits Requests group.
3.  In the Group form, navigate to the **Group Members** related list and review the list of example members.

Use the examples to determine the government agents, managers, and their associated roles to be added to the assignment group.

**Note:** Agents and managers added to this assignment group must also have the awa\_agent role.

4.  In the **Group Members** related list, click **Edit** to add members to the group.
5.  Select **Edit**.
6.  Select one or more names in the **Collection** list and move them to the **Group Members** list.
7.  Select **Save**.


</td></tr><tr><td id="d34504e1063">

**Configure the License and Permit Requests queue**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.
2.  Select the License and Permits Requests queue.

3.  Change other settings as needed, for example the assignment rule that determines Assignment Eligibility.

4.  Select **Update**.
For more information on queue settings, see [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td id="d34504e1115">

**Change Inbox card layouts for License and Permits request items in CSM Configurable Workspace**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Service Channels** and select the License and Permits Request channel.
2.  Select the **Inbox Layouts** related link.
3.  Select the layout and edit the fields to be updated.
4.  Select **Update**.
For more information on changing inbox card layouts, see [Create or modify an inbox layout](https://www.servicenow.com/docs/access?context=awa-modify-inbox-layout&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr></tbody>
</table>
## Automatically route information requests using Advanced Work Assignment

Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign information requests, such as public records requests, to designated agents.

The Information Request Playbook application provides the following items that are used in AWA to automatically route and assign public sector information requests:

-   **Information Request service channel** - The default service channel for routing incoming public sector information requests to specific government agents. This service channel includes related attributes that define the default conditions for determining the items handled in the channel, work queue associated with agent assignment groups, agent inbox layouts, and more.
-   **Public Sector Information Request assignment group** - The default assignment group that identifies the agents handling public sector information requests. Agent assignments are based on agent availability, capacity, and skills.
-   **Public Sector Information Requests queue** - The default queue to which public sector information requests are routed.
-   **Inbox layouts** - The default card layouts for information request items displayed in the agent inbox view of CSM Configurable Workspace:
    -   Constituent Information Request layout: Includes **Short description**, **Constituent**, and **Service** fields.
    -   Business Information Request layout: Includes **Short description**, **Business**, **Business Contact**, and **Service** fields.
    -   Generic Information Request layout: Includes **Short description** and **Service** fields.

As an admin, you can enable and disable Advanced Work Assignment for Information Request cases, as well as change the default attributes for the Information Requests service channel, such as the related assignment group and queue settings. For details, see [Configure Information Requests service channel](awa-psds-overview.md#).

## Configure Information Requests service channel

Change the default Information Requests service channel attributes in Advanced Work Assignment to control how public sector information requests are routed and assigned to government agents.

### Before you begin

-   [Activate the Advanced Work Assignment plugin \(com.glide.awa\)](https://www.servicenow.com/docs/access?context=awa-activate&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   [Activate the Agent Chat plugin \(com.glide.interaction.awa\)](https://www.servicenow.com/docs/access?context=awa-related-plugins&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   [Install the Information Request Playbook application](../task/install-psds-information-request-playbook.md).

Role required: sn\_gsm\_info\_req.admin, awa\_admin, admin

### About this task

You can modify the context and attributes for [service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) in AWA. For the Information Requests service channel, use the Public Sector Requests assignment group to specify the agents handling information requests. You can also add advanced conditions to filter the routing conditions in the Information Request service channel, or change queue settings, such as assignment rules.

### Procedure

1.  Configure the Information Requests service channel by modifying the default attributes as needed.

<table id="choicetable_rw4_m3w_s4b"><thead><tr><th align="left" id="d34504e1383">

Options

</th><th align="left" id="d34504e1386">

Steps

</th></tr></thead><tbody><tr><td id="d34504e1392">

**Enable the Information Request service channel**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** **Presence States**.
2.  Select the **Available** record.
3.  If prompted, move to the **Global** application to edit the record.
4.  In the Presence State form, go to the**Service Channels** field and move the Information Request channel to the **Selected** column.
5.  Select **Update**.


</td></tr><tr><td id="d34504e1449">

**Add members \(agents\) to the Public Sector Requests assignment group**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Management** &gt; **Groups**.
2.  Select the Information Requests group.
3.  In the Group form, navigate to the **Group Members** related list and review the list of example members.

Use the examples to determine the government agents, managers, and their associated roles to be added to the assignment group.

**Note:** Agents and managers added to this assignment group must also have the awa\_agent role.

4.  In the **Group Members** related list, click **Edit** to add members to the group.
5.  Select **Edit**.
6.  Select one or more names in the **Collection** list and move them to the **Group Members** list.
7.  Select **Save**.


</td></tr><tr><td id="d34504e1527">

**Configure the Information Requests queue**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.
2.  Select the Information Requests queue.

3.  Change other settings as needed, for example the assignment rule that determines Assignment Eligibility.

4.  Select **Update**.
For more information on queue settings, see [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td id="d34504e1575">

**Change Inbox card layouts for information request items in CSM Configurable Workspace**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Service Channels** and select the Information Request channel.
2.  Select the **Inbox Layouts** related link.
3.  Select the layout and edit the fields to be updated.
4.  Select **Update**.
For more information on changing inbox card layouts, see [Create or modify an inbox layout](https://www.servicenow.com/docs/access?context=awa-modify-inbox-layout&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr></tbody>
</table>
## Automatically route service requests using Advanced Work Assignment

Use the ServiceNow Advanced Work Assignment \(AWA\) application to route and assign public sector service requests, such as non-emergency requests, to designated agents.

The Service Request Playbook application provides the following items that are used in AWA to automatically route and assign public sector service requests:

-   **Service Requests service channel** - The default service channel for routing incoming public sector service requests to specific government agents. This service channel includes related attributes that define the default conditions for determining the items handled in the channel, work queue associated with agent assignment groups, agent inbox layouts, and more.
-   **Public Sector Requests assignment group** - The default assignment group that identifies the agents handling public sector service requests. Agent assignments are based on agent availability, capacity, and skills.
-   **Public Service Requests queue** - The default queue to which public sector service requests are routed.
-   **Inbox layouts** - The default card layouts for service request items displayed in the agent inbox view of CSM Configurable Workspace:
    -   Constituent Service Request layout: Includes **Short description**, **Constituent**, and **Service** fields.
    -   Business Service Request layout: Includes **Short description**, **Business**, **Business Contact**, and **Service** fields.
    -   Generate Service Request Layout: Displayed when anonymous users submit service requests. Includes **Short description** and **Service** fields

As an admin, you can enable and disable Advanced Work Assignment for Service Request cases, as well as change the default attributes for the Service Requests service channel, such as the related assignment group and queue settings. For details, see [Configure Service Requests service channel](awa-psds-overview.md#).

## Configure Service Requests service channel

Change the default Service Requests service channel attributes in Advanced Work Assignment to control how public sector service requests are routed and assigned to government agents.

### Before you begin

-   [Activate the Advanced Work Assignment plugin \(com.glide.awa\)](https://www.servicenow.com/docs/access?context=awa-activate&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   [Activate the Agent Chat plugin \(com.glide.interaction.awa\)](https://www.servicenow.com/docs/access?context=awa-related-plugins&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   [Install the Service Request Playbook application](../task/install-psds-service-request-playbook.md).

Role required: awa\_admin or admin

### About this task

You can modify the context and attributes for [service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) in AWA. For the Service Requests service channel, use the Public Sector Requests assignment group to specify the agents handling service requests. You can also add advanced conditions to filter the routing conditions in the Service Request service channel, or change queue settings, such as assignment rules.

### Procedure

1.  Configure the Service Requests service channel by modifying the default attributes as needed.

<table id="choicetable_rw4_m3w_s4b"><thead><tr><th align="left" id="d34504e1844">

Options

</th><th align="left" id="d34504e1847">

Steps

</th></tr></thead><tbody><tr><td id="d34504e1853">

**Enable the Service Request service channel**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** **Presence States**.
2.  Select the **Available** record.
3.  In the Presence State form, go to the**Service Channels** field and move the Service Request channel to the **Selected** column.
4.  Select **Update**.


</td></tr><tr><td id="d34504e1904">

**Add members \(agents\) to the Public Sector Requests assignment group**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Management** &gt; **Groups**.
2.  Select the Public Service Requests group.
3.  In the Group form, navigate to the **Group Members** related list and review the list of example members.

Use the examples to determine the government agents, managers, and their associated roles to be added to the assignment group.

**Note:** Agents and managers added to this assignment group must also have the awa\_agent role.

4.  In the **Group Members** related list, click **Edit** to add members to the group.
5.  Select **Edit**.
6.  Select one or more names in the **Collection** list and move them to the **Group Members** list.
7.  Select **Save**.


</td></tr><tr><td id="d34504e1982">

**Configure the Public Service Requests queue**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.
2.  Select the Public Services Requests queue.

3.  Change other settings as needed, for example the assignment rule that determines Assignment Eligibility.

4.  Select **Update**.
For more information on queue settings, see [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td id="d34504e2030">

**Change Inbox card layouts for service request items in CSM Configurable Workspace**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Service Channels** and select the Service Request channel.
2.  Select the **Inbox Layouts** related link.
3.  Select the layout and edit the fields to be updated.
4.  Select **Update**.
For more information on changing inbox card layouts, see [Create or modify an inbox layout](https://www.servicenow.com/docs/access?context=awa-modify-inbox-layout&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr></tbody>
</table>
