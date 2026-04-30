---
title: Column Level Encryption
description: Column Level Encryption permits and denies access to encrypted data based on user role. Column Level Encryption includes basic key management using encryption modules.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-02-01"
reading_time_minutes: 3
breadcrumb: [Encryption]
---

# Column Level Encryption

Column Level Encryption permits and denies access to encrypted data based on user role. Column Level Encryption includes basic key management using encryption modules.

**Important:**

Starting with the Zurich release, Column Level Encryption \(CLE\) and Column Level Encryption Enterprise \(CLEE\) are being prepared for future deprecation. They will be hidden and no longer activated on new instances but will continue to be supported. [Field Encryption](field-encryption.md) and [Field Encryption Enterprise](../../now-platform-encryption/concept/now-platform-encryption.md) provide the latest experience for this functionality.

For details, see the Deprecation Process \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] article in the Now Support knowledge base.

With Column Level Encryption, you can encrypt specific fields within your tables, as opposed to encrypting the entire table or database. Use this method to help ensure that your sensitive data remains protected without the need to encrypt and entire table. The ability to encrypt only the portions of your tables that require it helps to reduce the time spent encrypting and decrypting data.

Column Level Encryption grants access to encrypted data based on a user's role. Because of this approach, users must be associated with a role to view data encrypted by Column Level Encryption. Users can be associated with a role directly, or they can be assigned to a group that is associated with a role. This role-based approach simplifies the process of making sure that your data is visible only to users who need it.



In this example, you can see four users attempting to access data stored in two fields on a form. These fields are encrypted by an encryption context, which is only accessible to users who are associated with a specific role \(Role 1\).

-   User 1 is a member of Role 1, which provides access to encryption module 1. User 1 can see the contents of Field A and Field B.
-   User 2 and User 3 are members of Group 1. Group 1 is a member of Role 1, which enables everyone in Group 1 access to encryption module 1 and enables User 2 and User 3 to see the contents of Field A and Field B.
-   User 4 isn't a member of any group or role and has no access to encryption module 1. User 4 does note access to Field A or Field B. User 4 also doesn’t see these fields on a form. In a list view, these fields are visible, but the values are be empty.

## Get started

<table id="table_ryk_zzq_ryb" class="nav-card"><tbody><tr><td>

[Explore![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn the benefits of the Standard and Enterprise editions of Field Encryption.](exploring-column-level-encryption.md)

</td><td>

[Configure![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Learn how to activate and configure Column Level Encryption Enterprise, and manage migration from Encryption Support](configuring-column-level-encryption.md)

</td><td>

[Use![](../../../reuse/icons/brand-icons/bus-integration-and-apis.svg)Use Field Encryption to manage access to encrypted data on your instances](using-column-level-encryption.md)

</td></tr></tbody>
</table>## Troubleshoot and get help

-   [ServiceNow community developer forum](https://www.servicenow.com/community/developer-forum/bd-p/developer-forum)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

-   **[Exploring Column Level Encryption](exploring-column-level-encryption.md)**  
Learn more about Column Level Encryption.
-   **[Configuring Column Level Encryption](configuring-column-level-encryption-2.md)**  
Learn how to activate and configure Column Level Encryption and manage migration from Encryption Support.
-   **[Using Column Level Encryption](using-column-level-encryption-2.md)**  
Use Column Level Encryption to manage access to encrypted data on your instances.

**Parent Topic:**[Encryption](../../security/concept/encryption-landing.md)

