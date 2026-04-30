---
title: Creating data classifications
description: Create your own user-defined data classifications in the Data Classification \[data\_classification\] table that you can then assign to specific columns in specific tables.
locale: en-US
release: xanadu
product: Data Classification
classification: data-classification
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Classification, Platform Privacy]
---

# Creating data classifications

Create your own user-defined data classifications in the Data Classification \[data\_classification\] table that you can then assign to specific columns in specific tables.

## Before you begin

Role required: data\_classification\_admin, admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Data classification** &gt; **Data classes**.

2.  Select **New**.

3.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Classification Name|Name of the data classification.|
    |Description|Description of the data classification.|
    |Parent|Name of the parent data classification that this data classification is subordinate to. Leave the field empty if this data classification is not a parent to child data classifications.|
    |Application|Application scope for this data classification.|

4.  If this data classification should be a parent to child data classifications, click **New**.

    If you do not want to create child data classifications, skip this step.

5.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Classification Name|Name of the child data classification.|
    |Description|Description of the child data classification.|
    |Parent|Name of the parent data classification that this data classification is subordinate to. Leave the field empty if this data classification is not a parent to child data classifications.|
    |Application|Application scope for this child data classification.|

6.  Click **Submit**.


