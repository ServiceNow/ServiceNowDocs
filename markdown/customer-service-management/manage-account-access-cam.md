---
title: Restrict contact access
description: Restrict contact access to sold products and install bases by limiting the access for associated contacts and their access levels for customer access management.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using customer access management, Customer management, Using Customer Service Management, Customer Service Management]
---

# Restrict contact access

Restrict contact access to sold products and install bases by limiting the access for associated contacts and their access levels for customer access management.

## Before you begin

Role required: sn\_customerservice\_manager and sn\_customerservice.customer\_admin

## About this task

By restricting contact access, you can limit access to entities that are based on the contacts that are assigned to the sold products and install bases. You can't create duplicate account access records with the same account.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Manage Account Access**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_esz_qdw_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

Accounts that have restrictions for access to the sold products and install bases that are based on the associated contacts and the access level.

</td></tr><tr><td>

Restrict Contact Access

</td><td>

Access that is restricted to entities based on associated contacts.

 If the value of the field is **False**, the contacts that are associated with the account can read the sold products and install bases that are associated with the account.

 If the value of the field is **True**, the contacts that are associated with the accounts don’t get access to the sold products and install bases, unless they're added as a contact on the record or as a related party. The following contacts get access to the sold products and install bases:

-   Contacts that are associated with the sold product and install base records.
-   Contacts that are added as related parties with an Authorized Representative responsibility.
-   Contacts belonging to accounts that are added as related parties with an Authorized Account responsibility.


</td></tr></tbody>
</table>4.  Select **Submit**.


**Related topics**  


[Add additional contacts for the sold product](adding-additional-contacts-soldproduct.md)

