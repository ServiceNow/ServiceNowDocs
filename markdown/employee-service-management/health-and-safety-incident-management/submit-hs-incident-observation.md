---
title: Submit a safety incident as an employee
description: Submit a safety incident through the Employee Center to report it to the safety department for an investigation.
locale: en-US
release: xanadu
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Submit safety incidents and observations, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Submit a safety incident as an employee

Submit a safety incident through the Employee Center to report it to the safety department for an investigation.

## Before you begin

Role required: sn\_ohs\_im.requestor

## About this task

If there's an emergency, you can use the Health and Safety contacts knowledge article to access the emergency contact list. This knowledge article includes the local health and safety team contact numbers, emergency response numbers, or any other contacts that employees can use if there’s a health and safety incident or emergency.

To open the emergency contacts knowledge article from the Employee Center, navigate to **Health and Safety** &gt; **Policy and procedures** &gt; **Health and Safety contacts**.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  In the Employee Center, select the **Health and Safety** menu and then select **Health and Safety Incidents**.

    -   Select **Report Health and Safety Incident - Basic** to report an incident with basic information.
    -   Select **Report Health and Safety Incident - Advanced** to report an incident that includes its detailed information such as injured people, injury details, hazards, and assets involved in the incident.
3.  On the form, fill in the fields.

    **Note:** The **Contractor** option appears only when the Health and Safety Contractor Management \(sn\_hs\_crm\) application is installed on your instance. For more information, see [Additional features in Health and Safety](install-hs-incident-mgmt.md#table_ix1_bff_gxb). The field only lists users who have the \[snc\_external\] role assigned to them and have their Health and Safety profile created. For more information, see [Assign Health and Safety profile to a user](assign-hs-profile-user.md).

4.  If you have selected the **Report Health and Safety Incident - Advanced** form, use the **Describe the event** section to add more details about the incident.

<table id="table_bjs_5xp_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Is there an injured person?

</td><td>

Option to indicate if there's an injured person resulting from the incident.The **Injured people** section appears when **Yes** is selected in this field.

</td></tr><tr><td>

Injured people

</td><td>

Name and injury details of the person injured during the incident.1.  Select **Select injured people**.
2.  In the **Add injured person** section, add the person who got injured and the type of the injury.
3.  In the **Add injured body parts** section, add injury details for each body part injured during the incident.

Select a body part in the visual injury picker, then select **Severity** and **Affected body part**, and add **Description** about the injury.

4.  Select **Save**.
If there are more than one affected persons in this incident, add each.

</td></tr><tr><td>

Other people involved

</td><td>

People who are directly or indirectly connected to the incident, such as an injured person, collaborators, witnesses, and other relevant individuals. These individuals can be from within or outside your organization.If there are other people involved in the incident, add their names. Select **Add people involved** to add them. For more information, see [People Involved form](../reference/hs-people-involved-form.md).

If the incident involves more than one person, add each.

</td></tr><tr><td>

Select hazards

</td><td>

If there's a hazard identified during this incident, add it using the **Select hazards** button. Select all the hazards identified for this incident.

If there are other hazards that are identified and not available in the **Select hazards** window, enter them manually in the **Other hazards** field.

</td></tr><tr><td>

Add Assets

</td><td>

If an asset was involved in this incident, add it using the **Select assets** button. Add all the assets that are involved in this incident.

**Note:** The assets field appears only when Expanded Model and Asset Classes \[sn\_ent\] application is installed.

For more information, see [Additional features in Health and Safety](install-hs-incident-mgmt.md#table_ix1_bff_gxb)

</td></tr></tbody>
</table>5.  If necessary, attach an image about the incident using the add attachments icon \(![Add attachment icon.](../image/icon-add-attachment.png)\).

6.  Select **Submit**.

7.  To track the status and updates to your safety incident, navigate to the **My Requests** list and open the record.


## Result

-   The safety incident is submitted in the New state and is available in the **My Requests** list in the Employee Center.

-   The affected employee receives a pre-configured email notification about the incident submission.

## What to do next

As a safety manager or agent, if the incident isn’t assigned to you, you can assign it to yourself and start working on it. You can also assign it to another safety agent. For more information, see [Assign a safety incident or observation](assign-hs-incident-observation.md).

**Parent Topic:**[Submitting safety incidents and observations](../concept/submitting-safety-incidents-obvs.md)

