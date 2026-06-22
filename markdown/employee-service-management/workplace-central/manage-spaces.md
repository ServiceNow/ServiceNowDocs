---
title: Manage spaces using Space Planning
description: As a space planner, manage the spaces, their assignments, and their allocations using the Space Planning module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-central/manage-spaces.html
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Space Planning, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Manage spaces using Space Planning

As a space planner, manage the spaces, their assignments, and their allocations using the Space Planning module.

## Before you begin

Role required: sn\_wsd\_core.workplace\_manager or sn\_wsd\_spcmgmt.space\_planner

**Note:** The sn\_wsd\_core.scenario\_reader role has access to view the spaces, their details, and allocations.

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

2.  On the side navigation, select the **Space Planning** module.

    The Space Planning workspace opens with the **Floor plan** tab selected by default.

3.  Select the **Spaces** tab.

    The list of spaces opens with details like their name, location, and allocation.

4.  Manage the spaces based on your requirement.

<table id="choicetable_d2c_yt5_g3c"><thead><tr><th align="left" id="d155561e101">

Action

</th><th align="left" id="d155561e104">

Steps

</th></tr></thead><tbody><tr><td id="d155561e110">

**Create a space**

</td><td>

1.  On the Spaces list, select **New**.
2.  On the Create New Space form, fill in the fields based on your requirement.
3.  Select **Save**.
 **Important:** If you have Workplace Space Management installed, the Create New Space form contains fields from the `Space` form. For more information about the Space form, see [Add a space using Workplace Space Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-space-management/add-a-space.md).

</td></tr><tr><td id="d155561e156">

**Edit spaces**

</td><td>

1.  On the Spaces list, select the spaces that you want to edit.
2.  Select **Edit**.
3.  Edit the details based on your requirement.

**Important:** The value that you enter in any field is applied to all the selected spaces. For example, if you select **Is reservable**, all the spaces made reservable.

4.  Select **Update**.


</td></tr><tr><td id="d155561e194">

**Edit space allocations**

</td><td>

1.  On the Spaces list, select the spaces that you want to edit.
2.  Select **Edit allocation**.

The Edit space allocation pop-up opens with the `Allocation` tab selected by default.

3.  From the Allocation type list, select a value based on your requirement.

Allocation type is displayed only if you have the Workplace Space Management.

4.  Select the neighborhood that you want to assign the spaces to.

If you have Workplace Space Management, you can select the Cost Center, Department, or Workplace Entity based on the Allocation type value.

5.  Select either of the following options based on your requirement:
    -   **Remove existing and replace**: Replaces the existing allocations with the new allocation.
    -   **Add to existing**: Retains the existing allocations and adds the new allocation.
6.  Select **Apply**.


</td></tr><tr><td id="d155561e258">

**Remove space allocations**

</td><td>

1.  On the Spaces list, select the spaces that you want to edit.
2.  Select the context menu next to **Edit allocation**, then select **Remove allocation**.
3.  Select the Allocation type that you want to remove.

Allocation types are available only if you have the Workplace Space Management.

4.  Review the current allocation details, then select **Save**.


</td></tr><tr><td id="d155561e297">

**Export space details**

</td><td>

1.  On the Spaces list, select the spaces that you want to export.

If you don't select any spaces, the system exports the details of all the spaces in your instance.

2.  Select **Export**.
3.  On the **Export** pop-up, select a **File Type** based on your preference.
    -   Excel
    -   CSV
    -   JSON
    -   PDF
4.  Select the Delivery Type based on your preference.
    -   Download: Downloads the file to your local system.
    -   Email: Sends the file as an attachment to the specified email address.

If you select email, you must enter the email address of the recipient.

5.  Select **Export**.


</td></tr></tbody>
</table>
**Parent Topic:**[Working with Space Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/working-with-space-planning.md)

