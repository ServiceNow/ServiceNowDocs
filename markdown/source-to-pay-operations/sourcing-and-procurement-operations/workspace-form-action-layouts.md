---
title: Form action layouts for workspace record forms
description: The actions that appear on a record form in the Source-to-Pay Workspace are controlled by a form action layout for the table. An action that is not part of the layout does not appear.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/sourcing-and-procurement-operations/workspace-form-action-layouts.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-10-15"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay Workspace, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Form action layouts for workspace record forms

The actions that appear on a record form in the Source-to-Pay Workspace are controlled by a form action layout for the table. An action that is not part of the layout does not appear.

Three kinds of records work together to place an action on a workspace record form.

-   **Form action:** Points to the UI action that runs when a user selects the action, and to the table that the action applies to.
-   **Form action layout:** Defines the actions that appear on the form of a table, and is linked to an action configuration. When the layout is set to use layout items only, the form shows only the actions that are added to the layout.
-   **Form action layout item:** Adds a form action to a layout. The layout item sets the type, color, and variant of the action, and its order in the layout.

For example, the Submit For Review action for contracts is defined as a form action for the `ast_contract` table. It is added to the Contract action layout for PSM, which uses layout items only.

**Note:** If a UI action does not appear on a workspace record form, check that a form action exists for the UI action, and that the form action is added as an item to the form action layout for the table.

**Parent Topic:**[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/sourcing-and-procurement-operations/procurement-specialist-workspace.md)

