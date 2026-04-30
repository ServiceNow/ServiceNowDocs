---
title: Navigation action cancellation
description: The Request Manager allows users to cancel any navigation action they select from the application navigator by clicking another application navigator link. System properties work with settings for the table to allow navigation action cancellation.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Navigation action cancellation

The Request Manager allows users to cancel any navigation action they select from the application navigator by clicking another application navigator link. System properties work with settings for the table to allow navigation action cancellation.

This allows users to cancel slow loading transactions without having to wait for the previous transaction to complete.

One of the following conditions must be true for the Request Manager to cancel a transaction.

-   Both the original transaction and new transaction are cancelable \(both transactions have the setting **sysparm\_cancelable=true**\).
-   The original transaction is a member of the always cancelable allow list \(the module is listed in the **glide.request\_manager.always\_cancel** system property\) and the new transaction is cancelable \(has the setting **sysparm\_cancelable=true**\).
-   Both the original and new transaction produce an auto-completer query in a reference field.

## Cancellation workflow

The Request Manager uses the following workflow to determine whether to cancel a transaction.

![](../image/Cancelation_workflow.png "Cancel navigation actions")

<table id="table_fn3_kkq_n4"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.request\_manager.cancel\_other\_transaction**

</td><td>

Enables or disables automatic cancellation behaviors. When true, users can cancel one navigation action with another navigation action.**Type:** true \| false

 **Default value:** true

 **Location:** sys\_properties table

</td></tr><tr><td>

**glide.request\_manager.always\_cancel**

</td><td>

A comma-separated list of URIs that users can always cancel by clicking another navigation action. Typically items on this list are modules that provide read-only data such as dashboards, reports, or knowledge articles. **Type:** string

 **Default value:** home,sys\_report\_template

 **Location:** sys\_properties table

</td></tr><tr><td>

**glide.request\_manager.cancel\_reference\_completer**

</td><td>

Cancels a user query in a reference field when the user enters more information. For example, if the user starts an AJAX search in the Problem number field by entering **PRB** and then enters **PRB000**, the second query cancels the first query.**Type:** true \| false

 **Default value:** true

 **Location:** sys\_properties table

</td></tr></tbody>
</table>## Use cases

There are three use cases where administrators can control user cancellation actions.

1.  A user clicks a module, such as the homepage \(`home.do`\), and while waiting for the module to load decides to navigate to another module, such as the list of open incidents \(`incident_list.do`\). The system property **glide.request\_manager.cancel\_other\_transaction** controls this use case.
2.  A user clicks a module that displays read-only data, such as a report \(`sys_report_template.do?sysparm=sysid`\), and while waiting for the module to load decides to navigate to another module, such as the list of open incidents \(`incident_list.do`\). The system properties **glide.request\_manager.cancel\_other\_transaction** and **glide.request\_manager.always\_cancel** control this use case.
3.  A user starts typing a query in a reference field, such as entering `PRB` in the related Problem field and while waiting for the auto-completer to display results, decides to enter more information, such as `PRB000`. The system properties **glide.request\_manager.cancel\_other\_transaction** and **glide.request\_manager.cancel\_reference\_completer** control this use case.

-   **[Add sites to the always cancel list](../task/t_AddSitesAlwaysCancelWhiteList.md)**  
You can add UI pages or other links to the always cancel list so that users can cancel actions on these pages by navigating to another module or link.
-   **[Prevent users from canceling module transactions](../task/t_PrevUsersCancelModTrans.md)**  
You can explicitly prevent users from canceling the activity of a module by updating the module definition.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

