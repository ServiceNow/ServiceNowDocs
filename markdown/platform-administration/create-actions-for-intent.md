---
title: Create and associate actions for intent
description: Create and map actions to an intent for executing appropriate actions once the intent match happens.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 1
breadcrumb: [Configure email agentic workflows, Use agentic workflows in emails, Now Assist in Notifications, Configure core features, Administer]
---

# Create and associate actions for intent

Create and map actions to an intent for executing appropriate actions once the intent match happens.

## Before you begin

Role required: sn\_notif\_agents.notification\_ai\_admin

## About this task

Subflows must be created to invoke subflows to associate an action to the intent. For more information, see [Create a subflow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-subflow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Email Intents**.

2.  From the table, select the intent.

3.  From Notification Intent Actions, select **New** to add actions to the intent.

4.  Enter the **Name**.

5.  Select the **Type** based on the criteria defined for the intent.

<table id="choicetable_ovz_ssv_3hc"><thead><tr><th align="left" id="d309664e112">

Type

</th><th align="left" id="d309664e115">

Action

</th></tr></thead><tbody><tr><td id="d309664e121">

**Subflow Invocation**

</td><td>

Select the **Subflow** tab and select the subflow that must be triggered when the intent is matched. To create subflows see, [Create a subflow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-subflow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

</td></tr><tr><td id="d309664e136">

**Reply Email**

</td><td>

**Note:** **Reply Email** type will not work if the target record is not attached to the email.

 1.  Select the **Reply Email** tab
2.  Enter the **Email Content Guidelines** and **Recipients**.
3.  Enter the **Recipients** if it's a new recipient aside from the original recipient
4.  Select **Email Delivery Mode**, select **Auto** to send the email to the user, select **Draft** to draft a reply.

**Note:** If the **Assigned to** field in target record is not populated then the user won't be able to review the draft or draft a reply.

5.  In **Search profile**, select or add a profile that can be used for generating a reply for the email when the intent is matched.


</td></tr></tbody>
</table>6.  Enter the **Order** number for processing once the intent is identified, the system retrieves the associated actions according to the sequence specified in the action record.

7.  Select **Stop processing** check box to stop processing after a certain action.

8.  Select **Default** check box if there are no matching intents for the email.

    **Note:** For such cases, a Default Intent Action \(also referred to as a no intent action\) is executed. This ensures that every email gets a response, whether it's a generic mail or sending a standard confirmation or an acknowledgment.

9.  In the **Action Execution Criteria** tab, specify the conditions needed to execute the action.

10. Select **Submit**.


**Parent Topic:**[Configure email agentic workflows in Notifications](../reference/configuring-agentic-workflows-in-notifications.md)

