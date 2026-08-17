---
title: Add key stakeholders to a processing activity
description: Add key stakeholders to a processing activity. Based on their role, users are assigned default processing activity privileges that control whether they can edit a processing activity, view it, or respond to its privacy assessments.
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

Add key stakeholders to a processing activity. Based on their role, users are assigned default processing activity privileges that control whether they can edit a processing activity, view it, or respond to its privacy assessments.

## Before you begin

Role required: sn\_privacy.analyst

## About this task

A processing activity can have multiple key stakeholders. By default, the entity owner is one of the key stakeholders.

You can add key stakeholders only when the processing activity is either in the **Discover** or **Review** states.

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the List icon \[Omitted image "ListsIcon.jpg"\] Alt text:.

3.  In the **Lists** tab, select **Processing activities** &gt; **All processing activities**.

4.  Open the processing activity to which you want to add key stakeholders.

5.  In the Key stakeholders related list, select **Add**.

    1.  Select the users to add.

    2.  Select **Add**.

    **Note:** If a user's role changes, a privacy analyst must manually update the user's processing activity privilege.

6.  Modify the processing activity privilege of a key stakeholder.

    If a user's role changes, a privacy analyst must manually update the user's processing activity privilege.

    1.  From the Key stakeholders related list of the processing activity, open the stakeholder record you want to modify.

    2.  In the **Responsibility** field, enter the responsibilities for the stakeholder.

    3.  In the **Processing activity privileges** field, set the stakeholder processing activity privilege.

        The available options are:

        -   Respond to privacy assessments - Default privilege for stakeholders with the sn\_privacy.assessment\_responder or sn\_privacy.business\_user role.
        -   Edit processing activity and respond to privacy assessments - Stakeholders must have the sn\_privacy-business\_role to be assigned this privilege by a privacy analyst or manager.
        -   No privilege to respond to assessments - Default privilege for stakeholders with no privacy roles.
        **Note:**

        If you select an option that requires a role the stakeholder doesn't have, the application displays a validation message. Contact your system administrator to grant the necessary role, and then set the privilege again.

    4.  Select **Save**.


## Result

Selected stakeholders receive an email notification confirming they have been added as key stakeholders.

## What to do next

After the key stakeholders are defined, assign the processing activity to stakeholders with edit access. They can then review and update the related lists. See [Enable key stakeholders to update processing activities directly](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/assign-pa-to-keystakeholders.md).

Send privacy assessments to the stakeholders with the sn\_privacy.assessment\_responder or sn\_privacy.business\_user role who were added. See [Send a privacy assessment from a processing activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/send-privacy-asmt-from-pa.md).

**Parent Topic:**[Using Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/using-privacy-mgmt.md)

