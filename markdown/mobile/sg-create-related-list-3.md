---
title: Update your record screen to display a related list
description: Update your record screen to display a list of related records.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure a related list screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Update your record screen to display a related list

Update your record screen to display a list of related records.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder appears in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  From the menu on the left side, select **Screens** to display the data items for the scope.

4.  Open the screen record where you want to display your embedded list.

5.  In the control panel, find the **Record screen segments** list and click **New**.![Related list segment on a record screen](../image/record-screen-seg-section.png)

6.  Select **Record screen section** in the **Create a record screen segment** window.

7.  In the record screen segment, use the **Order** field to choose where to display embedded list on your record screen.

    Segments display using the value in the **Order** field from lowest to highest.

8.  In the **Embedded screen** section, click **New**.

9.  Select **Related Lists** in the **Create a screen** window.

10. In the **New related lists screen**, fill in the following fields.

<table id="table_np4_54l_5wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the related list

</td></tr><tr><td>

Description

</td><td>

Description of the related list.

</td></tr><tr><td>

Show count

</td><td>

Whether the screen displays a count of records in the list

</td></tr><tr><td>

Hide screen name

</td><td>

Whether to display the screen name for the related list

</td></tr><tr><td>

Available offline

</td><td>

Whether the list is accessible in offline mode.

</td></tr><tr><td>

Table

</td><td>

Select the table to use.**Important:** Select the table used in the record screen, not the table for the records within the list. For example, if you're creating a list to display incidents related to a problem, select the Problem table.

</td></tr><tr><td>

Icon

</td><td>

Choose an icon for the related list.

</td></tr></tbody>
</table>11. In the **Related list mapping** section, click **New**.

    In the next steps, you map a connection between this related list and the list screen that you created in the steps under [Create a list screen to use as a related list](sg-create-related-list-2.md).

12. In the **Related list map** panel, select a relationship in the **Relationship** field.

    This field creates the relationship between the table used in the record screen, and the table used for the records within the related list. For example, for a list of incidents related to a problem, you choose **Incident-&gt;Problem**.

13. In the **Destination screen** section, click the **Choose** button and select the list screen you created in the previous steps.


## Result

Your screen displays a tab for your related list. Users tap this tab to see records on that list.

**Note:** If you selected **Show count** in the related list screen field section, the screen displays a counter number in the related lists. This number relates to the number of records based on your selections in the **Related list maps** section.

The number of related records shown in a selected destination screen can be less or equal to the counter number displayed in the related list. The lower number of records is due to additional conditions applied to the list.

![Related list segment on a record screen](../image/form-related-list-segment.png)

## Example

Continuing the preceding example, the problem record screen must have a related list. In the **Related list maps** section, you select the **Incident-&gt;Problem** relationship. Under **Destination Screen**, you select the related incident list created in the previous steps. After logging out and back in again, you have a related list on your problem record screen, which displays a list of incidents related to that problem.

![Related list pop-up showing relationship options](../image/create-related-list.png)

