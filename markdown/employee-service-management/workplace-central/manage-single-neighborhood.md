---
title: Manage a single neighborhood
description: Edit the details of a neighborhood like the spaces, workplace profiles, space assignment tasks, and user assignment rules.
locale: en-US
release: australia
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage neighborhoods using Space Planning, Working with Space Planning, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Manage a single neighborhood

Edit the details of a neighborhood like the spaces, workplace profiles, space assignment tasks, and user assignment rules.

## Before you begin

Role required: sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Central**.

2.  Select the **Space Planning** module.

    The floor plan tab opens by default.

3.  Select the **Neighborhoods** tab.

    The list of neighborhoods opens with details like their name, active status, and restricted status.

4.  Select the neighborhood that you want to edit.

    The neighborhood opens with the Overview tab. The overview displays KPIs for the neighborhood like the total capacity, assigned users, assigned spaces, and assignment ratio.

5.  Edit the details of the neighborhood like the name, active status, restricted status, or short description.

6.  Manage the neighborhood based on your requirement.

<table id="choicetable_d2c_yt5_g3c"><thead><tr><th align="left" id="d156685e109">

Action

</th><th align="left" id="d156685e112">

Steps

</th></tr></thead><tbody><tr><td id="d156685e118">

**Add a space**

</td><td>

1.  Select the **Spaces** tab.
2.  On the Spaces list, select **New**.
3.  On the Create New Space form, in the **Space** field, select the space that you want to add to the neighborhood.
4.  Select **Save**.
 **Important:** If you have Workplace Space Management installed, the Create New Space form contains fields from the `Space` form. For more information about the Space form, see [Add a space using Workplace Space Management](../../workplace-space-management/task/add-a-space.md).

</td></tr><tr><td id="d156685e173">

**Remove a space**

</td><td>

1.  Select the **Spaces** tab.
2.  On the Spaces list, select the spaces that you want to remove, then select **Delete**.
3.  On the confirmation pop-up, select **Delete all**.


</td></tr><tr><td id="d156685e203">

**Export space details**

</td><td>

1.  Select the **Spaces** tab.
2.  On the Spaces list, select the spaces that you want to export.

If you don't select any spaces, the system exports the details of all the spaces in your instance.

3.  Select **Export**.
4.  On the **Export** pop-up, select a **File Type** based on your preference.
    -   Excel
    -   CSV
    -   JSON
    -   PDF
5.  Select the Delivery Type based on your preference.
    -   Download: Downloads the file to your local system.
    -   Email: Sends the file as an attachment to the specified email address.

If you select email, you must enter the email address of the recipient.

6.  Select **Export**.


</td></tr><tr><td id="d156685e275">

**Assign a workplace profile**

</td><td>

1.  Select the **Workplace Profile Location Assignments** tab.
2.  On the Workplace Profile Location Assignments list, select **New**.
3.  On the form, fill in the fields.

For a description of the field values, see [Workplace Profile Location Assignment form](../../workplace-service-delivery/reference/wsd-location-assignment-form.md).

</td></tr><tr><td id="d156685e312">

**Remove a workplace profile**

</td><td>

1.  Select the **Workplace Profile Location Assignments** tab.
2.  On the Workplace Profile Location Assignments list, select the profiles that you want to remove, then select **Delete**.
3.  On the confirmation pop-up, select **Delete all**.


</td></tr><tr><td id="d156685e342">

**Create a space assignment task**

</td><td>

1.  Select the **Space Assignment Tasks** tab.
2.  On the Space Assignment Tasks list, select **New**.
3.  On the Workplace Task form, fill in the fields.

For a description of the field values, see [Workplace Task form - Space Assignment task](../reference/workplace-task-space-assignment.md).

4.  Select **Save**.
 **Note:** Assigning spaces based on the task can take several minutes.

</td></tr><tr><td id="d156685e390">

**Create a user assignment rule**

</td><td>

1.  Select the **User assignment rules** tab.
2.  On the User assignment rules list, select **New**.
3.  On the **Neighborhood User Assignment Rule** form, fill in the fields.

For a description of the field values, see [Neighborhood User Assignment Rule form](../reference/user-assignment-rule-form.md).

4.  Select **Save**.
5.  After the rule is created, select **Execute user assignments** on the neighborhood page.
 After executing the user assignments, the `Assign Users to Neighborhood` scheduled job assigns workplace profiles to the neighborhood.

</td></tr></tbody>
</table>
**Parent Topic:**[Manage neighborhoods using Space Planning](manage-neighborhoods-central.md)

