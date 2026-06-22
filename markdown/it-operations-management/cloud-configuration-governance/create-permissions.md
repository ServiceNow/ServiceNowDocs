---
title: Assign a cloud permission
description: Assign a permission to refine the actions that are allowed or prohibited for users based on the user group they belong to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-configuration-governance/create-permissions.html
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Permissions management for Cloud Governance roles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Assign a cloud permission

Assign a permission to refine the actions that are allowed or prohibited for users based on the user group they belong to.

## Before you begin

-   Role required: sn\_cmp.cloud\_governor
-   The [user group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_CreateAGroup.md) to which you want the permission applied.

## Procedure

1.  Navigate to **All** &gt; **Cloud Admin Portal** &gt; **Governance** &gt; **Permission**.

2.  Fill out the form fields \(see table\).

    \[Omitted image "permission-form.png"\] Alt text: Read permissions on cloud accounts

    |Field|Description|
    |-----|-----------|
    |Target type|Select the cloud table in which the target record belongs.|
    |All Entities|Select this option to apply the permission to all records in the table.|
    |Permission|Select the [permission type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/cloud-permissions.md).|
    |Target Entity|Select the record that the permission is based upon.|
    |Group|Select the user group.|

3.  Click **Submit**.


**Parent Topic:**[Permissions management for Cloud Governance roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/cloud-permissions.md)

