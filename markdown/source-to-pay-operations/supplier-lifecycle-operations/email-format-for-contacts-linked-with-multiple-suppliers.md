---
title: Email format for contacts linked with multiple suppliers
description: Contacts linked with multiple suppliers have to include the supplier's legal name while sending emails for automatic creation of cases.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure properties, Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Email format for contacts linked with multiple suppliers

Contacts linked with multiple suppliers have to include the supplier's legal name while sending emails for automatic creation of cases.

When a supplier contact is mapped to only one supplier and sends an email, a case is created with that supplier. However, when the supplier contact is mapped to multiple suppliers, the supplier's legal name is retrieved from the email body.

**Important:** The valid supplier's legal name must be included in the email body in the following format:

```
Supplier: <supplier legal name>
```

When a supplier contact mapped to multiple suppliers sends an email for case creation, the following scenarios can occur:

## Supplier's legal name is correctly mentioned in the email

When the supplier's legal name is included in the email in the given format, the supplier case is created with the supplier name provided in the email.

## Supplier's legal name is not correctly mentioned in the email

When the supplier's name is not the exact legal name, a case is still created with the **Supplier** field set as empty. An auto-email is sent to the supplier contact requesting for the valid supplier's legal name. Once the supplier contact shares the supplier's legal name, it has to be added manually by the assigned person. The case is then assigned and the Supplier field is updated to mandatory.

**Parent Topic:**[Configure properties for Supplier Case Management](../reference/config-prop-supp-mgmt.md)

**Related topics**  


[Enable automatic creation of supplier cases from incoming emails](config-email-properties.md)

