---
title: Configure group ACL for aggregation requests
description: Use the glide.sg.group\_acl.enabled system property to control the validation of access control lists \(ACL\) during aggregation requests that are related to displaying results from data items that use grouping.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System properties, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure group ACL for aggregation requests

Use the **glide.sg.group\_acl.enabled** system property to control the validation of access control lists \(ACL\) during aggregation requests that are related to displaying results from data items that use grouping.

## Before you begin

Role required: admin

## About this task

The **glide.sg.group\_acl.enabled** system property determines whether ACL validation is performed when executing grouping operations. By default, this property is set to `true`. When this system property is set to `true`, an ACL is applied to check whether the record involved in the grouping operation is accessible. This default mobile platform behavior is different from the ServiceNow® instance behavior. The instance doesn't apply ACLs when it displays aggregation result counts. This is a key difference between instance and mobile platform behavior.

When this system property is set to `false`, the system doesn't validate ACLs while it executes a grouping operation. In this case, aggregate results are based on the selected aggregation field and the number of records for each group. In most cases, this shouldn't lead to security issues because ACL checking is still enforced for all other operations.

## Procedure

1.  Type `sys_properties.list` in the filter navigator.

2.  In the System Properties screen, select **New**.

    Make sure that the Application scope is set to **Global**.

3.  Use the following information to complete the fields on the system property form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter `glide.sg.group_acl.enabled`.|
    |Type|Select **true \| false**.|
    |Value|Enter `true`.|

4.  Select **Submit**.

    **Note:** This system property only affects aggregation requests that are related to displaying results from data items that use grouping. ACL checking remains active for all other operations.


**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)

