---
title: Contact form
description: Use the Contact form to create the contacts manually and then synchronize the contacts with Everbridge.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create contacts for emergency notifications, Setup for Everbridge notifications, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Contact form

Use the Contact form to create the contacts manually and then synchronize the contacts with Everbridge.

## Contact form

<table id="table_u1t_44f_ppb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Source of the contacts. -   If you created the contacts manually from the users' list, then the source is **Manual**.
-   If you had used the sync rule to create the contacts, then the source is **Sync rule**.

</td></tr><tr><td>

Last sync on

</td><td>

Date on which the contact was last synchronized with Everbridge.

</td></tr><tr><td>

Contact ID

</td><td>

Unique ID of the contact.

</td></tr><tr><td>

Sync status

</td><td>

Sync status when the contact is created. Defaults to **New** when the contact is created. The status can also be:-   **Success**: When the contact is successfully synced with Everbridge
-   **Error**: If there is an error in syncing
-   **Updated**: If the contact or the delivery details were modified

</td></tr><tr><td>

User

</td><td>

User reference from the Users table \[sys\_user\].

</td></tr><tr><td>

External contact ID

</td><td>

Contact ID in Everbridge.

</td></tr><tr><td>

Sync error

</td><td>

Error in syncing the contact with Everbridge.

</td></tr></tbody>
</table>**Parent Topic:**[Create contacts for emergency notifications](../task/create-contacts-emergency-noti-uib-ws.md)

