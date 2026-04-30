---
title: Enable automatic creation of supplier cases from incoming emails
description: The supplier administrator can set this property to create a supplier case automatically from an incoming email.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure properties, Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Enable automatic creation of supplier cases from incoming emails

The supplier administrator can set this property to create a supplier case automatically from an incoming email.

## Before you begin

Role required: admin

## About this task

Supplier Case Management automatically creates a supplier case if the incoming email address matches with the email address specified in this property. For more information, see [Configure properties for Supplier Case Management](../reference/config-prop-supp-mgmt.md).

If you use the automatic case creation functionality in both Supplier Case Management \(SCO\) and Sourcing and Procurement Operations \(SPO\), ensure that each instance is configured with a unique email address in the **Automatic creation of cases from email** property. This ensures that the instance can correctly match incoming emails to the appropriate user and create the corresponding case.

For example:

-   In SLO, set the email address to [supplierhelp@acme.com](mailto:supplierhelp@acme.com) for creating supplier cases.
-   In SPO, set the email address to [procurementhelp@acme.com](mailto:procurementhelp@acme.com) for creating procurement cases. For more information, see [Automatic case creation from emails](../../sourcing-procurement-operations/concept/case-creation-from-emails.md).

This approach enables seamless case creation and accurate email-to-user mapping.

## Procedure

1.  Navigate to **All** &gt; **Supplier Case Management** &gt; **Administration** &gt; **Properties**.

2.  In the **Automatic creation of cases from email** field, enter the email address of the incoming email.

3.  Select **Save**.

    **Note:** After M2M mapping between supplier contact and suppliers is enabled, the contacts linked with multiple suppliers have to include the supplier's legal name while sending emails for automatic creation of cases. For more information, see [Email format for contacts linked with multiple suppliers](email-format-for-contacts-linked-with-multiple-suppliers.md).


**Parent Topic:**[Configure properties for Supplier Case Management](../reference/config-prop-supp-mgmt.md)

**Related topics**  


[Email format for contacts linked with multiple suppliers](email-format-for-contacts-linked-with-multiple-suppliers.md)

