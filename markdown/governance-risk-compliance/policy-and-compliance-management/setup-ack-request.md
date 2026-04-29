---
title: Set up a policy acknowledgement campaign
description: A policy campaign is the record used to prepare for a policy acknowledgement request. It defines the audience who must provide an acknowledgement that a particular policy is in compliance. A policy campaign is requested only if the compliance user decides it is needed.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Acknowledge policy, Manage, Classic UI, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Set up a policy acknowledgement campaign

A policy campaign is the record used to prepare for a policy acknowledgement request. It defines the audience who must provide an acknowledgement that a particular policy is in compliance. A policy campaign is requested only if the compliance user decides it is needed.

## Before you begin

Role required: Compliance User

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Policies**.

2.  Open the Policy record in the **Published** state you want to acknowledge.

    ![Published policy](../image/policy-published.png)

3.  Scroll down and click the **Acknowledgement Setup** related list.

    ![Acknowledgement Setup related list](../image/acknowledgement_setup.png)

4.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Audience

</td><td>

Select the employees who are responsible for acknowledging the policy. You define the audience using the [Audience module](create-audience.md).

</td></tr><tr><td>

Reference Material URL

</td><td>

Click the lock icon and add a URL to reference materials for the policy that the audience can review. When you have completed your entry, click the lock icon again.

</td></tr><tr><td>

Allow users to decline policy

</td><td>

Select if you want members of the audience to be able to decline the policy.

</td></tr><tr><td>

Allow users to request exception

</td><td>

Select if you want to members of the audience to be able to [request a policy exception](request-policy-exception.md).

</td></tr></tbody>
</table>5.  Save the record.

6.  Scroll down and click the **Acknowledgement Campaigns** related list.

    ![Acknowledgement Campaigns tab](../image/ack-campaigns.png)

7.  Click **New**.

    ![New campaign](../image/new-campaign.png)

    **Note:** Notice that the majority of the fields are pre-filled with data from the policy record.

8.  On the form, fill in the fields.

    **Note:** Only field description that were not previously described are provided here.

<table id="table_nrx_lv2_mjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

An auto-generated record number for the acknowledgement.

</td></tr><tr><td>

State

</td><td>

The current state of the acknowledgement campaign. The default state is New.

</td></tr><tr><td>

Valid from/to

</td><td>

Select the period of time the acknowledgement is valid. The acknowledgement is valid from the beginning of the **Valid from** date until the end of the **Valid to** date.**Note:** The **Valid from** date cannot be prior to the current date. The **Valid to** date cannot be beyond the **Valid to** date defined in the policy.

</td></tr><tr><td>

Number of days to respond

</td><td>

The number of days by which members of the audience have to respond.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the policy.

</td></tr><tr><td>

**Acknowledgement Details** tab

</td><td>

This tab shows details and requirements from the policy, as well as the **Reference Material URL** defined during acknowledgement setup.

</td></tr></tbody>
</table>9.  Click **Submit**.

    The acknowledgement request is now ready for you to send to the defined audience.


-   **[Create an audience](create-audience.md)**  
When you set up a policy acknowledgement request, you must identify an audience responsible for providing the acknowledgement.

**Parent Topic:**[Acknowledge a policy](../concept/ack-policy.md)

