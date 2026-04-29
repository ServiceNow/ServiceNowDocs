---
title: Map a device user to a ServiceNow DEX user
description: Complete this procedure to map a device user to a DEX user so you can notify the user about any of the device metrics breaching a predetermined threshold.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced configuration, Configure, Digital End-User Experience, IT Service Management]
---

# Map a device user to a ServiceNow DEX user

Complete this procedure to map a device user to a DEX user so you can notify the user about any of the device metrics breaching a predetermined threshold.

## Before you begin

Role required: admin

## About this task

Column `user_name` on the base system is used for mapping user records in the `sys_user` table. In this case, the `user_name` matches the user id on the device. You can map a custom ServiceNow DEX user column to a device user id.

## Procedure

1.  Change the application scope from global to DEX Application and Device Health.

2.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

3.  Search for `sn_dex.dex_user_ref_mapping`.

4.  Select the property.

5.  In the pre-populated form, update the **Value** field as follows:

    1.  Copy the example JASON string from the **Description** field: `{"prefix": "dex-blah", "device_user_id_column": "first_name", "suffix": "dex-blah"}`

    2.  Paste the JASON string to the **Value** field and update as appropriate.

        -   `prefix`: Provide the prefix value if appropriate or leave it empty.
        -   `device_user_id_column`: Provide the value for the column to which you’re mapping.
        -   `suffix`: Provide the suffix value if appropriate or leave it empty.
        For example, `{"prefix": "", "device_user_id_column": "login", "suffix": "@example.com"}`.

6.  Select **Submit**.


**Parent Topic:**[Advanced configuration](dex-advanced-configuration.md)

