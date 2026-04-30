---
title: Account hierarchy
description: Use the account hierarchy feature to create a parent-child relationship between accounts.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-06"
reading_time_minutes: 1
breadcrumb: [Create customer relationships, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Account hierarchy

Use the account hierarchy feature to create a parent-child relationship between accounts.

An account hierarchy represents the legal entity structure of the accounts and their relationships. It also represents an account's customers, assets, and service entitlements.

Customer administrators can do the following for all of the accounts in the hierarchy:

-   View and create cases.
-   View assets and users.
-   View and manage contacts.

The system administrator defines the hierarchy between accounts on the Account form. From the Account form for the child account, select the parent in the **Parent Account** field. If this field is not filled in, the account is a top-level account.

After the account hierarchy has been defined, it is displayed on the Account form for the parent account. If a parent account is updated or deleted, the hierarchy for any child accounts is also updated.

## View the account hierarchy

The account hierarchy uses a tree structure to show the parent, child, and sibling accounts. Two different views of the account hierarchy are available. In both views, the current account is highlighted in the account structure.

-   The parent view displays the current account, the parent account \(if applicable\), and any child or sibling accounts.
-   The full view displays the entire structure of the organization from the root account.

Customer service agents can:

-   Expand and collapse the tree structure.
-   Switch between the parent view and the full view.
-   Click an account to open the related Account form.

## Account hierarchy in CSM Agent Workspace

From the Account form, customer service agents can click the open hierarchy icon \(![Open hierarchy icon](../image/workspace-account-hierarchy-icon.jpg)\) in the **Name** field to see the parent-child account relationships in the Account Hierarchy pop-up window. The account hierarchy is available for accounts that have a parent or child account.

![Window displaying the parent-child relationship for an account. For the text description, refer to the text that follows in the Account Hierarchy section.](../image/csm-config-workspace-account-hierarchy.png "CSM Workspace Account Hierarchy pop-up window")

## Account hierarchy in the platform interface

Customer service agents can view account information in the Account Hierarchy section on the Account form.

![Parent view of the account hierarchy structure with information about the current account and options to update and delete the account details.](../image/csm-account-hierarchy-platform.jpg "Account hierarchy (platform interface)")

