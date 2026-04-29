---
title: Add custom record producers to the service catalog in Care Team Operations for Facilities
description: Add custom record producers that you've configured into service catalogs in Care Team Operations for Facilities.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Operations for Facilities, Healthcare Operations, Healthcare and Life Sciences]
---

# Add custom record producers to the service catalog in Care Team Operations for Facilities

Add custom record producers that you've configured into service catalogs in Care Team Operations for Facilities.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Record Producers**.

2.  Select **New**.

3.  Set the table name to **Healthcare Facilities Case \[sn\_cto\_facilities\_case\]**.

4.  In the Accessibility tab, set Catalogs to **Facilities service**.

5.  Set the Category field to the desired service category.

6.  Add in the following common variable sets.

    |Title|Description|
    |-----|-----------|
    |**Facilities location set**|Contains a reference to the common location field to confirm that Facilities support agents can view where support is needed.|
    |**Facilities priority set**|Contains a reference to the Priority and Available Start fields.|
    |**Facilities description set**|Contains a reference to the Description field.|

7.  Add in the following catalog client scripts.

    |Catalog client script|Description|
    |---------------------|-----------|
    |**Populate Facilities session param**|Enables tokenized data to be captured when launched inside of Epic Hyperspace.|
    |**Clear location on unit change**|Clears the location field when the requesting unit is changed so that only locations associated with the current unit are shown.|

8.  Fill in other fields as needed.

9.  Select **Save**.


## Result

You have created a custom record producer for use with Care Team Operations for Facilities.

