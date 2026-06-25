---
title: Add key stakeholders to a processing activity
description: Add key stakeholders to a processing activity and set their privilege to control whether they can view it, respond to its privacy assessments, or edit it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/add-stakeholders-to-a-pa.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Add key stakeholders to a processing activity

Add key stakeholders to a processing activity and set their privilege to control whether they can view it, respond to its privacy assessments, or edit it.

## Before you begin

Role required: sn\_privacy.analyst

## About this task

A processing activity can have multiple key stakeholders. While you can add or delete as many key stakeholders as you want, by default, the entity owner is one of the key stakeholders. You can add any user as a key stakeholder, including users without privacy roles. Based on their role, they are assigned default processing activity privileges that control whether they can edit a processing activity, view it, or respond to its privacy assessments.

You can add key stakeholders only when the processing activity is either in the **Discover** or **Review** states.

## Procedure

1.  Navigate to **All** &gt; **Privacy Management** &gt; **Privacy Workspace** &gt; **Processing activities** &gt; **All processing activities**.

2.  Open the processing activity to which you want to add key stakeholders.

3.  Navigate to the Key stakeholders related list, and select **Add**.

    1.  Select the stakeholders to add.

    2.  Select **Add**.

        Selected stakeholders are added to the Key stakeholders related list of the processing activity. Based on their role, each stakeholder receives a processing activity privilege.

    **Note:** If a user's role changes, a privacy analyst must manually update the user's processing activity privilege.

4.  Modify the processing activity privilege of a key stakeholder.

    1.  From the Key stakeholders related list of the processing activity, open the stakeholder record you want to modify.

    2.  In the **Responsibility** field, enter the responsibilities for the stakeholder.

    3.  In the **Processing activity privileges** field, select one of the following options.

<table id="table_l3x_4m3_ljc"><thead><tr><th>

Privilege

</th><th>

Result

</th></tr></thead><tbody><tr><td>

**Respond to privacy assessments**

</td><td>

Default privilege for stakeholders with the sn\_privacy.assessment\_responder or sn\_privacy.business\_user role.

</td></tr><tr><td>

**Edit processing activity and respond to privacy assessments**

</td><td>

Privilege set manually by a privacy analyst or privacy manager. The stakeholder must have the sn\_privacy.business\_user role to be assigned this privilege.

</td></tr><tr><td>

**No privilege to respond to assessments**

</td><td>

Default privilege for stakeholders with no privacy roles.**Note:** To modify this privilege, the user must first be granted the sn\_privacy.business\_user role. Then, a privacy analyst must manually update their privilege to **Respond to privacy assessments** or **Edit processing activity and respond to privacy assessments**.

</td></tr></tbody>
</table>        If you select an option that requires a role the stakeholder doesn't have, the application displays a validation message. Contact your system administrator to grant the necessary role, and then set the privilege again.

    4.  Select **Save**.


## Result

Selected stakeholders receive an email notification confirming they have been added as key stakeholders.

## What to do next

After the key stakeholders are defined, assign the processing activity to stakeholders with edit access. They can then review and update the related lists, as required. See [Assign a processing activity to a key stakeholder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/assign-pa-to-keystakeholders.md).

Send privacy assessments to the added stakeholders. See [Send a privacy assessment from a processing activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/send-privacy-asmt-from-pa.md).

**Note:** Only users with sn\_privacy.assessment\_responder or sn\_privacy.business\_user role can be sent privacy assessments.

**Parent Topic:**[Using Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/using-privacy-mgmt.md)

**Related topics**  


[Access a processing activity from the Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/request-edit-access-pa.md)

