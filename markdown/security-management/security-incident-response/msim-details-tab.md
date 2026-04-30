---
title: Update Major Security Incident details
description: View and update specific details related to the major security incident such as Incident Record Details, Active Team participants, and the corresponding activity log.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Update Major Security Incident details

View and update specific details related to the major security incident such as Incident Record Details, Active Team participants, and the corresponding activity log.

All the related details of the major security incident are displayed with various Form sections on the **Details** tab of the workspace. Displays the details such as Incident Record Details, Active Team participants, and the corresponding activity log. You can also view the linked SIR incidents, Vulnerability Group record details, and an ability to broadcast an activity posting to all the linked incident records.

Primarily the Details tab contains:

1.  Major Security Incident Form fields and incident-related UI sections.
2.  Activity stream

The following table provides the details of the major security incident form fields:

<table id="table_hgw_4gb_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Incident**

</td></tr><tr><td>

Number

</td><td>

Major security incident record number.

</td></tr><tr><td>

Primary state

</td><td>

The primary state of the major security incident record.

</td></tr><tr><td>

Detection Date

</td><td>

The date when the major security incident was first created or proposed.Whenever you modify the Detection date on the Details tab, the date and time of the MSI is automatically calculated, refreshed, and displayed on the **Time** &gt; **Time since the incident started** section on the **Overview** section of the workspace.

</td></tr><tr><td>

Title

</td><td>

Title of the Major security incident.

</td></tr><tr><td>

Code name

</td><td>

Code name for the major security incident. For example, Blue Tiger.

</td></tr><tr><td>

Next update on

</td><td>

The date and time of the next update for resolving the major security incident. For example, 5:00 pm EST on March 25, 2024.

</td></tr><tr><td>

Category

</td><td>

Category of the major security incident.

</td></tr><tr><td>

Sub category

</td><td>

Subcategory type of the major security incident.

</td></tr><tr><td>

Estimated resolution date

</td><td>

The estimated date by when the incident is expected to be resolved. The default value is 7 days from the time of the major security incident creation.

</td></tr><tr><td>

Priority

</td><td>

Priority of the major security incident.

</td></tr><tr><td>

Alert sensor

</td><td>

Alert sensor of the major security incident. For example, User Reported Phishing.

</td></tr><tr><td>

Source

</td><td>

Source of the major security incident.

</td></tr><tr><td colspan="2">

**Active Team**

</td></tr><tr><td>

Incident Manager

</td><td>

Name of the incident manager.

</td></tr><tr><td>

Assignment Groups

</td><td>

Indicates the different response teams and team members from each team who are actively working on the major security incident.

</td></tr><tr><td colspan="2">

**Candidate**

</td></tr><tr><td>

MSI candidate state

</td><td>

Indicates the major security incident candidate state such as proposed or promoted. If the incident is promoted, then the state is displayed as Accepted.

</td></tr><tr><td>

Promoted by

</td><td>

User who had promoted the major security incident.

</td></tr><tr><td>

Promoted

</td><td>

Date when the major security incident was promoted.

</td></tr><tr><td>

Justification

</td><td>

Justification of the major security incident. The justification should include the MSI number and the code name.

</td></tr><tr><td>

Potential impact

</td><td>

The potential impact and severity of the major security incident. The Potential impact should include the MSI number and the code name.

</td></tr><tr><td colspan="2">

**Restriction**

</td></tr><tr><td>

Enforce restriction

</td><td>

Select this option to enforce restrictions on certain major security incident restrictions. You can enforce restrictions to limit the view or modify access only to certain users or groups. For more information, see [Restrict access to certain major security incidents](../task/restrict-access-major-security-incidents.md).

</td></tr><tr><td>

Allowed members

</td><td>

List of users who can access the major security incident.

</td></tr><tr><td>

Allowed groups

</td><td>

List of groups who can access the major security incident.

</td></tr><tr><td colspan="2">

**Other actions**

</td></tr><tr><td>

Attachment

</td><td>

Any attachments related to the major security incident.Select **Select** option to add attachments to the incident.

</td></tr><tr><td>

Conference Call

</td><td>

Use conference calls with the third-party service providers as a communication channel to meet with the stakeholders to resolve the major security incidents. For more information, see [Major Security Incident Management Conference Call Integration](integrate-msim-conference-calls.md)

</td></tr></tbody>
</table>**Activity**:

Use the Activity section to add your work notes and comments, and post your activity privately and also add additional comments as required using the Compose section. Save the activity after you post your work notes and comments to view the added activity or work notes in the Activity section.

**Note:** Select the **Show more** details link to view the details of a specific security incident record, which are associated with that major security incident.

Set your preferences to view the related activities such as:

1.  **Filters**: Select the **Filter sets** icon to set filters.

    Set filters to view the activity conversations such as activities added on the work notes, email, Timeline, and any additional comments.

2.  **Flagged**: Select the **Flagged** icon to flag the activities.

    Flag any important activity conversations for you to keep them handy.


-   **[Restrict access to certain major security incidents](../task/restrict-access-major-security-incidents.md)**  
Manage who can view or modify major security incidents that contain sensitive information. You can enforce major security incident restrictions to determine who has access to view or modify certain major security incident records and related lists and limit the read or write access only to certain users or groups.

**Parent Topic:**[Using Major Security Incident Management](../../security-incident-response/concept/major-security-incident-setup.md)

**Related topics**  


[Propose, promote, and link incident records](../../security-incident-response/concept/promoting-sir-to-msim.md)

[Using MSI List view in the MSIM workspace](../../security-incident-response/task/list-view-in-msim.md)

[View Major Security Incident impact metrics](viewing-trend-charts-and-progress-of-msi.md)

[View Major Security Incident trend charts](viewing-msi-impact-metrics.md)

[Link additional records to Major Security Incident](../task/linking-additional-records-to-major-security-incidents.md)

[Unlink records from Major Security Incident](../task/unlinking-msi-records.md)

[Manage tasks in a Major Security Incident](tasks-tab.md)

[Track collaboration activity via MSIM workspace](collab-tab.md#)

[Create and distribute MSIM Status Reports](../task/creating-and-distributing-major-security-incident-status-reports.md)

