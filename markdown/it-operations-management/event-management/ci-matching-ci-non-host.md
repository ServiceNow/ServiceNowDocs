---
title: Bind non-host CIs using CI field matching
description: If no match is found using the Node field, the system uses the CI identifier field to match alerts with non-host CIs based on attributes like Name, FQDN, IP, or MAC. This ensures accurate alert association, improving visibility, troubleshooting, and root cause analysis for diverse infrastructure components.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Overriding default binding, Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Bind non-host CIs using CI field matching

If no match is found using the **Node** field, the system uses the **CI identifier** field to match alerts with non-host CIs based on attributes like Name, FQDN, IP, or MAC. This ensures accurate alert association, improving visibility, troubleshooting, and root cause analysis for diverse infrastructure components.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

If no match is found using the **Node** field, the system looks at the **Additional information** field of the alert. When you select a CI type, such as File System, the system automatically searches for a matching record in the \[cmdb\_ci\_file\_system\] table. It uses the details provided in event rule record, specifically in the **Additional information** field, to refine the search. For example, if the **Additional information** field contains values like `{"mount_point": "/snap/amazon-ssm-agent/9565", "name": "/dev/loop0"}`, the system looks for a record in the \[cmdb\_ci\_file\_system\] table that matches these values. If a match is found, the system binds the CI to the alert, ensuring accurate identification and association. Similarly, if the **CI type** is **Network Adapter**, the system searches in the \[cmdb\_ci\_network\_adapter\] table.

There may be cases where no match is found because the column names in the event record and the table differ for the same item. In such cases, you can manually create an additional key-value pair with a name matching the table column, ensuring the matching process continues successfully. For information on how to create a manual field, see [Bind CIs using CI field matching and handling column name differences](ci-matching-manual-field.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Select **New** and complete the required fields of the event rule.

3.  Select the **Binding** tab.

4.  Select the **Override default binding** check box.

5.  In the **Binding type** field, select **CI field matching**.

    ![Binding type is CI field matching](../image/em-ci-field-matching-non-host.png)

6.  Select the **Transform and Compose Alert Output** tab.

7.  Clear the **Node** field value.

    ![Node field must be cleared.](../image/em-ci-field-matching-node.png)

8.  In the **CI type** field, select the non-host CI.

    A non-host CI type is any CI type that does not extend the \[cmdb\_ci\_hardware\] table, such as a Service or VM. The **CI type** determines the specific CMDB table where the system searches for the matching CI.

9.  Select **Save**.


