---
title: IT Service Management AI agent collection Manage Microsoft 365 group members agentic workflow
description: Use the Microsoft 365 group membership AI agent to manage users in the Microsoft 365 email distribution list.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [ITSM, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Manage Microsoft 365 group members agentic workflow

Use the Microsoft 365 group membership AI agent to manage users in the Microsoft 365 email distribution list.

## Manage Microsoft 365 group members agentic workflow overview

Using the Manage Microsoft 365 group members agentic workflow, add or remove names and their email address from the Microsoft 365 email distribution list.

**Important:**

-   To enable the Manage Microsoft 365 group members agentic workflow, you must install the Microsoft Entra ID spoke. For more information, see [Microsoft Entra ID Spoke \(formerly Microsoft Azure Active Directory spoke\)](https://www.servicenow.com/docs/access?context=microsoft-azure-ad-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
-   After you add or remove users to the group using the Microsoft 365 agentic workflow, follow the instructions listed in the table.

<table id="table_xvf_npv_w2c"><thead><tr><th>

If

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

You want the workflow output of adding or removing users to go through an approval process.

</td><td>

1.  [Add the **sn\_itsm\_aia.office\_365\_group\_member\_approval.required** system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** This property is set to **true** by default.

2.  [Add the **sn\_itsm\_aia.office\_365\_group\_member\_approval.group\_id** system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
3.  Add the sys\_id of the group that you want to use for approvals as the value of the **sn\_itsm\_aia.office\_365\_group\_member\_approval.group\_id** system property.
4.  Add users that you'd like to approve the output for this agentic workflow in the **Office 365 Approval** group.


</td></tr><tr><td>

You don’t want the workflow output of adding or removing users to go through an approval process.

</td><td>

Set the **sn\_itsm\_aia.office\_365\_group\_member\_approval.required** system property to **false**.

</td></tr></tbody>
</table>
**Note:** The Manage Microsoft 365 group members agentic workflow doesn’t have a trigger and is invoked manually.

To modify the Manage Microsoft 365 group members agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Manage Microsoft 365 group members

Autonomously manage adding and removing users in a Microsoft 365 email distribution list.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Manage Microsoft 365 group members**.

## AI agents used in the Manage Microsoft 365 group members agentic workflow

The Microsoft 365 group membership AI agent is used to look up Microsoft 365 groups and add or remove members from the email distribution list.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

## Add or remove group members in a Microsoft 365 group

In the agentic workflow record:

1.  Review the information in the Describe and connect screen and in the Define trigger screen, make the necessary updates, and then select **Save and Continue**.
2.  In the Select display screen:
    1.  Choose where you want the agentic workflow output to be displayed.
    2.  Use the arrow next to it to add roles that can access the agentic workflow.

        **Note:** The itil role is added by default. You can change the role for the agent. If you change the role, you must also change the role in the following three flow and flow action ACLs:

        -   sn\_itsm\_aia.look\_up\_group
        -   sn\_itsm\_aia.look\_up\_user
        -   sn\_itsm\_aia.manage\_office\_365\_group\_member
    3.  Select **Save and test**.

        The agent executes the request for the agentic workflow.


**Example of the Manage Microsoft 365 group members agentic workflow output in the ServiceNow AI Agent Studio**![Microsoft 365 group members agentic workflow output.](../image/now-assist-itsm-aiagents-o365-group-manage.png)

In the AI Agent Studio, the human agent gets notified as soon as one or more users are added or removed so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

