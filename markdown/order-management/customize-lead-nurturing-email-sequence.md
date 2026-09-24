---
title: Customize the Lead nurturing email sequence
description: Adapt the Lead nurturing email sequence available with the Customer Engagement Sequences app to match your organization's email and call outreach cadence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/customize-lead-nurturing-email-sequence.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Customer Engagement Sequences, Sales automation apps, Use, Sales Customer Relationship Management]
---

# Customize the Lead nurturing email sequence

Adapt the Lead nurturing email sequence available with the Customer Engagement Sequences app to match your organization's email and call outreach cadence.

## Before you begin

The User Mailbox Integration plugin \(com.glide.email.user\_mailbox.integration\) must be active on your instance so the sequence can detect email replies.

You should be familiar with using Workflow Studio and Playbook Experience.

Role required: sn\_crm\_sequence.admin, sn\_crm\_sequence.writer

## About this task

The Lead nurturing email sequence runs against the Lead \[sn\_lead\_mgmt\_core\_lead\] table when a lead is created with an email address, and assigns the resulting sequence task to the lead's owner.

The following table lists the stages included in the Lead nurturing email sequence.

|Stage|Description|
|-----|-----------|
|Setup|Prepares the sequence context for the lead.|
|Email Attempt 1|Sends an initial outreach email, then waits for a reply before moving to the next stage.|
|Email Attempt 2|Sends a follow-up email if the lead didn't reply to the first attempt, then waits for a reply.|
|Call Attempt 1|Creates a call task for an outbound call if the lead hasn't replied to either email, then waits for the call to be resolved.|
|Call Attempt 2|Creates a call task for a second outbound call if the first call attempt wasn't resolved, then waits for resolution.|
|Tear Down|Closes the sequence run. If the lead replied to an email or a call was resolved, the sequence marks the lead as contacted. If none of the outreach attempts were resolved, the sequence adds an outcome update to the sequence task's work notes.|

**Note:** Do not remove the Setup or Tear Down stages, or change the Start Sequence or End Sequence activities in those stages.

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to **Sequences** &gt; **All Sequences**.

4.  Duplicate the Lead nurturing email sequence.

    1.  Select the **Lead nurturing email sequence** record.

    2.  Select **Open steps**.

        You're redirected to Workflow Studio, where the sequence diagram opens for editing.

    3.  Create a copy of the sample sequence by selecting **Duplicate** from the More actions menu \[Omitted image "ellipsis-horizontal-outline-24.svg"\] Alt text:.

    4.  On the Duplicate playbook, enter a name for your sequence in the **Playbook name** field.

    5.  Select **Duplicate**.

        The duplicated sequence diagram opens for editing and it's in the Inactive state.

5.  Configure the sequence.

    At this stage, you can add, modify, or remove stages, decision nodes, and activities. For more information, see [Create a customer engagement sequence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/create-customer-engagement-sequence.md).

6.  Customize the email activity.

    1.  In the Email Attempt 1 or Email Attempt 2 stage, select the email activity such as **Send Email Attempt 1** to open the activity properties.

    2.  On the activity properties panel, select the **Automation** tab.

    3.  Modify the subject and the body text of the email.

        \[Omitted image "email-sequence.png"\] Alt text: Automation tab on the Email activity properties for the Lead nurturing email sequence in Workflow Studio.

    4.  Select **Save and close**.

7.  Customize the wait time between the email and call attempts to change how long the sequence waits before moving to the next attempt.

    By default, there's a gap of two days between the email and call attempts.

    1.  In the Email Attempt or Call Attempt stages, select the wait activity that follows an email or call attempt to open the activity properties.

    2.  Select **Show additional options** to view all available configuration options.

    3.  Navigate to **Details** &gt; **Schedule** &gt; **Start with delay**.

    4.  Set the number of days the sequence should wait between the current and the next attempt in the **Wait for** field.

    5.  Select **Save and close**.

8.  Customize what gets updated in the Lead record's Work Notes when the sequence ends.

    1.  In the Update the Notes on Lead as unresolved stage, select the **Update notes on lead as unresolved** activity.

    2.  Navigate to the **Inputs** section on the **Automation** tab.

    3.  Change the text under the **Fields** field to match your business requirements.

        \[Omitted image "email-sequence-work-notes.png"\] Alt text: Work notes that gets added on the Lead record when the sequence exits.

9.  Verify the sequence by selecting **Test**.

10. Publish the sequence by selecting **Activate**.


## Result

Your customized version of the Lead nurturing email sequence runs automatically against leads that meet your trigger conditions.

**Parent Topic:**[Using Customer Engagement Sequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-customer-engagement-sequences.md)

**Related topics**  


[Define trigger conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/define-trigger-conditions.md)

[Add decision nodes to a sequence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/add-decision-nodes-sequences.md)

[View sequence tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/view-sequence-tasks.md)

