---
title: Create an account relationship record
description: Create an account relationship record by selecting the account relationship type and then selecting the accounts involved in the relationship.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Bi-directional account relationships, Create customer relationships, Configure accounts and contacts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Create an account relationship record

Create an account relationship record by selecting the account relationship type and then selecting the accounts involved in the relationship.

## Before you begin

Role required: One of the following roles:

-   sn\_crm\_foundation\_data\_manager,
-   sn\_crm\_account\_relationship\_data\_manager
-   sn\_customerservice\_manager
-   sn\_crm\_foundation\_admin,
-   admin

## About this task

The administrator can create a relationship record for an account from the **Account Relationships** related list on the Account Relationship Type form.

The customer service manager and the administrator can create a relationship record for an account from the **Account Relationships** related list on the account or partner record.

Deleting a relationship record for an account also deletes the reverse relationship record.

**Note:** Deleting a relationship record doesn’t have any impact on customer service cases that refer to the relationship record.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Accounts** or **Partners**.

2.  Select an account.

3.  From the **Account Relationships** related list, select **New**.

4.  Fill in the fields on the Account Relationship form.

    |Field|Definition|
    |-----|----------|
    |Account From|The source accounts for this relationship. If you’re creating the relationship from an account or partner record, this field is automatically filled in; otherwise, make a selection from the Accounts list.|
    |Relationship Type|Select the account relationship type for this record. If you’re creating the record from an Account Relationship Type form, this field is automatically filled in. Otherwise, make a selection from the Account Relationship Types list, which shows all active account relationship types.|
    |Account To|The target accounts for this relationship.|
    |Order|Specifies the sequence in which records are displayed, organized according to business preferences.|

5.  Select **Submit**.

    Once a relationship record has been created, it appears in two places:

    -   The relationship appears in the **Account Relationships** related list on the source account record.
    -   The reverse relationship appears in the **Account Relationships** related list on the target account record.

