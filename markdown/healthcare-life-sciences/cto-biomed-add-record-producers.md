---
title: Add custom record producers to the service catalog in Care Team Operations for Biomed
description: Add custom record producers you have configured into service catalogs in Care Team Operations for Biomed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Add custom record producers to the service catalog in Care Team Operations for Biomed

Add custom record producers you have configured into service catalogs in Care Team Operations for Biomed.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Record Producers**.

2.  Select **New**.

3.  Set the table name to **Healthcare Biomed Case \[sn\_cto\_biomed\_case\]**.

4.  In the Accessibility tab, set Catalogs to **Biomed service**.

5.  Set the Category field to the desired service category.

6.  Add in the following common variable sets.

    |Title|Description|
    |-----|-----------|
    |**Description set**|Contains the short description and description fields.|
    |**Care Team Portal Asset Model Set**|Contains a reference to the asset model.|
    |**Care Team Portal Asset Tag Set**|Contains the asset tag or serial number and the identified asset. Used in combination with the catalog client script to identify the asset by its asset tag or serial number and sets the reference field to the asset.|
    |**Requesting unit set**|Contains the requesting service organization.|
    |**Urgency set**|Contains the urgency field.|

7.  Recommended - Add in the following catalog client scripts.

    |Catalog client script|Description|
    |---------------------|-----------|
    |**Populate biomed service session params**|Allows tokenized data to be captured when launched inside of Epic Hyperspace when reporting other biomed issue.|
    |**Clear location on unit change**|Clears the location field when the requesting unit is changed so that only locations associated with the current unit are shown.|
    |**Clear location on asset change**|Clears the location field when the asset is changed so that only locations associated with the current asset are shown.|
    |**Populate med device session params**|Allows tokenized data to be captured when launched inside of Epic Hyperspace when reporting a medical device issue.|
    |**Populate phone number on user selection**|Populates phone number when a contact person is selected.|
    |**Update biomed service description**|Aggregates the contact person information and appends it to the case description when reporting other biomed issue.|
    |**Update contact on unit change**|Clears contact person field when the unit is changed so only contact persons associated with the new unit are shown.|
    |**Update medical device issue description**|Aggregates the contact person information and appends it to the case description when reporting a medical device issue.|

8.  Fill in other fields as needed.

9.  Select **Save**.


## Result

You have created a custom record producer for use with Care Team Operations for Biomed.

