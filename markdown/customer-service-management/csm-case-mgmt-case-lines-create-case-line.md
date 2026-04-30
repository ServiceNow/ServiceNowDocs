---
title: Creating case line items and case line tasks
description: Agents can create case line items for cases and create tasks for case line items.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-09-16"
reading_time_minutes: 2
breadcrumb: [Case lines and workflows, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Creating case line items and case line tasks

Agents can create case line items for cases and create tasks for case line items.

## Creating case lines

To create a case line record:

-   CSM Configurable Workspace: Open a case and select **New** on the [Case Line list action bar](csm-case-mgmt-case-lines-create-case-line.md#section_h41_s1h_5cc) to open a new case line record in the Draft state.
-   Core UI: Open a case and select **New** on the Case Lines related list on the case record to open a new case line record in the Draft state.

The information in the following fields is copied from the parent case:

-   Account
-   Contact
-   Parent case
-   Priority
-   Assignment group
-   Assigned to

If a bundled product is added to a case line item record, the system creates a case line item for each component in the bundle after the agent saves the new case line item record. The case line characteristics are also created for each component.

## Create a case line task

The case line item record includes a **Create case line task** action that agents can use to create tasks for a case line item.

1.  Open a case line item record.
2.  Select **Create case line task** to open a Create new case line task form.

    Some fields on this form are auto populated with details from the Case line record.

3.  Enter additional information as needed.
4.  Select **Save** to create the case line task record.

    Case line tasks appear in the Tasks tab on the case line item record.


## Case Line list action bar

In CSM Configurable Workspace, the Case Line list action bar appears at the top of the Case Line list component on a case record.

Agents can add case lines from existing entities, such as orders or invoices, or create new case lines.

-   **New**: Opens a Create New Case Line record in a separate tab. Fill in the fields and select **Save** to add the case line to the list.
-   **Add**: Displays the Add lines to case modal. Select one or more lines and then select **Add** to add the selected case lines to the list.

After selecting a case line, users can edit the case line details, assign a case line to themselves, or delete a case line.

-   **Edit**: Displays the details for the selected case line in a panel. Make the necessary changes and select **Update** at the bottom of the panel.
-   **Assign to me**: Assigns the selected case line to the current user.
-   **Delete**: Deletes the selected case line. Select **Delete all** in the confirmation pop-up window.

