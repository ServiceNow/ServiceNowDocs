---
title: Module lifecycle policy exceptions for Field Encryption
description: Use module lifecycle policy exceptions to customize the lifecycle of your module keys.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Module lifecycle policy exceptions for Field Encryption

Use module lifecycle policy exceptions to customize the lifecycle of your module keys.

## Before you begin

Role required: KMF Admin or KMF Cryptographic Manager

## About this task

Module lifecycle policy exceptions change the lifecycle policy of Field Encryption modules from the standard Instance-level lifecycle policy. For example, if you've configured symmetric keys to be limited to one year at the instance level, you can create a module lifecycle policy exception for a specific Field Encryption module to allow its key to remain active for two years.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Modules**.

2.  Select the field encryption module record that requires a module lifecycle policy exception.

3.  In the field encryption module record, select **New** in the **Module Policy Exceptions** related list.

4.  In the key lifecycle policy form, fill in the fields as needed.

    |Field|Description|
    |-----|-----------|
    |Crypto Module|Displays the name of the field encryption module that will use this policy exception.|
    |Applies To|The specified key is auto populated.|
    |Key Type|Select the key type. Exception policies are related to a specific key. Multiple exception policies can be created per Field Encryption Module.|
    |Policy Condition|Create qualifying conditions from the drop-down menu and complete the additional constraint criteria.|
    |Result|Select **Reject** to reject use of the key or **Track** to allow use of it when the criteria are met.|

5.  Select **Submit**.


**Parent Topic:**[Configuring Field Encryption](../concept/configuring-column-level-encryption.md)

