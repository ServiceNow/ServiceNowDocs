---
title: Create an account relationship record
description: Create an account relationship record by selecting the account relationship type and then selecting the accounts involved in the relationship.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Bi-directional account relationships, Create customer relationships, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Create an account relationship record

Create an account relationship record by selecting the account relationship type and then selecting the accounts involved in the relationship.

## Before you begin

Role required: sn\_customerservice\_manager or admin

## About this task

The system administrator can create a relationship record for an account from the **Account Relationships** related list on the Account Relationship Type form.

The customer service manager and the system administrator can create a relationship record for an account from the **Account Relationships** related list on the account or partner record.

Deleting a relationship record for an account also deletes the reverse relationship record.

**Note:** Deleting a relationship record does not have any impact on customer service cases that refer to the relationship record.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Accounts** or **Partners**.

2.  Select an account.

3.  From the **Account Relationships** related list, click **New**.

4.  Fill in the fields on the Account Relationship form.

    |Field|Definition|
    |-----|----------|
    |Account From|The source account for this relationship. If you are creating the relationship from an account or partner record, this field is automatically filled in; otherwise, make a selection from the Accounts list.|
    |Relationship Type|Select the account relationship type for this record. If you are creating the record from an Account Relationship Type form, this field is automatically filled in. Otherwise, make a selection from the Account Relationship Types list, which shows all active account relationship types.|
    |Account To|The target account for this relationship.|

5.  Click **Submit**.

    Once a relationship record has been created, it appears in two places:

    -   The relationship appears in the **Account Relationships** related list on the source account record.
    -   The reverse relationship appears in the **Account Relationships** related list on the target account record.

