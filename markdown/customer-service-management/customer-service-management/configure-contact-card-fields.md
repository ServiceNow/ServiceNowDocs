---
title: Configure fields on the Contact Card in the Customer Information view
description: Change the fields that display on the Contact Card in the Customer Information view of the . Edit the Contact Card - Fields Generator client script to add fields beyond the out-of-the-box defaults.
locale: en-US
release: brazil
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
---

# Configure fields on the Contact Card in the Customer Information view

Change the fields that display on the Contact Card in the Customer Information view of the . Edit the Contact Card - Fields Generator client script to add fields beyond the out-of-the-box defaults.

## Before you begin

Role required: admin

## About this task

The out-of-the-box **Contact** and **Consumer** record configurations ship with a fixed set of default fields on the Contact Card, and their **Fields** value on the Record Configuration form is locked. To display additional or different fields on the Contact Card, edit the **Contact Card - Fields Generator** client script for the **Customer Central** experience in UI Builder.

The Contact Card displays the following default fields for each context table:

|Context table|Default fields|
|-------------|--------------|
|Contact \[customer\_contact\]|Mobile phone, Business phone, Account, Email, Location.Street, Location.City, Location.State/Province, Country code, Active|
|Consumer \[csm\_consumer\]|Mobile phone, Business phone, Email, Street, City, State|

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **Customer Central** experience.

3.  Open the **Customer Information** page, and then select the **Customer Information Default** variant.

4.  In the left panel, under **Client scripts**, select **Contact Card - Fields Generator**.

5.  In the Edit client script dialog, locate the `DEFAULT_FIELDS` object and the entry for the context table you want to modify.

    The entry key matches the context table name: `customer_contact` for **Contact**, and `csm_consumer` for **Consumer**.

6.  Edit the `fields` value to add or remove field names.

    The value is a comma-separated string of field names on the context table. Use dot-walked notation for related fields, for example `location.city`.

7.  Select **Apply**.


**Related topics**  


[Configure records for the Customer Information view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-ci-records.md)

