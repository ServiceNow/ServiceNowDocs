---
title: How to separate Docusign account data
description: Restrict access to Docusign data based on a user's role. For example, your company may have one Docusign account used by the HR team and another used by the Legal team. To keep the data separate between these two accounts, you can create a role for each account and add it to the accounts record.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Docusign eSignature Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# How to separate Docusign account data

Restrict access to Docusign data based on a user's role. For example, your company may have one Docusign account used by the HR team and another used by the Legal team. To keep the data separate between these two accounts, you can create a role for each account and add it to the accounts record.

## Before you begin

-   Request Integration Hub subscription
-   Activate Docusign eSignature spoke
-   [Create child aliases for additional Docusign accounts](create-aliases-docusign.md)
-   [Set up Docusign eSignature spoke using JWT grant](setup-docusign-jwt.md#) or [Set up Docusign eSignature spoke using authorization code grant](setup-docusign-authorization-code.md#)
-   Role required: admin.

## Procedure

1.  Create a role for each Docusign account that you want to restrict access to.

    1.  Navigate to **System Security** &gt; **Users and Groups** &gt; **Roles**.

    2.  In the Roles \[sys\_user\_role\] table, select **New**.

    3.  Check that the value of the **Application** field is **Docusign Spoke**.

        If a different scope is listed, change the scope to **Docusign Spoke**.

    4.  In the **Suffix** field, add a name to indicate the account that the role is for, for example, `Legal`.

    5.  Save the record.

    6.  Note the name of the role you just created.

        For example, **sn\_docusign\_spoke.legal**.

2.  Add the role to the associated account in the accounts table.

    1.  Navigate to **Docusign** &gt; **Accounts**.

    2.  Open the account record that you want to restrict access to.

    3.  In the **Role** field, add the associated role.

    4.  Select **Update**.

3.  Grant the role to the desired users.

    1.  Navigate to **System Security** &gt; **Users and Groups** &gt; **Users**.

    2.  Open the record for the user that you want to provide access.

    3.  Add the role that you created to the Roles related list.


## Result

Only users with the designated role have access to Docusign data associated with the account.

