---
title: Configure a program
description: Add a program for use within the Healthcare and Life Sciences Service Management applications.Create a specification characteristic so that you can define the program offering in Healthcare and Life Sciences workflows.Create a relationship between a program and program services to make the program service available within the program.Publish a program for use within the Healthcare and Life Sciences Service Management applications.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure programs and program services, Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure a program

Add a program for use within the Healthcare and Life Sciences Service Management applications.

## Before you begin

Role required: sn.hcls\_manager or admin

To associate an eligibility criteria checklist with the program, create a checklist. For more information, see [Create a checklist](https://www.servicenow.com/docs/access?context=t_CreateAChecklist&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

**Note:** By default, the application provides a few checklist templates that you can use as a reference when creating a checklist for a Healthcare and Life Sciences program.

## About this task

By default, the application provides a few sample programs for the Healthcare and Life Sciences workflows that you can as a reference when creating a program.

## Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Program**.

2.  In the Programs list, click **New**.

3.  In the **Name** field, enter a name to identify the program.

4.  In the **Eligibility criteria** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select a checklist from the **Name** column of the Checklist Templates list.

5.  Select the **Active** check box to enable the program for use.

6.  Provide the start date by either entering the date in the **Start Date** field in the `yyyy-mm-dd` format, such as `2021-12-31`, or clicking the select date icon \(![Select date icon.](../image/select-date-icon.png)\) and selecting the date.

7.  Provide the end date by either entering the date in the **End Date** field in the `yyyy-mm-dd` format, such as `2021-12-31`, or clicking the select date icon \(![Select date icon.](../image/select-date-icon.png)\) and selecting the date.

    **Note:** The end date of the program must be later than the start date.

8.  Associate medication products with the program.

    1.  Click the unlock medication product icon \(![Unlock medication product icon.](../image/lock.png)\) next to the **Medication product** field.

    2.  Click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) for the **Medication product** field.

    3.  In the Medication product models list, click the link to the medication product.

    4.  To add multiple medication products, repeat steps 8.b through 8.c.

    **Note:** When you add a medication product for a program, you must also configure the dosage specifications for the medication product. For more information, see [Configure dosage specifications for a medication product](../concept/hcls-config-dosage-spec.md).

9.  In the **Description** field, enter a summary of the program.

10. Click **Submit**.

11. [Configure a specification characteristic for the program](hcls-create-program.md#).

12. [Associate the program with a program service](hcls-create-program.md#).

13. [Publish the program](hcls-create-program.md#).


**Parent Topic:**[Configure programs and program services for Healthcare and Life Sciences workflows](../concept/hcls-program-setup.md)

## Configure a specification characteristic for a program

Create a specification characteristic so that you can define the program offering in Healthcare and Life Sciences workflows.

### Before you begin

Role required: sn.hcls\_manager or admin

### Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Program**.

2.  In the Programs list, click the link to a program from the **Number** column.

3.  In the Specification Characteristics related list, click **New**.

4.  In the **Characteristic** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select a characteristic from the **Name** column of the Characteristics list.

    By default, the application provides the **Benefit Investigation** characteristic for use a reference when creating a characteristic. To create a new characteristic, click **New** in the Characteristics list and fill in the characteristic details.

5.  In the **Characteristic Option** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select a characteristic option from the **Option** column of the Characteristic Options list.

    To create a new characteristic option, click **New** in the Characteristic Options list and fill in the characteristic option details.

6.  Select the **Mandatory** check box to make the specification characteristic as a requirement for completing the program.

7.  Click **Submit**.

    **Note:** You can ignore the Activities section, which is not used.


## Associate a program with a program service

Create a relationship between a program and program services to make the program service available within the program.

### Before you begin

[Configure a program service](hcls-create-program-service.md#).

Role required: sn.hcls\_manager or admin

### About this task

You can also associate a program with a program service by using the Program service module. For more information, see [Associate a program service with a program](hcls-create-program-service.md#).

### Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Program**.

2.  In the Programs list, click the link to a program from the **Number** column.

3.  In the Program relationships related list, click **New**.

4.  In the **Program** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select the program from the **Name** column of the Specifications list.

5.  In the **Program service** field, click the lookup icon ![Lookup using list icon.](../image/lookup-using-list.png) and select a program service from the **Name** column of the Specifications list.

6.  In the **Relationship Type** field, select **Offers**.

7.  Select the **Active** check box for activating the relationship.

8.  Click **Submit**.


## Publish a program

Publish a program for use within the Healthcare and Life Sciences Service Management applications.

### Before you begin

Role required: sn.hcls\_manager or admin

### Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Program**.

2.  In the Programs list, click the link to the program from the **Number** column.

3.  On the Program form, click **Publish** to make the program available for use within Healthcare and Life Sciences Service Management applications.


