---
title: Encrypt search fields to appear in search assist
description: Encrypt search fields to search from a field other than the first name, last name, and phone fields. By encrypting search fields, you can configure them to appear in search assist.
locale: en-US
release: xanadu
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Vaccine Administration Management, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Encrypt search fields to appear in search assist

Encrypt search fields to search from a field other than the first name, last name, and phone fields. By encrypting search fields, you can configure them to appear in search assist.

## Before you begin

Role required: security\_admin

## About this task

You can encrypt fields such as the street, city, state, and zip code based on your organization's requirement. Decrypted fields are kept hidden from the search assist. By default, the first name, last name, and phone fields are visible to users.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations**.

2.  In the **Search** field, enter `sn_vaccine_sm_personal_info`.

    In the Encrypted Field Configurations table, you can see multiple `sn_vaccine_sm_personal_info` fields.

3.  Right-click the Active column and select **Group By Active**.

4.  In the **Active** field, select **False**.

5.  Click **Update**.

6.  To encrypt or decrypt fields, repeat steps 3 through step 5, as needed.


**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

