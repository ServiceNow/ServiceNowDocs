---
title: Account Address table
description: Avoid duplication of address records by using the Account Address table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enhanced address data model for accounts, Configure accounts and contacts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Account Address table

Avoid duplication of address records by using the Account Address table.

The Account Address \[account\_address\_relationship\] table maintains the relationship between an address and the accounts that use that address.

The Account Address table eliminates the need to duplicate address records that must be reused across multiple accounts. The Account Address table provides details like the name and the location of the account. The table also provides information on the type of account address, and whether the account is primary or not.

The Account Address table is available for use when the Enhanced address data model for accounts feature is enabled. For more information on enabling the feature and configuring the Account Address table, see [Enable enhanced address model for accounts](../task/enable-enhanced-address-model.md). When address sharing is enabled, Account address related list is visible on the account and location forms.

If you have any one of the sn\_crm\_account\_data\_manager, sn\_crm\_account\_relationship\_data\_manager, sn\_crm\_foundation\_data\_manager, and sn\_crm\_foundation\_admin, roles, you can create, update, view and delete account address records. If you have the sn\_crm\_account\_viewer, sn\_crm\_account\_relationship\_viewer, or sn\_crm\_foundation\_data\_viewer role, you can view the account address records.

|Field|Description|
|-----|-----------|
|Location|The location or address associated with the account.|
|Account|The name associated with the account.|
|Primary|An account can only have one primary address.|
|Type|The type of account address, whether Billing, Shipping or Mailing.|

![Fields in the Account Address New Record form to set up the Account and Location information.](../image/account-address-form.png "Account Address form")

**Related topics**  


[Enable enhanced address model for accounts](../task/enable-enhanced-address-model.md)

[Associate an address to an account](../task/associate-address-account.md)

