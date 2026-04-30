---
title: Diagnose user access to a knowledge base
description: Identify which users have access to a knowledge base and what enables that access.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [User criteria diagnostics for Knowledge Management, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Diagnose user access to a knowledge base

Identify which users have access to a knowledge base and what enables that access.

## Before you begin

Role required: knowledge\_manager, knowledge\_admin, or admin

## Procedure

1.  Access the **User Criteria Diagnostics** landing page using one of these options:

<table id="table_sht_xcv_bdb"><thead><tr><th>

To access

</th><th>

Navigate to

</th></tr></thead><tbody><tr><td>

Using the application navigator

</td><td>

**Knowledge** &gt; **Administration** &gt; **User Criteria Diagnostics**

</td></tr><tr><td>

From a knowledge base

</td><td>

1.  **Knowledge** &gt; **Administration** &gt; **Knowledge Bases**.
2.  Select the knowledge base to diagnose user access.
3.  In the **Related Links** section, click **Run User Criteria Diagnostics**.
 The **User Criteria Diagnostics** landing page appears with the **Select knowledge base** field pre-populated.

</td></tr></tbody>
</table>2.  To diagnose user access:

    1.  In the **Select user** field, select a user.

    2.  From the **Select record type** choice list, select **Knowledge base**.

    3.  In the **Select knowledge base** field, select a knowledge base.

        Every time you select a different user, record type, or knowledge base, the page refreshes and displays data for the selected user.

    4.  Click **Diagnose**.

        The page displays these details:

        -   Whether the user has access to the knowledge base based on their domain. Only system administrators can view domain information and change the domain to give access to a user.
        -   Which user criteria provides read or read and contribute access for this user to the knowledge base and what type of [user criteria definition](t_SelectUserCriteria.md) enables this access.
        -   Whether a role that the user has \(knowledge\_manager, knowledge\_admin, or owner of the knowledge base\) enables this access.
        -   For a user with no access to this knowledge base, which user criteria may be modified to grant the access.

## Example

The following image shows an example of a diagnosis where the user Alene Reback does not have access to the IT knowledge base.

Alena can get access to the knowledge base if:

-   Alena is added to one of the existing user criteria defined in the knowledge base.
-   Alena is added to a new user criteria that is defined and added to the knowledge base.

Click the IT knowledge base link and provide the access by adding Alena to a user criteria for this knowledge base.

![User criteria diagnosis for a knowledge base.](../image/user-crit-diag-kb.png)

**Parent Topic:**[User criteria diagnostics for Knowledge Management](../concept/diagnose-knowledge-user-criteria.md)

