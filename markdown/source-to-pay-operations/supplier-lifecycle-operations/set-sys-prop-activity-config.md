---
title: Set the property to configure activity configurations
description: Set the sn\_supplier\_sp.allow\_all\_apps\_configuration property to make activity configurations and filters accessible from all application scopes.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install Supplier Collaboration Portal, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Set the property to configure activity configurations

Set the **sn\_supplier\_sp.allow\_all\_apps\_configuration** property to make activity configurations and filters accessible from all application scopes.

## Before you begin

Role required: sn\_slm.admin

## About this task

If you set this system property to **true**, you can create or modify an activity configuration to display relevant activities in My active items widget of the Supplier Collaboration Portal. For more information, see [Configure properties for Supplier Case Management](../reference/config-prop-supp-mgmt.md).

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Administration** &gt; **Properties**.

2.  Select the check box for the **Allow "Activity Configurations" and "Filters" to be picked from all application scopes \(sn\_supplier\_sp.allow\_all\_apps\_configuration\)** property.

    By default, the check box for this property is deselected \(set to No\).

3.  Select **Save**.


**Parent Topic:**[Install Supplier Collaboration Portal](install-supp-central.md)

**Related topics**  


[Enable automatic creation of supplier cases from incoming emails](config-email-properties.md)

[Email format for contacts linked with multiple suppliers](email-format-for-contacts-linked-with-multiple-suppliers.md)

