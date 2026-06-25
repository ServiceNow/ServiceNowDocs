---
title: Add a schedule call activity to a telesales workflow sequence
description: Add a schedule call activity in your sequences to support telesales workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/add-schedule-call-activity.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create sequences, Customer Engagement Sequences, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Add a schedule call activity to a telesales workflow sequence

Add a schedule call activity in your sequences to support telesales workflows.

## Before you begin

Review feature support information in [Compatibility information for Customer Engagement Sequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/compatibility-matrix-upgrade-info.md).

To support the ability for your agents to initiate outbound calls from the sequence task, your instance must be integrated with platforms such as Amazon Connect. The Omnichannel Callback application \(sn\_omni\_callback\) must also be installed. For more information, see [Install Omnichannel Callback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/install-omnichannel-callback.md).

Delegated developer roles must be assigned to designated users. For more information, see [Grant delegated developer permissions for managing sequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/grant-delegated-developer-permissions.md).

Role required: sn\_crm\_sequence.admin, sn\_crm\_sequence.writer

## About this task

You can add the Schedule call activity with other activities in a stage or in its own stage.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to **Sequences** &gt; **All Sequences**.

4.  Select a sequence that you're creating or updating.

5.  In the sequence diagram, create a stage to add the activity.

    For more information, see [Add and configure a stage in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/add-configure-stage.md).

6.  Within a stage, select the Add icon \[Omitted image "circle-plus-fill-24.svg"\] Alt text:.

7.  Open the activity picker by selecting the Add an activity icon \[Omitted image "square-outline-24.svg"\] Alt text:.

8.  On the Add activity screen, search for and select **Customer Engagement Sequences** &gt; **Schedule call**.

    **Note:** The options available in the activity picker vary by release. For compatibility information, see [Compatibility information for Customer Engagement Sequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/compatibility-matrix-upgrade-info.md).

9.  On the Details tab of the Schedule call properties pane, enter a name to appear on the Sequence Steps tab during runtime in the **Label** field.

    For example, you might enter `Call attempt 1`.

10. On the Automation tab, fill in the fields.

    For a description of the field values, see [Automation form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sequences-automation-form-fields.md).

11. Select **Save and close**.


**Parent Topic:**[Create a customer engagement sequence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-customer-engagement-sequence.md)

**Related topics**  


[Start with delay input properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/start-with-delay-properties.md)

[Add decision nodes to a sequence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-decision-nodes-sequences.md)

[Omnichannel Callback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/omnichannel-callback.md)

