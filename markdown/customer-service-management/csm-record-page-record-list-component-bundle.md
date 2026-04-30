---
title: Record List component bundle
description: The Record List component bundle is a list component bundle that uses a dedicated controller to configure list actions such as sorting, filtering, and grouping.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Front-line case page, CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Record List component bundle

The Record List component bundle is a list component bundle that uses a dedicated controller to configure list actions such as sorting, filtering, and grouping.

The Record List component bundle includes a record list header with declarative actions as well as pagination control for navigating list pages.

Starting with the Zurich release, CSM Configurable Workspace record pages use the Record List component bundle. This list component bundle is the default experience for both new \(zboot\) and upgrade customers.

For more information, see the following topics:

-   [Record List Overview](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/record%20list/overview) in the ServiceNow Developer documentation
-   [Record List](https://internal.horizon.servicenow.com/workspace/components/record-list?release=zurich) on the Horizon design system website

## Upgrade information

The default declarative actions included with CSM Configurable Workspace record pages work with the Record List component bundle.

Customer declarative actions that open a modal on the list page require some configuration to work with the Record List component. See the example below for details.

To continue using the previous list bundle component in place of the Record List component bundle:

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.
2.  Select the UX Screen \[sys\_ux\_screen\] table.
3.  Search for and select **List bundle default** in the Screen Name column.
4.  Set the **Active** field to false and select **Update**.

## Example

This example uses the Customer Service Case Types application, which includes multiple page variants under a single route. This example details the steps needed to configure a customer declarative action for **Create Case** that opens a modal on the list page:

-   Create the mapping for a declarative action to open a modal.
-   Make the modal available on the list bundle component.

**Step 1**: Create the mapping for a declarative action to open a modal.

1.  Navigate to the UX Add-on Event Mapping \[sys\_ux\_addon\_event\_mapping\] list.
2.  Search for the **Create Case** event mapping name by filtering the Target Event column: LIST\#OPEN\_MODAL.
3.  Select **Create Case** for the event that creates a case on list view.
4.  Right-click the form header and select **Insert and Stay** to create a new event mapping record. This creates a new record to the existing source declarative action.
5.  Fill in the following fields on the event mapping form:

    -   Name = &lt;Enter a unique name&gt;
    -   Source Component = Record List Header
    -   Controller = List Controller
    -   Target Event = Open modal
    For more information, see [Create a UX add-on event mapping](https://www.servicenow.com/docs/access?context=create-a-ux-add-on-event-mapping&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

6.  Select **Submit**.

**Step 2**: Make the modal available on the list bundle component.

To make the modal available, add it to the List Page Modals page collection.

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Open the CSM/FSM Configurable Workspace experience.
3.  Select **List \(List bundle default\)** in the experience header.
4.  In the content tree on the left side, select **List Viewport Modal**.
5.  In the Configure tab on the right side, select the icon in the **Page collections** field to display the List page modals page collection.
6.  Create a page under the page collection. For example, create a page called create\_case.

    1.  Select the **+** icon next to Pages and variants and then select **Create a new page**.
    2.  Add a name in the **Name** field and select **Continue**. For example, add create\_case as the name.
    3.  Select **Build responsive** and then select **Create**. The create\_case page is added to the list of pages and variants for the page collection
    For more information, see [Page collections](https://www.servicenow.com/docs/access?context=page-collections&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

7.  Go to the app route record and change the screen collection to point to the existing screen collection. For example, the Create Case screen collection.
    1.  Select **Settings** for the create\_case page to open the general page settings.
    2.  In the Actions field, select **Open records** and then select **Page collection**. This displays the List page modals extension point form.
    3.  In the create\_case app route record, add the required **Fields** parameters: table,sysId.
    4.  Set the **Screen Collection** field on the create\_case app route record to **Create Case** and then select **Update**.

