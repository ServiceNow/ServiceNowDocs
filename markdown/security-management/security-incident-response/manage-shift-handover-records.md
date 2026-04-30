---
title: Manage Shift Handover records
description: Use the Shift Handover records list view to create, edit, copy, or delete Shift Handover records. Each Shift Handover record is associated with a Shift Handover Report Template.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [List view in SIR Workspace, Explore, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Manage Shift Handover records

Use the Shift Handover records list view to create, edit, copy, or delete Shift Handover records. Each Shift Handover record is associated with a Shift Handover Report Template.

## Before you begin

Role required:

-   sn\_escm\_sh.shift\_analyst: Minimum requirement to access the Shift Handover records.
-   sn\_escm\_sh.shift\_owner: Create, edit, and delete handover log records in the user groups the Shift Owner is part of. This role inherits the sn\_escm\_sh.shift\_analyst role.
-   sn\_escm\_sh.shift\_analyst: View all the Shift Handover log records but can contribute only to In-progress Shift Handover records assigned to the Shift Analyst's group.
-   sn\_si.analyst - Inherits the sn\_escm\_sh.shift\_analyst role.
-   sn\_si.admin - Inherits the sn\_escm\_sh.shift\_admin role.
-   sn\_escm\_sh.shift\_admin - Inherits the sn\_escm\_sh.shift\_owner role

**Important:** To learn how to configure the Shift Handover Template as an Admin, see [Configure Shift Handover Templates](../task/configure-shift-handover-templates.md).

## About this task

The Shift Owner and the respective team or user group create the Shift Handover log records. The Shift Owner has to choose the Shift Handover template and user group that will work on the Shift Handover report. After the Shift Handover report is complete, it will be shared with the next active Shift Owner and team.

Shift Handover template key points:

-   If some other analyst from the active shift team has already updated the report before you, and if changes are being processed, then you might see an error message that there are pending content updates. You must wait 30 seconds and then select **Change to "Review" state** again. You can see the consolidated report on the right-pane get updated with other analysts' updated content.
-   If the Shift owner has modified the content in a section in the Review state, then the same content gets reflected for the Analyst when the record moves back to the In-progress state.
-   The Shift owner must be mindful while editing the content in the Review state, and performing actions like merging two lines, merging two sections, removing a section, as this will affect the Shift Handover report of the other analysts.
-   After publishing the Shift Handover report, the Shift owner can modify the content, but they can’t change the record state.
-   When someone is modifying the content and during that time, if the record state gets changed from In-progress to Review, then the unsaved content changes get discarded.
-   Shift admin will have write access to all shift handover log records irrespective of user groups.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select the Security Incident List ![list icon](../image/listview-icon.png) icon.

3.  On the **Lists** tab, select **Shift Handover Records**.

4.  Select **All Records** to view the list of all the Shift Handover records.

5.  Select **Assigned to Team** to view the list of Shift Handover records that are assigned to all the teams/user groups that the analysts belong to.

6.  To create a new Shift Handover record, select **New**.

7.  On the form, fill the fields.

<table id="table_ahr_y2c_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number that is automatically generated for a Shift Handover record.

</td></tr><tr><td>

Template

</td><td>

The Shift Handover Template to use. For example, Sample Shift Template.

</td></tr><tr><td>

Description

</td><td>

Description for the Shift Handover record.

</td></tr><tr><td>

User group

</td><td>

The user group/team for the Shift Handover record to be assigned to. For example, Team Development Code Reviewers.

</td></tr><tr><td>

State

</td><td>

The current state of the Shift Handover record. By default, the initial state is Draft**Note:** The State can't be changed during the creation of a record.

</td></tr><tr><td>

Shift Name

</td><td>

The shift name containing the shift start and shift end details. For example, US Day Shift.

</td></tr></tbody>
</table>8.  Select **Create**.

    A new Shift Handover record is created based on the template that you selected and added to the list view.

9.  Open the new Shift Handover record to update the status and details of the security incidents on the Shift Handover report.

    By default, the Shift Handover record is in the **Draft** state.

    **Note:** Only the Shift Owner can modify the content.

    ![Edit Shift Handover report content](../image/shift-handover-list.png "Shift Handover report content")

10. In the Draft shift report editor, use the Shift Handover report template sections to update the details of the security incidents and users.

    You can format your report with all the options in the editor, like fonts, colors, bullets, links, and attachments.

    **Note:** The Shift Owner and Shift Analyst can both modify the content.

    1.  After making the required changes to the Shift Handover report, select **Save**.

    2.  Select **Change to "In-progress" state** action to move the Shift Handover record to In-progress state.

        ![Shift Handover in-progress state](../image/shift-handover-report-progress.png "Shift Handover in-progress")

11. In the My shift handover notes editor, update the required details for all the sections like security incident and user details.

    **Note:** The Shift Owner and Shift Analyst can both modify the content.

    1.  To mention a particular record in the editor, use **/** and choose **Select a record**, and then select a record from the list of tables that pops-up.

        For example, if you select **Security Incidents** record, then a list of security incident appear. Select a security incident \(**SIR0010025**\) from the list and update the required Shift Handover details. You can also mention the fields associated with the security incident like short description, watch list by using **/** after the security incident number.

        ![Shift Handover notes](../image/shift-handover-sample.png "Shift Handover Notes")

    2.  To mention a particular user in the editor, use **/** and choose **Select a user**, and then select a user from the list that pops-up.

    3.  To mention the count of records in the editor, use **/** and choose **Mention count**, and then select the record from the list that pops-up.

    4.  You can format your report with all the options in the editor, like fonts, colors, bullets, links, and attachments.

    5.  After making the required changes to the Shift Handover notes, select **Save**.

    6.  Select **Change to "Review" state** action to move the Shift Handover record to Review state.

        **Note:** If some other analyst from the active shift team has already updated the report before you, and if changes are being processed, then you might see an error message. You must wait a few seconds and then select **Change to "Review" state** again.

        ![Shift Handover Review state](../image/shift-handover-report-review.png "Shift Handover Review")

12. In the Consolidated shift report, review the Shift Handover report and make the required changes.

    **Note:** Only the Shift Owner can modify the content.

    1.  After making the required changes to the Shift Handover notes, select **Save**.

    2.  If the Shift Handover report requires more updates from the Analysts, you can select **Change to "In progress" state**.

    3.  Select **Publish** action to publish the Shift Handover report.

        ![Publish the Shift Handover report](../image/shift-handover-report-publish.png "Shift Handover Publish")

13. Select **Save** to save the Shift Handover report.

    After you save, you can see a preview of the Shift Handover report with your latest updates on the Preview pane.

    **Note:** Though you can preview the updates you made on the Shift Handover report immediately, the other analysts might take a few seconds to see the changes.

14. As a Shift Owner, you can also perform the following actions on the Shift Handover list view.

    1.  To edit an existing Shift Handover record, select the record and select the **Edit** action.

        You can modify only the Start time, End time, Description, and Region.

    2.  To create a copy of a Shift Handover record, select the record and select **Create copy** action.

    3.  To delete an existing Shift Handover record, select the record and select the **Delete** action.


**Parent Topic:**[List view in SIR Workspace](setting-up-list-view-in-analyst-workspace.md)

**Related topics**  


[Personalize a list](personalize-a-list.md)

[Apply quick filters on Security Incidents and Response Tasks lists](use-quick-filters-for-security-incidents.md)

[Assign Security Incidents](assign-security-incident.md)

[Close multiple security incidents](../task/close-multiple-incidents-sir.md)

[Assign Response Tasks](../task/assign_response_tasks.md)

[Report Phish Email](../task/report-phish-email.md)

[Working with quick filters](configure-quick-filters.md)

[Export Security Incidents or Response Tasks](export-security-incidents-or-response-tasks.md)

