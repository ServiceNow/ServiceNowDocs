---
title: Add custom record producers to the service catalog in Care Team Operations for Environmental Services
description: Add custom record producers that you have configured into service catalogs in Care Team Operations for Environmental Services.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Operations for Environmental Services, Healthcare Operations, Healthcare and Life Sciences]
---

# Add custom record producers to the service catalog in Care Team Operations for Environmental Services

Add custom record producers that you have configured into service catalogs in Care Team Operations for Environmental Services.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Record Producers**.

2.  Select **New**.

3.  Set the table name to **Healthcare EVS Case \[sn\_cto\_evs\_case\]**.

4.  In the Accessibility tab, set Catalogs to **EVS service**.

5.  Set the Category field to the desired service category.

6.  Add in the following common variable sets.

    |Title|Description|
    |-----|-----------|
    |**EVS location set**|Contains a reference to the common location field to confirm that Environmental Services support agents can view where support is needed.|
    |**EVS priority set**|Contains a reference to the Priority and Available Start fields.|
    |**EVS description set**|Contains a reference to the Description field.|

7.  Recommended - Add in the following catalog client scripts.

    |Catalog client script|Description|
    |---------------------|-----------|
    |**Populate Facilities session param**|Enables tokenized data to be captured when launched inside of Epic Hyperspace.|
    |**Clear location on unit change**|Clears the location field when the requesting unit is changed so that only locations associated with the current unit are shown.|

8.  Fill in other fields as needed.

9.  Select **Save**.


