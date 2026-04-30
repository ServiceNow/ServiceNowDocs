---
title: Navigation stack
description: The navigation stack is the portion of the ServiceNow suite of applications that determines where a user is redirected after the update of a record.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Navigation stack

The navigation stack is the portion of the ServiceNow suite of applications that determines where a user is redirected after the update of a record.

An administrator can cause page references to be manually inserted into the navigation stack when a link in the **Navigation Page** is clicked. This is done by modifying a module definition to include an argument of sysparm\_stack with a string value equal to the URL reference to the page to be inserted into the stack. The administrator can also override the redirection determined by the stack by creating a business rule or editing an existing one to include `gs.setRedirect("http://redirect_page.com")`.

## Operating parameters of the navigation stack

The navigation stack can be thought of a user's navigation history in the instance. It is updated every time a user views a new page. The navigation stack is referenced when users press the page back button. It is also referenced when a user submits or updates a record, at which point users are redirected to their last page in the navigation stack.

![Actions that invoke the navigation stack](../image/BackAndUpdate.png "Back and Submit or Update")

## Inserting pages to the navigation stack

The administrator can insert page references manually into the navigation stack when a link in the navigation page is clicked. The module definition is modified to include an argument of sysparm\_stack with a string value equal to the [URL reference](../../../use/navigation/task/navigate-using-url.md) to the page to insert into the stack. The following image shows the system definition for the **Incident** &gt; **Create New** module. By passing an argument of "sysparm\_stack=incident\_list.do", the list view of incidents \(incident\_list.do\) is added to the stack. After submitting an incident, the user is directed to this page.

![Argument in a module link](../image/SysparmStackEx.png "Sysparm stack example")

## Overriding the redirection behaviors of the navigation stack with onEvent business rules

The redirection behaviors that occur as a result of navigation stack behaviors can be overridden using onEvent business rules. This override is performed by using the function **gs.setRedirect**. Doing so overrides the redirection as determined by the navigation stack, when the specified event occurs. The function **gs.setRedirect** takes a string argument that is a URL for the page that the user is redirected to. This URL can be external, for example: **gs.setRedirect\('http://www.google.com'\)**.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

