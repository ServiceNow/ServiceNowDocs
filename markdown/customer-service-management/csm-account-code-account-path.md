---
title: Account codes and account paths
description: An account code is a unique identifier for an account, while an account path establishes the account hierarchy.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Import accounts and contacts with guided setup, Configure accounts and contacts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Account codes and account paths

An account code is a unique identifier for an account, while an account path establishes the account hierarchy.

## Account codes

An account code is a unique key that identifies an account in a ServiceNow instance. This code is stored in the **Account Code** field on the Account form.

An account code must be unique. Attempting to insert a new record with previously existing account code in the Account \[customer\_account\] table, the value for the code results in the following error:

`java.sql.BatchUpdateException: Duplicate entry for key account_path`

## Account paths

An account path establishes the hierarchy among different accounts. This path is stored in the **Account Path** on the Account form.

An account path is a combination of the account codes for each account in the hierarchy. For example, let's use the following accounts to demonstrate account paths.![Account hierarchy example with three levels of parent and child companies](../image/csm-config-workspace-account-hierarchy-example.png)

<table id="table_mxm_dst_jyb"><thead><tr><th>

Account

</th><th>

Account Code

</th><th>

Account Path

</th></tr></thead><tbody><tr><td>

Boxeo

</td><td>

~~~~1

</td><td>

~~~~1

 Boxeo is the parent company. The account path for Boxeo is the same as the account code, which indicates that it’s the first element in the hierarchy.

</td></tr><tr><td>

Boxeo USA

</td><td>

~~~~2

</td><td>

~~~~1/~~~~2

 Boxeo USA is a child company of Boxeo. The structure of the account path is interpreted as Boxeo/Boxeo USA.

</td></tr><tr><td>

Boxeo EMEA

</td><td>

~~~~3

</td><td>

~~~~1/~~~~3

 Boxeo EMEA is also a child company of Boxeo and the structure of the account path is interpreted as Boxeo/Boxeo EMEA.

</td></tr><tr><td>

Boxeo France

</td><td>

~~~~5

</td><td>

~~~~1/~~~~3/~~~~5

 Boxeo France is a child company of Boxeo EMEA. The structure of this account path is interpreted as Boxeo/Boxeo EMEA/Boxeo France.

</td></tr></tbody>
</table>## Importing account records

If you create your account records by importing the data from some source system through a transform map, make sure that you execute the business rules. The Account Path is added, updated, and deleted based on the insertion, updating, and deletion of records in the Account \[customer\_account\] table through the business rules. If the business rules aren’t executed, it can result in empty account paths, which can then result in data access issues.

**Note:** If you don’t execute the business rules during import, run the script in the **Update account path** business rule for the newly imported records to set the account paths correctly.

