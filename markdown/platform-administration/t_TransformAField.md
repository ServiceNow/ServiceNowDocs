---
title: Transform a field
description: Transform the contents of field using a set of rules and conditions.Creating a transformation record is the first step in transforming a field.Each related transform record performs a specific transformation type such as adding characters to the beginning of the value or replacing one string for another. You may need to create multiple related transform records to generate a preferred output field value.Verify the transform changes the field value as desired before applying them to existing records in the database.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Transforms, Field normalization and transformation, Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Transform a field

Transform the contents of field using a set of rules and conditions.

## Before you begin

Role required: admin or normalizer

## Procedure

1.  Create a transformation record.

2.  Create one or more related transform records.

3.  Test the transform.

4.  Runs data jobs.


## What to do next

If you want to also show what the original \(raw\) input value was prior to transformation, create a raw field to store this value.

## Create a transformation record

Creating a transformation record is the first step in transforming a field.

### Procedure

1.  Activate the Field Normalization plugin.

2.  Navigate to **Field Normalization** &gt; **Configurations** &gt; **Transformations**.

3.  Click **New**.

4.  Create a transformation record.

<table id="table_ppz_nfs_w1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for this transformation record. This value is for reference only and is not used in any processing.

</td></tr><tr><td>

Table

</td><td>

Select the ServiceNow table containing the field being transformed. It is important to understand the table hierarchy when setting up a field transform. For example, if you configure transformation for a field in the Computer \[cmdb\_ci\_computer\] table, that field will be transformed for all workstation machines, Windows servers, Linux servers, and UNIX servers.

</td></tr><tr><td>

Field

</td><td>

Select the field to transform. The list presented contains only those field types \(integer and string\) from the table selected that can be transformed. **Note:** The sys\_user record that initiates the transform process must have its date format set to the default format of "yyyy-MM-dd." Any other date format causes an error during transformation. This problem is only specific to transforming **TO TARGET** fields of type Date/Time. This problem is not an issue if the target field type is of type String or if the field mapping for the date field is changed to the same date format as the transformation process.

</td></tr><tr><td>

Mode

</td><td>

The three available modes are **Off**, **Test**, and **Active**. All transformation records are created in the test mode by default. Do not change the mode until you have thoroughly tested the transformation. When testing is complete, change the mode to **Active**. To disable this transformation, switch the mode to **Off**.

</td></tr><tr><td>

Normalize query

</td><td>

Select this check box to apply the field value transformed by this record to all queries involving this field. Queries issued with the raw \(original\) field value will be edited to use the transformation value.

</td></tr><tr><td>

Raw field

</td><td>

Select the field to use to display the original input \(non-normalized\) values on a form in which a field value has been normalized. For the selection to appear in the drop-down list, add a custom field to the form for the table selected. For instructions on adding a field for raw data, see [Create a raw field](t_CreateARawField.md).

</td></tr></tbody>
</table>5.  Click **Submit**.

    The **Transforms** and **Data Jobs** Related Lists appear on the form.


## Create one or more related transform records

Each related transform record performs a specific transformation type such as adding characters to the beginning of the value or replacing one string for another. You may need to create multiple related transform records to generate a preferred output field value.

### Procedure

1.  In the Transformation record, select the **Transforms** Related List.

2.  Click **New**.

    A selection list of transform types appears, displaying only those transformations appropriate for the field type selected.

    ![Transform types](../image/TransformTypes.png "Transform types")

3.  Select a transform type and provide the appropriate parameters.

4.  Select an **Order** number for this transform.

    **Note:** The conditions for the transforms are executed according to the order numbers assigned.

5.  Select the **Final** check box to stop processing with this transform if the condition evaluates to true.

6.  Select the **Case sensitive** check box to force case sensitivity in the condition statement.

    The following transform example replaces the INC at the beginning of an incident number with the string ENG if the assignment group is ITSM Engineering.

    ![Transformation record](../image/TransformationRecord.png "Transformation record")

7.  Click **Submit**.

    The new Transform appears in the Related List of the Transformation record.

    When the Transform is created, a Transformation application data job is also created. This data job applies this transform to appropriate records in the entire database and should not be run until testing is complete.

8.  Repeat steps 2 through 8 until the output value meets your desired criteria.


## Test a transform

Verify the transform changes the field value as desired before applying them to existing records in the database.

### About this task

**Note:** Users must have the normalization\_tester role to create test records.

New transformation records open in the **Test** mode by default, enabling administrators to test transforms thoroughly before applying them to the existing records in the database. In the test mode, the **Start** controls are not available for the **Transform application** data job. There are two methods, listed below, for testing transforms before committing the transformations to existing data.

### Procedure

-   Manually create or update test records.

    In the test mode, only records that have been created or updated by a user with the normalization\_tester role are transformed. Grant the normalizer and normalization\_tester roles to the same user or grant them to separate users.

-   Use the Test transforms utility to enter a raw value and see the resulting transformed value.

    This feature enables a normalization tester to transform field values on the fly without opening or updating records. This utility tests all the transforms configured for this field.

    1.  Open a Transformation record.

    2.  Click the **Test transforms** Related Link.

        A dialog box appears for testing field values.

    3.  Enter a value to transform in the **Raw data** field.

        ![Raw data field](../image/RawDataField.png)

    4.  Click **OK**.

        The platform transforms the raw value in the **Transformed data** field.

        ![Transformed data field](../image/TransformedDataField.png)

    5.  Enter new raw data to test other transforms.

    6.  Click **Cancel** to end the test.

    7.  When testing is complete, change the **Mode** to **Active** and run the data job.


