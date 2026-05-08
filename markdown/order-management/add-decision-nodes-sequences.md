---
title: Add decision nodes to a sequence
description: Activate the next stage in the playbook based on the outcome of the previous stage by adding decision nodes while creating or updating a sequence.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create sequences, Customer Engagement Sequences, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Add decision nodes to a sequence

Activate the next stage in the playbook based on the outcome of the previous stage by adding decision nodes while creating or updating a sequence.

## Before you begin

**Note:** Decision-based stages and the demo data are available only starting with Playbook version 28.3 on the Zurich release. The sample Lead nurturing tele-sales sequence available with the demo data shows how to configure a decision-based, telesales sequence with the schedule call activity.

Delegated developer roles must be assigned to designated users. For more information, see [Grant delegated developer permissions for managing sequences](grant-delegated-developer-permissions.md).

Role required: sn\_crm\_sequence.admin, sn\_crm\_sequence.writer

**Note:** If you're using Customer Engagement Sequences 1.0.0, you need the playbook.admin or pd\_author role to create sequences.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Sequences** &gt; **All Sequences**.

4.  Select a sequence that you're creating or updating.

5.  In the sequence diagram, hover over the object that you want to insert a decision activity next to, and select the ![](../../../reuse/icons/product-icons/circle-plus-fill-24.svg) icon to add an activity.

6.  Select the Add a decision icon ![](../image/diamond-icon.png).

    A decision is added with two branches and the Decision properties side panel opens for configuration.

7.  Under the Details tab, enable the **Start with delay** option to add delay between the two call attempts.

    For example, if you want the agent accessing the workflow to wait two days before calling the prospective lead or customer again, you would set Duration type to **Explicit duration** and set **Days** to `2`.

    For more information, see Start with delay input properties.

8.  Under the Branches tab, expand New branch and enter a unique name for the branch in the **Branch label** field.

9.  Select **Add Condition**.

    For example, to execute the branch when the outcome of the previous call attempt was unsuccessful, you would set the condition **\[Schedule call &gt; Output &gt; State\]****\[is\]****\[Cancelled\]**.

    For more information, see Decision activities.

10. Select **Save and close**.


## What to do next

Add a stage for the new branch you created earlier, and repeat the steps to add more activities as needed. For more information, see Add and configure a stage in a playbook.

**Parent Topic:**[Create a customer engagement sequence](create-customer-engagement-sequence.md)

**Related topics**  


[bundle-crworkflow.create-decision-stage]

