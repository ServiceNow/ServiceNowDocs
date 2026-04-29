---
title: Set the account code property
description: After importing customer account information, update the com.snc.cs\_base.last.generated.code.tree.path property with the correct account code value.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Import accounts and contacts with guided setup, Configure accounts and contacts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Set the account code property

After importing customer account information, update the **com.snc.cs\_base.last.generated.code.tree.path** property with the correct account code value.

## Before you begin

Role required: import\_admin and sn\_crm\_foundation\_admin

## About this task

The **com.snc.cs\_base.last.generated.code.tree.path** system property stores the **Account Code** value for the most recently created customer account in the Account \(customer\_account\) table.

When you create a customer account record, the system uses this property to generate a unique account code. The property is then updated with the latest value, confirming the next account record receives a new unique code.

The value of the **com.snc.cs\_base.last.generated.code.tree.path** property must match the value of the Account Code field for the last inserted customer account record. When you create customer account records by importing data from other sources or instances, these values can get out of synchronization. If these values don’t match, the system generates an error on the creation of the next new record in the Account table:

`java.sql.BatchUpdateException: Duplicate entry for key account_path`

Use the following steps to fix this error.

## Procedure

1.  Determine the highest or last used account code value from the account \(customer\_account\) table.

2.  Navigate to the System Property \[sys\_properties\] table.

3.  Set the **com.snc.cs\_base.last.generated.code.tree.path** property to the value determined in step 1.


