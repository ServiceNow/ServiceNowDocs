---
title: Use the client GlideList API in the Workspace Experience UI
description: Add a custom button to the Agent Workspace Lists page that returns list information in the current view. Define the information to return by adding client GlideList API methods to an action assignment.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Developer guides, API implementation and reference]
---

# Use the client GlideList API in the Workspace Experience UI

Add a custom button to the Agent Workspace Lists page that returns list information in the current view. Define the information to return by adding client GlideList API methods to an action assignment.

## Before you begin

Role required: admin

[GlideList](../../../app-store/dev_portal/API_reference/GlideListClientNowEx/concept/GlideListClientAPINEx.md#) API methods are provided in the Action Assignments \[sys\_declarative\_action\_assignment\] **List Action** view. You can add GlideList functionality to a custom button in the Workspace Experience UI. You can use the button to apply a GlideList method to the current view. Use the GlideList methods to manage table lists by getting list view details, setting filters, sorting by column, and more.

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Actions &amp; Components** &gt; **List Actions**.

    If you are using [getFixedQuery\(\)](../../../app-store/dev_portal/API_reference/GlideListClientNowEx/concept/GlideListClientAPINEx.md#), navigate to **Related List Actions** instead of **List Actions**.

2.  Create a new action assignment by selecting **New**.

3.  In the **Action label** field, type a button label.

4.  Type a name into the **Action** name field.

    Providing text in this field ensures that you can add multiple buttons to the view.

5.  From the **Implemented as** menu, select **Client Script**.

6.  Right-click in the form header and select **Save**.

7.  Select **Advanced View**.

8.  Select the **Client Script** tab and add one or more method calls into the `onClick{}` method definition.

    This method defines what actions to take when the button is selected. For a list of available methods, see [GlideList \(Now Experience\)](../../../app-store/dev_portal/API_reference/GlideListClientNowEx/concept/GlideListClientAPINEx.md#).

    ![GlideList method calls in the Client Script field.](../image/add-api-glidelist-workspace.png)

9.  Select **Update**.

    You can test your button in a Workspace Experience table list view.

    **Note:** If the button uses the [getFixedQuery\(\)](../../../app-store/dev_portal/API_reference/GlideListClientNowEx/concept/GlideListClientAPINEx.md#) method, select the tab on a record in a Workspace Experience list to test your button.

    The following table illustrates successful button implementation in the Agent Workspace **Incidents \(All\)** table. The button implements the GlideList addFilter\(\) method to display only active records.

<table id="table_bzt_dtx_msb"><thead><tr><th>

List before clicking

</th><th>

List after clicking

</th></tr></thead><tbody><tr><td>

Before selecting the button, an assortment of active and inactive \(closed\) records display in the view.![List displayed before the user selects the button to view active records.](../image/add-api-glidelist-listClosed.png)

</td><td>

Selecting the button filters the view to display only active records.![List displayed after the user selects the button displaying only active records.](../image/add-api-glidelist-listOpenOnly.png)

</td></tr></tbody>
</table>
