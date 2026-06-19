---
title: Client GlideList API in the Workspace Experience UI Developer Guide
description: Add a custom button to the Agent Workspace Lists page that returns list information in the current view. Define the information to return by adding client GlideList API methods to an action assignment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/add-api-glide.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Developer guides, API implementation and reference]
---

# Client GlideList API in the Workspace Experience UI Developer Guide

Add a custom button to the Agent Workspace Lists page that returns list information in the current view. Define the information to return by adding client GlideList API methods to an action assignment.

## Before you begin

Role required: admin

[GlideList](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/GlideListClientAPINEx.md) API methods are provided in the Action Assignments \[sys\_declarative\_action\_assignment\] **List Action** view. You can add GlideList functionality to a custom button in the Workspace Experience UI. You can use the button to apply a GlideList method to the current view. Use the GlideList methods to manage table lists by getting list view details, setting filters, sorting by column, and more.

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Actions &amp; Components** &gt; **List Actions**.

    If you are using [getFixedQuery\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/GlideListClientAPINEx.md), navigate to **Related List Actions** instead of **List Actions**.

2.  Create a new action assignment by selecting **New**.

3.  In the **Action label** field, type a button label.

4.  Type a name into the **Action** name field.

    Providing text in this field ensures that you can add multiple buttons to the view.

5.  From the **Implemented as** menu, select **Client Script**.

6.  Right-click in the form header and select **Save**.

7.  In the **Client Script** editor, add one or more method calls into the `onClick{}` method definition.

    This method defines what actions to take when the button is selected. For a list of available methods, see [GlideList \(Now Experience\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/GlideListClientAPINEx.md).

    \[Omitted image "add-api-glidelist-workspace.png"\] Alt text: GlideList method calls in the Client Script editor.

8.  Select **Update**.

    You can test your button in a Workspace Experience table list view.

    **Note:** If the button uses the [getFixedQuery\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/GlideListClientAPINEx.md) method, select the tab on a record in a Workspace Experience list to test your button.

    The following table illustrates successful button implementation in the Agent Workspace **Incidents \(All\)** table. The button implements the GlideList addFilter\(\) method to display only active records.

<table id="table_bzt_dtx_msb"><thead><tr><th>

List before clicking

</th><th>

List after clicking

</th></tr></thead><tbody><tr><td>

Before selecting the button, an assortment of active and inactive \(closed\) records display in the view.\[Omitted image "add-api-glidelist-listClosed.png"\] Alt text: List displayed before the user selects the button to view active records.

</td><td>

Selecting the button filters the view to display only active records.\[Omitted image "add-api-glidelist-listOpenOnly.png"\] Alt text: List displayed after the user selects the button displaying only active records.

</td></tr></tbody>
</table>
