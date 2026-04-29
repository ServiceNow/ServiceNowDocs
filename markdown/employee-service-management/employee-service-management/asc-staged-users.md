---
title: Edit staged users for Alumni Center
description: Use Staged Alumni to ensure the import set upload and transform process ran correctly. It also ensures that your uploaded alumni are configured with the correct user ID.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Edit staged users for Alumni Center

Use **Staged Alumni** to ensure the import set upload and transform process ran correctly. It also ensures that your uploaded alumni are configured with the correct user ID.

## Before you begin

Role required: sn\_asc.admin

## Procedure

1.  Navigate to **All** &gt; **Alumni Service Center** &gt; **Administration** &gt; **Staged Alumni**.

2.  Review the list of staged alumni.

3.  Look for and correct duplicate names and duplicate user IDs.

4.  Click the number associated with a user to edit it.

5.  Enter or edit the fields on the form for the user.

<table id="table_phb_1gt_lbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically assigned staging number of the user.

</td></tr><tr><td>

State

</td><td>

The status of the user.-   Approval Needed
-   Approved
-   Alumni Created
-   Duplicate
-   Invalid
-   Denied


</td></tr><tr><td>

Personal email

</td><td>

The personal email of the user. How your company contacts the user.

</td></tr><tr><td>

Internal user

</td><td>

The user record found in the User \[sys\_user\] table for the alumnus.

</td></tr><tr><td>

Internal profile

</td><td>

The HR profile of the user.

</td></tr><tr><td>

Alumni

</td><td>

The name of the user found in the Alumni \[sn\_asc\_user\] table.

</td></tr><tr><td>

First name

</td><td>

First name of the user.

</td></tr><tr><td>

Last name

</td><td>

Last name of the user.

</td></tr><tr><td>

Date format

</td><td>

Date format to override the system date format.

</td></tr><tr><td>

Time zone

</td><td>

The time zone the user resides in.

</td></tr><tr><td>

Proposed user ID

</td><td>

The user ID created after you fill in the fields and click **Generate Proposed User ID**.The user ID creates based on the personal email address provided with a suffix from the properties. For more information on the suffix, see [Properties for Alumni Center](asc-properties.md).

</td></tr></tbody>
</table>6.  Select **Save**.

7.  Select **Generate Proposed User ID**.

8.  Select **Update**.

9.  After making edits, ensure that valid users are in the **Approved** state.

10. Return to the **Staged Alumni** list view.

11. Select **Import** or from the **Staged Alumni** list, select **Import All Approved** at the bottom.

12. Select **Import All**.

    For more information about the default state for staged alumni, see [Properties for Alumni Center](asc-properties.md).

    The Import Approved Staged to Alumni scheduled job runs.


