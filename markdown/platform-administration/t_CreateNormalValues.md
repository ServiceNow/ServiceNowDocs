---
title: Create a normal value
description: A normal value is a simplified, generic value for a field that replaces all the possible variants of that value that exist in the database.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Normal values, Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a normal value

A normal value is a simplified, generic value for a field that replaces all the possible variants of that value that exist in the database.

## Before you begin

Role required: admin or normalizer

## About this task

Normal values should be clear and unambiguous.

After the platform runs the data job, the **Pending Values** related list on the Data normalization jobs form is populated with all the unique values for the field in the database. Examine the values in the list and decide which normalizing method is best for the existing data. For example, define an alias for a small pool of values and a rule for a large pool of values..

## Procedure

1.  Navigate to **All** &gt; **Field Normalization** &gt; **Normalizations**.

2.  Open the appropriate normalization record.

3.  Click the **Normal Values** related list.

4.  Click **New**.

5.  In the Normal Value form, create normal values for the variants in the **Pending Values** related list.

    Pending values are used to replace the variants configured as aliases.


