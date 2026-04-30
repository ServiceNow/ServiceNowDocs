---
title: Create anonymization policies
description: Configure an anonymization policy to specify which techniques are used when anonymizing your data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Data anonymization, Platform Privacy]
---

# Create anonymization policies

Configure an anonymization policy to specify which techniques are used when anonymizing your data.

## Before you begin

The data privacy configuration defines tables, sys\_user and other, and columns to the de-identified, depending on the use case and specifies parameterized types of the techniques to be used while de-identifying data.

**Note:** To complete a privacy configuration, you must first configure a data privacy technique configuration. See [Create anonymization techniques](dps-create-anonymization-techniques.md)for more information.

Role required: data\_privacy\_admin and admin

## Procedure

1.  Elevate to the **data\_privacy\_admin** role.

    For details on role elevation, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

2.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Anonymization**.

    All anonymization policies display. Published policies are available to schedule the anonymization job.

3.  Select **Create new policy**.

4.  Select to either anonymize **Data tables or columns**, **User specific data**, or **Real time data**.

    ![New policy selection window.](../image/create-new-policy.png)

    |Data Type|Description|
    |---------|-----------|
    |Data tables or columns|Records that match the data policy will be anonymized.|
    |User specific data|Select a set of users or user groups to be anonymized.|
    |Real time data|Anonymize real time entries for a set of columns. See [Real time anonymization](../concept/real-time-anonymization.md) for more information.|

    Data privacy policies can only apply to classified data, for more information on data classification, see [Data classification](../concept/dps-data-classification.md).

5.  Select **Create**.

    There are sequential steps required to complete the policy, **Define details**and **Assign techniques**. **Select user reference** is also required when defining the policy for user specific data.

6.  Define the details for the new anonymization policy.

    -   Enter the policy name in the **Name** field, and the policy description in the **Description** field.
    -   In the **Data Class** field, select the data class to use with this policy.
    **Note:** If you are not anonymizing an entry, select the **DoNothing** technique rather than leaving the entry empty. Policies with empty values in the Privacy Technique Configuration field cannot execute when used in data privacy jobs.

    After selecting a data class, the Assign techniques form displays for each record returned for the defined data class.

7.  Assign anonymization techniques for the selected data class.![The bulk assign techniques form.](../image/bulk-assign-technique.png)

<table id="choicetable_ywk_ywc_dwb"><thead><tr><th align="left" id="d166217e268">

Option

</th><th align="left" id="d166217e271">

Description

</th></tr></thead><tbody><tr><td id="d166217e277">

**Select __Bulk Assign Techniques__**

</td><td>

Applies anonymization to all data records in the chosen data class. Select the data type and the anonymization technique to apply to all entries with the selected data type. Repeat this step for additional bulk assignments of different data types.See [Supported field types for anonymization](../../security/reference/data-privacy-supported-data-types.md) for a list of data types.

</td></tr><tr><td id="d166217e299">

**Select an __anonymization technique__ for each data column record**

</td><td>

Your data privacy processor users can choose which records to anonymize when creating data privacy jobs. Individually apply anonymization to each data record in the chosen data class.

</td></tr></tbody>
</table>    ![Individually assign a technique.](../image/assign-technique.png)

8.  Enter child tables to be scanned.

    Child tables of the parent will be anonymized, if a table has no children this option will not be available.

    **Warning:** A parent job will fail if a child job fails.

9.  If Data Pattern Anonymization is selected, select the anonymization technique to be used.

10. Set the ordering for data patterns.

11. **Tip:** Use the **Test** feature to test sample inputs. You can review metrics from the result like scan time, result, and discovered patterns.

    Select the **Test** button to test the policy.

12. **Important:** All tables must have a correct sys\_dictionary entry.

    Select **Save**.

13. Select **Publish** to update the anonymization policy for scheduling and be returned to Anonymization policies.

    **Note:** Only published policies can be used for anonymization job scheduling.


## What to do next

[Create anonymization job](dps-create-anonymization-job.md).

