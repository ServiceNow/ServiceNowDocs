---
title: Account hierarchy
description: Use the account hierarchy feature to create and view a parent-child relationship between accounts.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Create customer relationships, Configure accounts and contacts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Account hierarchy

Use the account hierarchy feature to create and view a parent-child relationship between accounts.

An account hierarchy The account hierarchy uses a tree structure to show the parent, child, and sibling accounts. This structure represents the legal entity structure of the accounts and their relationships.

Agents can do the following from the account hierarchy:

-   Expand and collapse the tree structure.
-   Switch between the parent view and the full view.
-   Select an account to open the related Account form.

## Account hierarchy in the workspace view

To view the account hierarchy in CSM Configurable Workspace, navigate to an account record and select the Open Hierarchy \(![](../image/account-hierarchy-workspace-icon.png)\) icon on the **Account** field.

![Parent view of the account hierarchy structure with information about the current account and options to update and delete the account details.](../image/csm-account-hierarchy-workspace.png "Account hierarchy (workspace)")

Two different views of the account hierarchy are available.

-   Enable **Parent view** to see the current account, the parent account \(if applicable\), and any child or sibling accounts.
-   Disable **Parent view** to see only the parent account.

## Account hierarchy in the Core UI view

The account hierarchy is available in the Account Hierarchy section on the Account form.

![Parent view of the account hierarchy structure with information about the current account and options to update and delete the account details.](../image/csm-account-hierarchy-platform.png "Account hierarchy (Core UI)")

Two different views of the account hierarchy in the Core UI are available. In both views, the current account is highlighted in the account structure.

-   **Parent view:** Displays the current account, the parent account \(if applicable\), and any child or sibling accounts.
-   **Full view:** Displays the entire structure of the organization from the root account.

## Configuring the account hierarchy

Users with the system administrator role can define the hierarchy between accounts on the Account form by using the **Parent Account** field.

-   From the Account form for the child account, select the parent in the **Parent Account** field.
-   For top-level accounts, do not fill in the **Parent Account** field.

