---
title: Create a data privacy policy
description: Configure a data privacy policy to specify which data privacy techniques are used when anonymizing your data.
locale: en-US
release: yokohama
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data privacy \(Classic\) configuration, Data privacy \(Classic\), Data Privacy, Platform Privacy]
---

# Create a data privacy policy

Configure a data privacy policy to specify which data privacy techniques are used when anonymizing your data.

## Before you begin

The data privacy configuration defines tables, sys\_user and other, and columns to the de-identified, depending on the use case and specifies parameterized types of the techniques to be used while de-identifying data.

**Note:** To complete a privacy configuration, you must first configure a data privacy technique configuration. See [Create a data privacy technique configuration](config-dp-technique.md) for more information.

Role required: data\_privacy\_admin and admin

## Procedure

1.  Elevate to the **data\_privacy\_admin** role.

    For details on role elevation, see [Elevate to a privileged role](t_ElevateToAPrivilegedRole.md).

2.  Navigate to **System Security** &gt; **Data Privacy \(Classic\)** &gt; **Privacy Policy Configuration**.

3.  Select **New**.

4.  In the **Name** field, enter a name for your privacy policy configuration.

5.  In the **Data Class** field, select the data class to use with this policy.

    Data privacy policies can only apply to classified data, for more information on data classification, see [Data classification](../concept/data-classification.md).

    After selecting a data class, the **Privacy Classified Field Techniques** and **Privacy Primary Reference Links** lists display on the form.

6.  Select **Apply to All Data in Class** to apply anonymization to all data in the chosen data class.

    If you don’t select this field, your data privacy processor users can choose which users to anonymize when creating data privacy jobs. If you select this field, that option is not available.

    -   **Apply when Cloning**: This option becomes available. When selected, the privacy configuration executes during data privacy clone.
    -   **Application Order**: A data privacy job for Postclone configuration with a higher Application Order might start before another job with lower order.

        **Important:** Avoid creating multiple data privacy policies with the same Application Order, as the resultant processing order for those with the same order will be inconsistent.

7.  Select **Supports Rollback** to enable the ability to de-anonymize the data from a data privacy job.

    See [Roll back a data privacy job](rollback-data-privacy-job.md) for more information.

    After selecting **Supports Rollback** when creating a data privacy job, the option to roll back the job becomes available.

8.  Select the **Privacy Classified Field Techniques** tab to display the **Privacy Classified Field Techniques** list.

9.  Select an entry in the **Table** field to open the **Privacy Technique Configuration** field for each list entry.

    The **Privacy Classified Field Techniques** list displays all the data to be anonymized in your selected data class. For each of these entries, you must select a privacy technique to apply.

10. Select a **Privacy Technique Configuration** to apply.

    **Important:** If you aren’t anonymizing an entry, select the **DoNothing** technique rather than leaving the entry empty. Policies with empty values in the **Privacy Technique Configuration** field can’t execute when used in data privacy jobs.

11. Select **Submit** or **Save** to save the record.


## What to do next

[Configure a data privacy job](config-data-privacy-job.md).

