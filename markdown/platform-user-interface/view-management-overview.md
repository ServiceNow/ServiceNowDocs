---
title: View management
description: A view defines the elements that appear when a user opens a form or a list, and you can switch the view from the default for lists and forms.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# View management

A view defines the elements that appear when a user opens a form or a list, and you can switch the view from the default for lists and forms.

When the system displays a form or list it usually displays only a subset of the fields belonging to the underlying table. For example, this is the Incident form in the **Self-Service View**:

![](../image/SelfServiceView.png "Self service view")

This is the Incident form in the **Metrics View**:

![](../image/MetricsView.png "Metrics view")

Administrators and users with the personalize role have permission to perform the key tasks related to views:

-   create views for any list and form
-   determine which view is visible by default
-   delete views they have created
-   create and modify view rules determining which views are available depending on the values of the fields of the underlying table
-   create rules that determine which views pertain to specific user roles

Users with the admin or view\_changer roles can change views.

## Views included with the base system

Several views are included with the base system, including the Default view and Advanced view.

**Warning:** Do not delete any of the base system views.

## Switching views

To switch between list views, click the list context menu at the top left corner of the list, and then select **Views** &gt; **\[Desired View\]**.

![](../image/ListViewDropdown.png "List view list")

To switch between the list view in list v3, click the context menu, then select **Change view** &gt; **\[Desired View\]**.

To switch between form views, click the context menu at the left side of the form header, and then select **Views** &gt; **\[Desired View\]**:

![](../image/FormViewDropdown.png "Form view list")

Switching views submits the form, which saves all changes and triggers any **onSubmit** client scripts that apply. You cannot switch form views on a new form that has not been saved yet.

When a user switches views, the selected view is saved as a user preference so the user sees the same view by default when the form opens. When a user has a view saved as a user preference and then opens a URL to a record that specifies another view, the form displays in the view saved in the user preference, not the URL. For example, if a user selects the Mobile view on an Incident record and then tries to open the following link, which specifies the visual task board view, the form still opens in the Mobile view: `https://{instance}/nav_to.do?uri=incident.do?sys_id={sys_ID}sysparm_view=vtb`

The sysparm\_view parameter specifies the view to be used for a list or a form, and can be overwritten by a user’s stored preference for a view. You can override this behavior by setting the **sysparm\_view\_forced** parameter to **true**.

-   **[Create and delete views](../task/create-delete-view.md)**  
Administrators can create views and delete any views they have created. You can create or delete views from either the list view or the form view.
-   **[Create a view rule](../task/t_CreateAViewRule.md)**  
When a user switches views, the selected view is saved as a user preference so the user sees the same view by default when the form opens. With a view rule, you can override this functionality to force a specified view to be used.
-   **[Control when the system displays a view](../task/control-views.md#)**  
Administrators can create rules that determine the conditions for when the system should display a form or list in a specified view. Administrators can also restrict views by user role.
-   **[Navigation handler](c_NavigationHandler.md)**  
A navigation handler is a scripted view rule and runs each time data from the specified table is requested in the form view.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

