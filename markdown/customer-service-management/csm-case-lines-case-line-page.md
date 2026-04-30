---
title: Case line item page
description: The case line item page displays information about a case line item associated with a case.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Case line record pages, Case Lines and Workflows, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Case line item page

The case line item page displays information about a case line item associated with a case.

The case line item page shows the details of a case line item, including customer and product information, the requested change to the ordered quantity, the shipping location, and estimated dates.

## Case line item page tabs

The case line item page includes the following tabs:

-   Details: Displays the case line item details, including order and account information, ordered and requested quantities, and shipping information.
-   Case Line Characteristics: Displays the specific characteristics of the case line item.
-   Case Line Tasks: Displays the tasks created for the case line item.
-   Case Line Entitlements: Displays the entitlements associated with the case line item. The visibility of the Entitlements tab is controlled by the [sn\_customerservice.advanced\_entitlements](../reference/csm-case-mgmt-case-lines-install-comp.md#section_owr_n1r_hfc) system property.

    The Entitlements tab displays the entitlements associated with the case line item. From this tab, users can associate one or more entitlements to a case line item. The system displays the available entitlements for a case line item based on the customer's service contracts and accounts.


## Contextual side panel

The contextual side panel on the case line item page includes different tools that agents can use to research and resolve customer issues. The contextual side panel on the case line item page includes the following tabs.

-   Record Information
-   Attachments
-   Templates

## Case line item page UI actions

The case line page includes the following actions.

<table id="table_hjj_kry_fdc"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create case line task

</td><td>

Appears in the case line item action bar.To create a case line task:

1.  Select **Create case line task** to display a Create New Case Line Task record in a separate tab.
2.  Enter information in this record and select **Save** to create the case line task record.

Case line tasks are added to the Tasks tab on the case line record.

</td></tr><tr><td>

Save

</td><td>

Appears in the case line item action bar. Selecting this action saves changes to the case line item record.

</td></tr><tr><td>

Delete

</td><td>

Appears in the More actions menu. Selecting this action displays a confirmation pop-up window. Select **OK** to complete the delete action.-   Agent role: can delete case line item records in Draft state.
-   Admin role: can delete case line item records in any state.

</td></tr></tbody>
</table>