---
title: Configure a program service
description: Add a program service for use within the programs associated with the Healthcare and Life Sciences Service Management applications.Create a specification characteristic so that you can define the program service offering in Healthcare and Life Sciences programs.Create a relationship between a program service and programs to make the service available within the program.Publish a program service for use within the Healthcare and Life Sciences Service Management applications.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring programs and program services for Healthcare and Life Sciences workflows, Configuring Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure a program service

Add a program service for use within the programs associated with the Healthcare and Life Sciences Service Management applications.

## Before you begin

Role required: sn.hcls\_manager or admin

## About this task

By default, the application provides a few sample program services for the Healthcare and Life Sciences workflows that you can as a reference when creating a program service.

## Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Program service**.

2.  In the Program services list, click **New**.

3.  On the form, fill in the fields.

<table id="table_scn_ppw_brb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identifier for the program service. This field is automatically set to an auto-generated number.

</td></tr><tr><td>

Name

</td><td>

Name to identify the program service.

</td></tr><tr><td>

Active

</td><td>

Option to enable the program service for use.

</td></tr><tr><td>

State

</td><td>

State of the program service. This field is automatically set to the **Draft** state.

</td></tr><tr><td>

Start Date

</td><td>

Date when the program service is scheduled to start.

</td></tr><tr><td>

End Date

</td><td>

Date when the program service is scheduled to end.

**Note:** The end date of the program service must be later than the start date.

</td></tr><tr><td>

Description

</td><td>

Summary of the program service.

</td></tr></tbody>
</table>    **Note:** Either enter the date in the `yyyy-mm-dd` format, such as `2021-12-31`, or click the select date icon corresponding to the date type. For example, provide the end date of the program service by either entering the date in the **End Date** field or clicking the select date icon \(![Select date icon.](../image/select-date-icon.png)\) and selecting the date.

4.  Click **Submit**.

5.  [Configure a specification characteristic for the program service](hcls-create-program-service.md#).

6.  [Associate the program service with a program](hcls-create-program-service.md#).

7.  [Publish the program service](hcls-create-program-service.md#).


**Parent Topic:**[Configuring programs and program services for Healthcare and Life Sciences workflows](../concept/hcls-program-setup.md)

## Configure a specification characteristic for a program service

Create a specification characteristic so that you can define the program service offering in Healthcare and Life Sciences programs.

### Before you begin

Role required: sn.hcls\_manager or admin

### Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Program service**.

2.  In the Program services list, click the link to a program service from the **Number** column.

3.  In the Specification Characteristics related list, click **New**.

4.  In the **Characteristic** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select a characteristic from the **Name** column of the Characteristics list.

    By default, the application provides the **Benefit Investigation** characteristic for use a reference when creating a characteristic. To create a new characteristic, click **New** in the Characteristics list and fill in the characteristic details.

5.  In the **Characteristic Option** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select a characteristic option from the **Option** column of the Characteristic Options list.

    To create a new characteristic option, click **New** in the Characteristic Options list and fill in the characteristic option details.

6.  Select the **Mandatory** check box to make the specification characteristic as a requirement for completing the program service.

7.  Click **Submit**.

    **Note:** You can ignore the Activities section, which is not used.


## Associate a program service with a program

Create a relationship between a program service and programs to make the service available within the program.

### Before you begin

[Configure a program](hcls-create-program.md#).

Role required: sn.hcls\_manager or admin

### About this task

You can also associate a program service with a program by using the Program module. For more information, see [Associate a program with a program service](hcls-create-program.md#).

### Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Program service**.

2.  In the Program services list, click the link to a program service from the **Number** column.

3.  In the Program relationships related list, click **New**.

4.  In the **Program** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select the program from the **Name** column of the Specifications list.

5.  In the **Program service** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select a program service from the **Name** column of the Specifications list.

6.  In the **Relationship Type** field, select **Offers**.

7.  Select the **Active** check box for activating the relationship.

8.  Click **Submit**.


## Publish a program service

Publish a program service for use within the Healthcare and Life Sciences Service Management applications.

### Before you begin

Role required: sn.hcls\_manager or admin

### Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Program service**.

2.  In the Program services list, click the link to the program service from the **Number** column.

3.  On the Program service form, click **Publish** to make the program service available for use within Healthcare and Life Sciences Service Management applications.


