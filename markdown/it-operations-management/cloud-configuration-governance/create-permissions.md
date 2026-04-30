---
title: Assign a cloud permission
description: Assign a permission to refine the actions that are allowed or prohibited for users based on the user group they belong to.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Permissions management for Cloud Governance roles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Assign a cloud permission

Assign a permission to refine the actions that are allowed or prohibited for users based on the user group they belong to.

## Before you begin

-   Role required: sn\_cmp.cloud\_governor
-   The [user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) to which you want the permission applied.

## Procedure

1.  Navigate to **All** &gt; **Cloud Admin Portal** &gt; **Governance** &gt; **Permission**.

2.  Fill out the form fields \(see table\).

    ![Read permissions on cloud accounts](../image/permission-form.png "Read permissions on cloud accounts")

    |Field|Description|
    |-----|-----------|
    |Target type|Select the cloud table in which the target record belongs.|
    |All Entities|Select this option to apply the permission to all records in the table.|
    |Permission|Select the [permission type](../concept/cloud-permissions.md#default-permission).|
    |Target Entity|Select the record that the permission is based upon.|
    |Group|Select the user group.|

3.  Click **Submit**.


**Parent Topic:**[Permissions management for Cloud Governance roles](../concept/cloud-permissions.md)

