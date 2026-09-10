---
title: On-call bulk roster template Excel file
description: The roster template workbook contains one sheet per mapped group, prefilled with shift template details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/oc-bulk-schedule-roster-template.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-08-21"
reading_time_minutes: 5
keywords: [oncall\_roster\_template.xlsx, on-call roster template, bulk create schedules]
breadcrumb: [Create on-call schedules for multiple groups, Configuring On-Call Scheduling in Service Operations Workspace, On-Call Scheduling in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# On-call bulk roster template Excel file

The roster template workbook contains one sheet per mapped group, prefilled with shift template details.

When you select **Download template** on the roster upload step of the On-call Onboarding wizard, the wizard generates the `roster_template.xlsx` workbook. The wizard prefills each sheet with the shift template details for the group that you mapped in the wizard.

For more information, see [Create on-call schedules for multiple groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/oc-create-bulk-schedule-onboarding.md).

\[Omitted image "oc-roster-template-sheet.png"\] Alt text: Screenshot showing the roster template workbook with group sheets, group members list, and roster details including rotation interval and member assignment fields.

<table id="table_tz3_vjp_jkc"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group sheet

</td><td>

One sheet per group that you mapped in the wizard, named for that group. The group sheet is prefilled with details about the shift, roster, rotation, and frequency from the on-call template mapped to that group. If the shift template includes multiple regions, separate blocks appear for each region, such as APAC and EMEA.

 Sheet names cannot exceed 31 characters. If a group name is longer, the wizard shortens it and adds a number to keep duplicate names unique. The sheet name might not exactly match the group name.

</td></tr><tr><td>

Group Members

</td><td>

List of active group members.

</td></tr><tr><td>

Roster details

</td><td>

Update the roster and rotation details as needed. -   **Roster Name**: Primary or Secondary. These are the only supported roster names.
-   **Rotation Interval**: The rotation interval of the shift: Daily, Weekly, or Monthly.
-   **Rotation Every**: Positive whole number that sets the rotation frequency of the shift.
-   **Day of Week**: The day when the shift rotates. Applies to Weekly rotation.
-   **Monthly Rotation Type**: When the monthly shift rotation happens: Specific Day or Last day of the month. Applies to Monthly rotation.
-   **Start rotation on**: When monthly rotation type is specific day, which day of the month the rotation happens.
-   **Members**: Group members assigned to the roster.

Copy one member name per row from the **Group Members** list.


</td></tr><tr><td>

— DO NOT DELETE — end of roster

</td><td>

Structural boundary row that marks the end of each roster's member list. The upload parser uses this row to determine where the member list ends. **Important:** Don't delete, modify, or type in this row. Deleting or altering this row breaks parsing for all roster data below it on that sheet.

</td></tr></tbody>
</table>## File requirements

The workbook must be an `.xlsx` or `.xls` file. The file cannot exceed the attachment limit set by the **com.glide.attachment.max\_size** system property. If the file exceeds this limit, the wizard displays an error and blocks the upload.

## Upload validation

When you upload the completed workbook, the wizard validates it and reports issues at two severity levels. After the upload passes validation, the wizard displays a per-group preview of the resulting on-call configuration.

If validation flags an issue, refer to the following tables for the cause and resolution.

|Message|Cause|Fix|
|-------|-----|---|
|No groups detected|The workbook has no recognizable group sheets.|Re-download the template instead of removing all the sheets.|
|Group name is missing|The **Group** cell is empty.|Don't clear the pre-filled group name.|
|Duplicate group|Two sheets list the same group name.|Verify that each sheet's **Group** cell matches only its own group.|
|Unknown group|The group named in the **Group** cell wasn't selected in Team selection step of the wizard.|Go back to the wizard and add the group.|
|No shifts on a sheet|Every shift block was removed from a group's sheet.|Keep at least one shift block, even if its rosters are empty.|
|Shift name is missing|The **Shift** cell is empty.|Don't clear the pre-filled shift name.|
|Duplicate shift|The same shift name appears twice on one sheet.|Each shift should appear only once per group.|
|Shift name doesn't match the template|The **Shift** cell was edited to a name that isn't on the group's shift template.|Use the exact shift name the wizard pre-filled. The error message lists the shift names it expects.|
|No rosters on a shift|Both the Primary and Secondary roster blocks were removed.|Keep at least one roster block per shift.|
|Roster name is missing|The **Roster Name** cell is empty.|Don't clear the pre-filled **Primary** or **Secondary** label.|
|Duplicate roster|Two rosters under the same shift are both named Primary, or both Secondary.|Keep one of each.|
|Member row contains placeholder text|A label such as Members or Roster Name was left in a member row.|Replace it with a person's name, or leave the row empty.|
|Member not found|The name doesn't match any active user.|Check the spelling, or copy the exact name from the Group Members list.|
|Member name matches more than one user|Two or more active users share that display name.|Use the person's username instead.|

|Message|Cause|Fix|
|-------|-----|---|
|Rotation interval is missing|The wizard doesn't apply a default for this field.|Fill in Daily, Weekly, or Monthly.|
|Day of week is missing|Weekly rotation selected but Day of Week left empty.|The wizard defaults it to Monday.|
|Monthly rotation type is missing|Monthly rotation selected but Monthly Rotation Type left empty.|The wizard defaults it to Specific Day.|
|Start day of the month is missing|Specific Day selected but no start day provided.|The wizard defaults it to day 1.|
|Roster has no members|A roster \(Primary or Secondary\) has no member names under it.|That roster is created with nobody scheduled on it.|
|Duplicate member|The same name appears twice under one roster.|Remove the duplicate if it wasn't intentional.|
|Member not in the group|The person is added to the roster but isn't currently an active member of the group.|The person is still scheduled, but this usually signals a mismatch worth double-checking.|

**Parent Topic:**[Create on-call schedules for multiple groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/oc-create-bulk-schedule-onboarding.md)

