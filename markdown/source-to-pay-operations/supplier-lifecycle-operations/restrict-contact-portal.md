---
title: Restrict the primary contact role for a contact from the Supplier Collaboration Portal
description: Restrict the primary contact role for a contact to prevent them from accessing all the contacts and tasks in the Supplier Collaboration Portal.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing supplier contacts, Using Supplier Collaboration Portal, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Restrict the primary contact role for a contact from the Supplier Collaboration Portal

Restrict the primary contact role for a contact to prevent them from accessing all the contacts and tasks in the Supplier Collaboration Portal.

## Before you begin

Role required: sn\_slm.contact or sn\_slm.admin

## About this task

The **Restrict access** option is available only to the primary supplier contact and the supplier administrator.

## Procedure

1.  Navigate to the Supplier Collaboration Portal home page by accessing your instance URL and adding a /supplier suffix.

    For example, `https://example.com/supplier`.

2.  In the Contacts widget, select a contact to open the contact's profile page.

3.  Select **Restrict access**.![Selected button for restricting access.](../image/restrict-access-supplier-collaboration-portal.png)

    The Restrict access dialog box is displayed.

4.  In the **Comments** field, enter the reason why you want to restrict the primary contact role for this contact.

5.  Select **Submit**.


## Result

The Primary contact column is set to **false** for this contact on the Vendor Contacts page, and the contact no longer has the primary contact role.

**Parent Topic:**[Managing supplier contacts from the Supplier Collaboration Portal](../concept/managing-contacts-scp.md)

**Related topics**  


[Managing supplier contacts from the Supplier Collaboration Portal](../concept/managing-contacts-scp.md)

[Elevate a contact to the primary contact role from the Supplier Collaboration Portal](elevate-contact-portal.md)

[Reassign tasks to a different contact from the Supplier Collaboration Portal](reassign-task-contact.md)

[Update the supplier contact email from the Supplier Collaboration Portal](update-supp-contact-email.md)

[Remove a supplier contact from the Supplier Collaboration Portal](remove-supplier-contact.md)

