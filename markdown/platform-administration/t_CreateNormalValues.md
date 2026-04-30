---
title: Create a normal value
description: A normal value is a simplified, generic value for a field that replaces all the possible variants of that value that exist in the database.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Normal values, Field normalization and transformation, Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a normal value

A normal value is a simplified, generic value for a field that replaces all the possible variants of that value that exist in the database.

## Before you begin

Role required: admin or normalizer

## About this task

Normal values should be clear and unambiguous.

After the platform runs the data job, the **Pending Values** related list on the Data normalization jobs form is populated with all the unique values for the field in the database. Examine the values in the list and decide which normalizing method is best for the existing data. For example, define an alias for a small pool of values and a rule for a large pool of values. The following screenshot shows the pending values for CPU types in Linux servers in a network. The list contains several choices for Intel Xeon CPUs, which might be normalized as **Xeon**.

![](../image/NormalizationPendingValues2.png "Normalization pending values 2")

## Procedure

1.  Navigate to **All** &gt; **Field Normalization** &gt; **Normalizations**.

2.  Open the appropriate normalization record.

3.  Click the **Normal Values** related list.

4.  Click **New**.

5.  In the Normal Value form, create normal values for the variants in the **Pending Values** related list.

    These are the values the platform uses to replace the variants configured as aliases.

    ![Normalization normal values](../image/NormalizationNormalValues1.png)


