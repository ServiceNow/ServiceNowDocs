---
title: View choice list definitions
description: The Choice Set \[sys\_choice\_set\] table contains a record for every field that uses a choice list.You can personalize the options that are available in a choice list.After defining a set of choice list values, you can reuse the values for another field in a different table.You can remove the None option from a choice list if it is not necessary.You can change the default display label of the None option for a choice field.You can delete all choices for a choice field from the Choice Set record.You can create a choice list for a field with another type, such as an integer, string, or reference field.By default, inactive or invalid choice list values appear in blue text instead of black. You can disable the color indicator for invalid choices.Add a search field to choice fields that have a long list of options.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Choice list field type, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# View choice list definitions

The Choice Set \[sys\_choice\_set\] table contains a record for every field that uses a choice list.

## Before you begin

Role required: personalize\_choices

**Note:** The personalize\_choices role must be explicitly granted to the user; it cannot be an ACL.

## About this task

The choice set record is associated with an application file, which allows update sets and team development to track and transfer all choices for a field in a single update record.

Choice list values allow a maximum length of 40 characters. The range of allowable numerical values is \[-999, 999\].

## Procedure

1.  Right-click the choice list field label and select **Show Choice List**.

    To view other choice list values, modify the filter at the top of the list.

    **Note:** When you use an ACL to grant personalize\_choices on a particular field, **Show Choice List** is not available. It is only available if you explicitly grant the role to the user. **Configure Choices** continues to appear regardless of whether it is an ACL or an explicitly granted user role.

2.  Review the items in the list.

    **Warning:** Do not add new choices to the list. To add new choices to a choice list field, use the **Configure Choices** option.


**Parent Topic:**[Choice list field type](../concept/c_ChoiceLists.md)

## Define an option for a choice list

You can personalize the options that are available in a choice list.

### Before you begin

Role required: personalize\_choices

### Procedure

1.  Navigate to a form where the field appears.

2.  If the choice list is dependent on another field, enter the choice value that the options depend on.

    For example, on the incident table, the **Subcategory** is dependent on the **Category**. To customize which subcategory choices are available for the hardware category, select **Hardware** in the **Category** field.

3.  Right-click the field label and select **Configure Choices**.

4.  Use the slushbucket to rearrange the order, add, or remove items or to create new items.

5.  Click **Save**.

    To dynamically add items to a choice list, use the `addOption` GlideForm method .

    **Note:** Some business rules may be affected by changes to choice list options \(for example, default Incident states\).


## Reuse a choice list

After defining a set of choice list values, you can reuse the values for another field in a different table.

### Before you begin

Role required: personalize\_choices

### Procedure

1.  Right-click an existing choice field \(Field A\) and select **Configure Choices**.

2.  Add the desired choice list values in the **Choices** related list.

3.  To reuse the choice list values for another field \(Field B\) in a different table, right-click the label for Field B and select **Configure Dictionary**.

4.  In the **Choice table** field, select the table where Field A resides.

5.  In the **Choice field** field, select Field A.

    ![Choice list sharing](../image/ChoiceListSharing.png)

6.  Click **Update**.

    The choice list values defined on Field A are displayed on Field B. When you add or remove choice list values on Field A, those changes are also reflected on Field B. After you specify a choice table and a choice field, the field no longer uses the defined choice list.


## Remove the None option from a choice list

You can remove the **None** option from a choice list if it is not necessary.

### Before you begin

Role required: personalize\_dictionary

### Procedure

1.  Navigate to a form where the field appears.

2.  Right-click the field label and select **Configure Dictionary**.

3.  Change the **Choice** field value to **Dropdown without -- None -- \(must specify a default value\)**.

    ![Choice without none](../image/ChoiceWithoutNone.png)

4.  Ensure that the **Default** field is populated to determine which choice is displayed by default.

    **Note:** If the field is dependent on another field, the **-- None --** option remains available.


## Change the None display value for a choice list

You can change the default display label of the **None** option for a choice field.

### Before you begin

Role required: personalize\_choices

**Note:** The personalize\_choices role must be explicitly granted to the user; it cannot be an ACL.

### Procedure

1.  Navigate to a form on which the field appears.

2.  Right-click the field label and select **Show Choice List**.

3.  Click **New**.

4.  Complete the form.

<table id="table_otd_hzt_cq"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select the table.

</td></tr><tr><td>

Element

</td><td>

Leave the name of the field that is automatically populated.

</td></tr><tr><td>

Language

</td><td>

Enter ISO language code for the label.

</td></tr><tr><td>

Sequence

</td><td>

Leave empty. This field determines the order.

</td></tr><tr><td>

Inactive

</td><td>

Leave cleared.

</td></tr><tr><td>

Label

</td><td>

Enter the label to appear in the choice list.

 You can use JavaScript, including calls to script includes, to define the label. For example, the JavaScript label in the following example changes the **-- None --** value of the **Time zone** choice list in a user record to use the time zone value of the instance.

 ![New record creation](../image/DefNullLabelChoice.png)

</td></tr><tr><td>

Value

</td><td>

Enter `NULL_OVERRIDE`.**Note:** You must enter `NULL_OVERRIDE` as the value, or the new label appears in addition to the **-- None --** option.

</td></tr><tr><td>

Dependent value

</td><td>

Leave blank.

</td></tr><tr><td>

Hint

</td><td>

Leave blank.**Note:** When field type is set to **List \(Glide List\)** the hint won't display.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Delete all choice list options

You can delete all choices for a choice field from the Choice Set record.

### Before you begin

Role required: personalize

### About this task

You may want to use this method when you are developing a new application and the business requirements change. If you are updating a choice list that is already in use, consider deactivating the options you no longer use to avoid conflicts with existing data or scripts that may rely on the previous options.

### Procedure

1.  In the navigation filter, enter `sys_choice_set.list` and press Enter.

2.  Open the choice set record for the field.

    For example, to locate the choice set for the incident subcategory, filter by **\[Table\] \[is\] \[incident\] AND \[Element\] \[is\] \[subcategory\]**.

3.  Check the box beside the choice set record to delete and select **Delete** from the Actions choice list below the list.

4.  Click **Delete** in the confirmation window.

    All choices for the field are deleted.


## Create a choice list for another field type

You can create a choice list for a field with another type, such as an integer, string, or reference field.

### Before you begin

Role required: personalize\_dictionary

### About this task

You can use this configuration to standardize data entry and limit available options for a field while still maintaining the original field type.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Open the dictionary entry for the field.

    **Note:** Reference fields with a large number of records in the reference table cannot be converted to look like choice fields. A reference field with too many records reverts to looking like a reference field.

3.  Change the **Choice** value to **Dropdown with --- None ---** or **Dropdown without --- None --- \(must specify a default value\)**.

4.  Right-click the form header and select **Save**.

5.  Click **Create Choice List**.

    -   The **Choices** related list appears on the dictionary entry form.
    -   If records on the table contains data for the field, a choice list value for each unique field value is created. For example, if three records exist on the table and each record has a unique value in the field, then three choices are created.
    -   If no data exists in the field, a choice list value of **-- New choice --** is created.

## Display invalid choice list values

By default, inactive or invalid choice list values appear in blue text instead of black. You can disable the color indicator for invalid choices.

### Before you begin

Role required: admin

### About this task

In the following example, the **Network** category has been deactivated, so it appears in blue for records that still contain the inactive value.

![Choice list invalid](../image/ChoiceListInvalid2.png)

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Clear the check box for the **Display missing choice list entries** property.


## Add search option to a choice field

Add a search field to choice fields that have a long list of options.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to a form that contains choice fields.

    For example, incident.

2.  From a choice field on the form, for example State, right-click the field and select **Configure Dictionary**.

3.  Switch to the advanced view for the dictionary entry form using the context menu by navigating to **View** &gt; **Advanced**.

4.  In the Attributes field, type `is_searchable_choice=true`.

    If there are other entries in the attributes field, use a comma to separate the entries.

5.  Update the Dictionary Entry form and reload the page containing the choice list.


### Result

The choice list contains a search field that users can use to filter the list of choices.

![State field with the list open and a search field at the top of the list](../image/ChoiceFieldSearch.png "Choice field search")

