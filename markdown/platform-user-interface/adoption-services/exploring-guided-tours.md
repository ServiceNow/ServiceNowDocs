---
title: Exploring Guided Tours
description: Learn about Guided Tours features that enable you to demonstrate to users how to perform a task.
locale: en-US
release: xanadu
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Guided tours, Adoption services, Configure user experiences]
---

# Exploring Guided Tours

Learn about Guided Tours features that enable you to demonstrate to users how to perform a task.

## Get to know Guided Tours

Guided tours help train and onboard users within the ServiceNow user interface \(UI\). Each tour contains a series of interactive steps that help users complete online tasks within their browser window. Administrators can create tours for ServiceNow applications, service portals, and custom applications. For example, you can create a tour to represent a training model for specific policies and processes, such as creating an incident or reviewing change requests.

Guided tours use a series of steps that may span multiple pages. You can create purely informational steps that users read through and acknowledge, which result in no change to the ServiceNow instance. Alternatively, you can provide users with an interactive experience where they click through and actively work with the application at hand. For example, an “Introduction to Incidents” tour may simply show them the key features of the Incidents table, while a “Create your first incident” tour may actually walk them through creating a real incident, which results in a new record in the Incidents list.

**Important:** Guided Tours are supported in Next Experience pages, such as configurable workspaces or pages configured in UI Builder using the Next Experience UI Framework. To enable Next Experience support, configure the `com.snc.guided_tours.standard_ui.enable` system property and set to **True**. For more information about Guided Tours in Configurable Workspaces see [Guided Tours in Configurable Workspaces](guided-tours-in-configurable-workspaces.md). The following scenarios are still supported with Next Experience enabled.

-   Creating and running new or existing Guided Tours in the Classic Environment \(including lists and forms\).
-   Creating and running new or existing Guided Tours for a Service Portal.
-   Creating new Guided Tours for Unified Navigation menus \(such as the All or Favorites menus\).

See [Next Experience](../../../get-started/servicenow-overview/concept/next-experience-landing-page.md). The Guided Tour Designer is only available in Core UI. The designer is not compatible with UI15. For information about how to activate the Core UI plugin, see [Activate Core UI](../../../administer/navigation-and-ui/task/t_ActivateUI16.md)

Several guided tours are provided in the base system for particular applications, for example, Performance Analytics. As an administrator, you can edit existing tours or create tours. You can also assign one or more roles to a tour to control access.

The guided tours feature uses these two plugins: Guided Tour \(com.glide.guided\_tours\) and Guided Tour Designer \(com.glide.sn\_tourbuilder\).

## Navigating to guided tours

Guided tours run on four types of UI: Standard, Service Portal, Custom and Workspaces. Tours launch differently when accessed based on each tour type as follows.

-   **Standard Forms and Lists UI:**

    Users access a guided tour by navigating to a page that has one. If they have one or more of the roles that the tour is targeted to, they can click the ![Blue Toggle Help sidebar indicates tours are available](../image/gtd-bluehelp-icon.png) icon so the GTD panel opens to show the **Take a Tour** button. If more than one tour is available to a user on a page, the **Select Tour** choice list appears so they can select which tour to launch.

    Tours on **Custom UI pages/applications** can be accessed in the same way. This is only applicable for custom pages which are opened in the navigator. The tours are not visible if the user opens a Custom UI page without the navigator.

-   **Service Portal UI:**

    Users access a guided tour by navigating to a page that has one. When a user accesses a Service Portal page that has a guided tour on it, no GTD panel is present. Instead, the ![Show users how to launch a Service Portal tour](../image/gtd-tours-button.png) menu item appears on the banner indicating a tour is available. If a guided tour is available on a page on the service portal, a color indicator appears to the right of the **Tours** menu. When the user clicks **Tours**, all available tours for the page appear.

    If a page has no Service Portal Header Menu, the Tours menu item is not accessible to the user. In this case, the tour is accessible to users only via auto-launch. See [Configure auto-launch for guided tours](../task/auto-launch-guided-tours.md).

    When you add at least one role to a tour, it limits the audience to those users who have that role. For more Service Portal guided tour information, see [Activate guided tours](../task/activate-guidedtours-service-portal.md).

-   **Workspaces**

    Users access a guided tour by navigating to a page that has one. When a user accesses a Workspace page that has a guided tour on it, they can click the ![Blue Toggle Help sidebar indicates tours are available](../image/gtd-bluehelp-icon.png) icon so the GTD panel opens to show the **Take a Tour** button. If more than one tour is available to a user on a page, the **Select Tour** choice list appears so they can select which tour to launch.


## Guided Tour Designer support

**Note:** The same system property as Standard UI is used to enable and disable guided tours.

The Guided Tour Designer \(GTD\) supports most of the standard platform UI areas and their content, such as lists, forms, and the elements they reference. It also supports Service Portal pages, including those that have custom UI elements.

The GTD does not currently support the following areas.

Standard Forms and Lists UI:

-   Flow Designer
-   Agent Workspace
-   Pop-up windows
-   Connect Chat and Embedded Help on the GTD sliding panel
-   Select2 elements
-   SVG elements
-   Custom Tags
-   Standard UI pages that have custom UI elements, such as Contextual search.

Service Portal:

-   Service Portal pages that contain IFRAMES
-   The Service Portal Branding Editor, which also contains IFRAMES
-   Select2 elements
-   SVG elements
-   Custom Tags
-   Seismic components \(shadow dom\). For example: sn-search-combobox - AI search box, sn-search-results-container - AI search results.
-   Tours when accessed in the Next Experience UI.

Workspaces

-   Only the following app shell experiences are supported:
    -   Breadcrumb App shell
    -   ACE Unified Nav App shell
    -   Workspace App shell
    -   Custom App shell
-   Experiences with an empty app shell are not supported.
-   Tours that start in a custom app shell and go to the Polaris app shell are not supported.
-   Not recommended to create tours on workspaces in UI16
-   Variants
-   Callouts inside iframes in a workspace
-   Guided tours that start in a standard UI or workspace and go to a service portal
-   Guided tours are only supported within a page, if a link opens in a new tab the tour does not continue

    **Note:** Admins must add the right action for the callout on elements that can open in a new tab.

-   Guided tours are not supported in mobile view
-   Callouts on elements inside visualisation components or par widgets

Technical limitations

-   Elements that are loaded in DOM by scrolling the page effect guided tours. The admin must inform the user to scroll further when the form is present.
-   If there is no click action on the elements that are selectable while creating the tour, place the callout on the parent element.

## Guided Tours workflow

Guided tours are composed of the following components that function as building blocks for the tours that you create.

|Component|Description|
|:--------|:----------|
|Introduction|Shows an introductory message to your users.|
|Step|A discrete component of a guided tour that implies an order. A step can provide a definition, an instruction, or both.|
|Callout|Shows the definition and instruction about the current step in the tour. The callout includes the instruction to proceed to the next step. It points to the element that the instruction describes.|
|Element|The objects that the tour points to, such as a record in the database, or a widget on a page. Elements require formatting so that the tour can link to them.|
|Trigger|Moves the tour to the next step. Triggers include pressing the Enter key, clicking or right-clicking a UI element, or clicking a **Next** button in the callout.|
|Conclusion|Shows a closing message to your users at the end of the guided tour.|

Guided tours require careful planning before entering the tour into the instance. You can create an outline and include any assumptions to guide you when you create the guided tour. List each step, callout, and trigger.

<table id="table_oml_pcz_pyb"><thead><tr><th>

Step

</th><th>

Callout

</th><th>

Trigger

</th></tr></thead><tbody><tr><td colspan="3">

This tour assumes that the user has navigated to **User Administration** &gt; **Delegates**. The UI page is `sys_user_delegate_list.do`.

</td></tr><tr><td>

Open the Delegate form to enter a new record.

</td><td>

-   Points to the **New** button in the Delegates list view.
-   Text: Click **New** to set up a delegate who receives your notifications while you are on vacation.

</td><td>

Click the element: **New** button

</td></tr><tr><td>

Describe the **User** field.

</td><td>

-   Points to the **User** field.
-   Text: Your name defaults as the user who wants to delegate to another user. If you are setting up a delegate for someone else, you can select a different user.

</td><td>

**Next** button

</td></tr><tr><td>

Select the delegate

</td><td>

-   Points to the **Delegate** field.
-   Text: You specify who you want to delegate to. Type the user's name, and select it when it appears.

</td><td>

**Next** button

</td></tr><tr><td>

Set the start date

</td><td>

-   Points to the **Starts** field.
-   Text: Enter the date and time to start forwarding notifications. Click away from the field to proceed.

</td><td>

Change the Value: **Starts** field

</td></tr><tr><td>

Set the end date

</td><td>

-   Points to the **Ends** field.
-   Text: Select the date and time to stop forwarding notifications. Click away from the field to proceed.

</td><td>

Change the Value: **Ends** field

</td></tr><tr><td>

Describe the delegate options

</td><td>

-   Points up from below the **Meeting invitations** field.
-   Text: If you do not want these notifications forwarded to your delegate, you can clear any of these fields.

</td><td>

**Next** button

</td></tr><tr><td>

Submit the delegate record

</td><td>

-   Points to the **Submit** button
-   Text: Click **Submit** to add the delegate.

</td><td>

Click the element: **Submit** button

</td></tr></tbody>
</table>