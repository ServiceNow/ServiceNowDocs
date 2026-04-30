---
title: Submit an acknowledgement request using the Compliance Workspace
description: After you have created an acknowledgement campaign using the Compliance Workspace, you can submit the acknowledgement request to the defined audience.
locale: en-US
release: zurich
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Acknowledge policy, Manage control objectives and policies, Use, GRC Compliance Workspace, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Submit an acknowledgement request using the Compliance Workspace

After you have created an acknowledgement campaign using the Compliance Workspace, you can submit the acknowledgement request to the defined audience.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, click the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Policy acknowledgements** &gt; **All campaigns**.

4.  Open the Policy Acknowledgement Campaign \(PAC\) record you want to submit to the defined audience.

5.  Scroll down and click the **Acknowledgement Setup** related list.

6.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Audience

</td><td>

Select the employees who are responsible for acknowledging the policy. You define the audience using the [Audience module](create-audience-ws.md).

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

Select if you want to members of the audience to be able to [request a policy exception](request-policy-exception-ws.md).

</td></tr></tbody>
</table>7.  Save the record.

8.  Scroll down and click the **Acknowledgement Campaigns** related list.

9.  Click **New**.

    **Note:** The majority of the fields are pre-filled with data from the policy record.

10. On the form, fill in the fields.

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

 

</td></tr><tr><td>

Valid from/to

</td><td>

Select the period of time the acknowledgement is valid. The acknowledgement is valid from the beginning of the **Valid from** date until the end of the **Valid to** date.**Note:** The **Valid to** date cannot be beyond the **Valid to** date defined in the policy.

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
</table>11. Click **Submit**.

12. Click **Request Acknowledgement**.

    Notice that the following changes occur.

    -   The state of the acknowledgement campaign changes to **Pending Acknowledgement**.
    -   Acknowledgement \(ACK\) records for each member of the audience appear at the bottom of the screen.
    -   The **Acknowledgement Results** tab shows the progress of the acknowledgement process. That is, it reports the total number of acknowledgements sent, and keeps a running tally of the number and types of responses received \(for example, number of accepted, declined, exempted, and so forth\).
    **Note:** The **Activity** tab shows acknowledgement activities as they happen. The compliance user can click the Work notes check box and post work notes to track changes. The Additional comments box can be used to communicate with the audience.

    Also, each member of the audience receives an email notification similar to the following example.

13. As the acknowledgement period elapses, you can monitor the progress of the responses by navigating to **Policy and Compliance** &gt; **Policy Acknowledgement** &gt; **Pending Acknowledgements**.

14. You can also identify any audience members who have exceeded the acknowledgement time line by navigating to **Policy and Compliance** &gt; **Policy Acknowledgement** &gt; **Overdue Acknowledgements**.


