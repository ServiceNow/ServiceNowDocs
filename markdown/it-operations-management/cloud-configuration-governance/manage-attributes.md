---
title: Manage operation attributes
description: You can specify attribute values for catalog items help cloud users to correctly provision catalog items. You can configure and manage attributes for provision, pre-provision, and post-provision operations.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Manage operation attributes

You can specify attribute values for catalog items help cloud users to correctly provision catalog items. You can configure and manage attributes for provision, pre-provision, and post-provision operations.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer.

## About this task

The attributes for provision, pre-provision, and post-provision operations are generated automatically. You can generate variables for these attributes and also create new attributes for the resource operation. You can also use the Pre-Provision Operation, Post-Provision Operation or Lifecycle Operations related lists to create variables for Orchestration attributes.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Catalog Items**.

2.  Open a catalog item and click the Pre-Provision Operation or Post-Provision Operation related list.

    The Operations Step page lists the operations.

    ![Post-provisioning attributes](../image/manage-attributes-post-provision.png)

3.  Click an operation to view its corresponding attributes.

4.  Configure the attributes for each operation.

    -   **Mapping**: View the auto-generated mapping values for each attribute. Mappings specify where to pull the information in the system. To modify the expression mappings, double-click the mapping value and enter new values. Then click the check mark icon \(![check mark icon](../image/icon-check-mark.png)\). Expressions can hold the values for information that's dynamically generated in the system, such as the values for the selections that users make in the Cloud User Portal. See [Using expressions in Cloud Provisioning and Governance](../reference/expressions-cloud-mgt.md).
    -   **Generate Variable**: Generates a variable for an attribute. Double-click the value \(**false**\), select **True**, and click the check mark icon \(![check mark icon](../image/icon-check-mark.png)\).
5.  Click **Apply Changes** after you've made all the required changes.

    All the configurations you made to the attributes are saved and you're returned to the Cloud Catalog Items screen.


