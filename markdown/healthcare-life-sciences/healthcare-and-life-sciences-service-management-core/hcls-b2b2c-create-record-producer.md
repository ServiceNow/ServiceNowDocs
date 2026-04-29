---
title: Create a record producer for B2B2C in Healthcare and Life Sciences Service Management Core
description: Create a record producer for use with B2B2C.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up B2B2C, Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Create a record producer for B2B2C in Healthcare and Life Sciences Service Management Core

Create a record producer for use with B2B2C.

## Before you begin

Create a table for use with B2B2C. For more information, see [Create a table for B2B2C in Healthcare and Life Sciences Service Management Core](hcls-b2b2c-create-hcls-case-table.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Record Producers**.

2.  Click **New**.

3.  On the form, fill in the fields.

    **Note:** For details on the fields, refer to [Create a record producer](https://www.servicenow.com/docs/access?context=t_DefRecProdInSCat&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

4.  Click **Save**, then re-open the record.

5.  In the related links, do the following:

    1.  Navigate to **Variables** and click **New**.

        **Note:** For details on variables, refer to [Variables to collect data for record producer fields](https://www.servicenow.com/docs/access?context=r_CreatingVariablesForFieldTypes&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    2.  Add the following variables in **Type Specifications**:

<table id="table_oqn_zyw_qwb"><thead><tr><th>

Variable

</th><th>

Type

</th><th>

Reference

</th></tr></thead><tbody><tr><td>

Account

</td><td>

Reference

</td><td>

customer\_account

</td></tr><tr><td>

Contact

</td><td>

Reference

</td><td>

customer\_contact

</td></tr><tr><td>

Consumer

</td><td>

Reference

</td><td>

csm\_consumer

</td></tr><tr><td>

Short Description

</td><td>

Single Line Text

</td><td>

N/A

</td></tr></tbody>
</table>    3.  In the Question related list for each variable, enter the following:

        1.  In **Question**, specify a question that explains the options available to the end user.

            For example, for the Account variable, enter `Select the account`.

        2.  In **Name**, enter the variable being referenced.

            For example, for the Account variable, enter `account` as the name.

    4.  Click **Submit** and repeat for all variables as needed.

6.  Navigate back to the record producer you created.

    1.  Navigate to **Available for** and add **SNC External** and **Users with sn\_customerservice.customer**.

    2.  Navigate to **Not available for** and remove any values.

7.  Click **Save**.


## Result

The record producer is created.

## What to do next

Add your record producer to the CSM portal. For more information, see [Add a record producer to CSM portal for B2B2C in Healthcare and Life Sciences Service Management Core](hcls-add-record-producer-csm-portal.md).

