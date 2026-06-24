---
title: Configure Information Requests service channel
description: Change the default Information Requests service channel attributes in Advanced Work Assignment to control how public sector information requests are routed and assigned to government agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/government-industry/psds-awa-configure-ir.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Automatically route information requests using Advanced Work Assignment, Information Request Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure Information Requests service channel

Change the default Information Requests service channel attributes in Advanced Work Assignment to control how public sector information requests are routed and assigned to government agents.

## Before you begin

-   [Activate the Advanced Work Assignment plugin \(com.glide.awa\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/advanced-work-assignment/awa-activate.md).
-   [Activate the Agent Chat plugin \(com.glide.interaction.awa\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/advanced-work-assignment/awa-related-plugins.md).
-   [Install the Information Request Playbook application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/government-industry/install-psds-information-request-playbook.md).

Role required: sn\_gsm\_info\_req.admin, awa\_admin, admin

## About this task

You can modify the context and attributes for [service channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/advanced-work-assignment/awa-service-channels.md) in AWA. For the Information Requests service channel, use the Public Sector Requests assignment group to specify the agents handling information requests. You can also add advanced conditions to filter the routing conditions in the Information Request service channel, or change queue settings, such as assignment rules.

## Procedure

1.  Configure the Information Requests service channel by modifying the default attributes as needed.

<table id="choicetable_rw4_m3w_s4b"><thead><tr><th align="left" id="d32880e95">

Options

</th><th align="left" id="d32880e98">

Steps

</th></tr></thead><tbody><tr><td id="d32880e104">

**Enable the Information Request service channel**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** **Presence States**.
2.  Select the **Available** record.
3.  If prompted, move to the **Global** application to edit the record.
4.  In the Presence State form, go to the**Service Channels** field and move the Information Request channel to the **Selected** column.
5.  Select **Update**.


</td></tr><tr><td id="d32880e161">

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


</td></tr><tr><td id="d32880e239">

**Configure the Information Requests queue**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.
2.  Select the Information Requests queue.

3.  Change other settings as needed, for example the assignment rule that determines Assignment Eligibility.

4.  Select **Update**.
For more information on queue settings, see [Create a work item queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/advanced-work-assignment/awa-create-queue.md).

</td></tr><tr><td id="d32880e287">

**Change Inbox card layouts for information request items in CSM Configurable Workspace**

</td><td>

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Service Channels** and select the Information Request channel.
2.  Select the **Inbox Layouts** related link.
3.  Select the layout and edit the fields to be updated.
4.  Select **Update**.
For more information on changing inbox card layouts, see [Create or modify an inbox layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/advanced-work-assignment/awa-modify-inbox-layout.md).

</td></tr></tbody>
</table>
