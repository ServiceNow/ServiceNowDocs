---
title: Create an account relationship type
description: Create an account relationship type by defining the types of source and target accounts and providing a name for the relationship between these accounts.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Bi-directional account relationships, Create customer relationships, Configure accounts and contacts, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Create an account relationship type

Create an account relationship type by defining the types of source and target accounts and providing a name for the relationship between these accounts.

## Before you begin

Role required: admin

## About this task

Use the steps below to create an account relationship type.

You can edit an existing account relationship type by changing the types of source and target accounts and the name of the relationship that exists between these accounts. If that account relationship type is currently being used by any account relationship records, the **Relationship** and **Reverse relationship** fields in those records are automatically updated.

You can also delete an existing account relationship type.

-   If there are no account relationship records that use the account relationship type, then it is simply deleted.
-   If there are active account relationship records that use the account relationship type, an attempt to delete that relationship type results in a warning message. Deleting an account relationship type also deletes the relationship records based on that type.

Account relationship types can be set to inactive at any time.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Account Relationship Types**.

2.  Click **New**.

3.  Fill in the fields on the Account Relationship Type form.

<table id="table_gza_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Relationship type

</td><td>

A unique name that identifies the type of relationship. For example, Service Provider.

</td></tr><tr><td>

From

</td><td>

The type of source account for this relationship type; can be either an account or a partner.

</td></tr><tr><td>

Relationship

</td><td>

A text field where you can name the relationship from the source account to the target account. For example, Service provider for.

</td></tr><tr><td>

To

</td><td>

The type of target account for this relationship type; can be either an account or a partner.

</td></tr><tr><td>

Reverse relationship

</td><td>

A text field where you can name the reverse relationship from the target account to the source account. For example, Customer of.

</td></tr><tr><td>

Active

</td><td>

Sets the account relationship type as active or inactive. Active account relationship types can be used to create account relationship records. An account relationship type can be set to inactive at any time.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The new account relationship type appears on the Account Relationship Types list.


