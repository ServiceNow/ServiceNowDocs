---
title: Context-sensitive help
description: By default, the help link available in the product opens the welcome page of the help system, allowing you to enter search criteria for the information you want to find. With context-sensitive help, you can set a base URL for an external help system. The context-sensitive system properties define the base URLs for the default and custom help systems.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Context-sensitive help

By default, the help link available in the product opens the welcome page of the help system, allowing you to enter search criteria for the information you want to find. With context-sensitive help, you can set a base URL for an external help system. The context-sensitive system properties define the base URLs for the default and custom help systems.

The ServiceNow system provides several preconfigured help contexts connected to this link that display the exact information you need for the current list, form, or record. You can define your own help topics and configure them to appear when you click the help icon in a ServiceNow record.

Users click the help icon to open the default help pages provided in the base system. For any page that does not have context-sensitive help defined, the instance displays the help system welcome page. Users can use the search feature or the index to find the correct help topic. The location of the help icon depends on the user interface version you are using.

## Core UI

Click the help icon in the right corner of the header bar and select **Search Product Documentation** from the menu.

![Context help access in Core UI](../image/context-help-page.png "Context help access in Core UI")

Alternatively, administrators can create custom context-sensitive help to suit the needs of their organizations. Create a help context that links the help icon to a topic describing a list, form, or specific record. You may initially want to set a base URL to direct to a help system other than the default ServiceNow help system.

## Set base URLs

To create numerous help contexts that direct to a single server other than the ServiceNow help system, enter the base URL in the **help.base.default** property.

![Base URL for custom help contexts](../image/HelpBaseDefault.png "Base URL for custom help contexts")

On the Help Context form, when the **ServiceNow Product Documentation** check box is cleared and you enter a value in the **URL or page name** field that does not contain the string `://`, that value is appended to the base URL defined by **help.base.default** property.

**Note:** When the **ServiceNow Product Documentation** check box is cleared and the **URL or page name** field contains an absolute URL \(distinguished by the string `://` in the value\), the value in the **help.base.default** property is ignored. This allows you to create help contexts that link to several different servers.

## Context-sensitive help properties

To access the context-sensitive help properties, navigate to **sys\_properties.list** and filter by **Name**. You can edit a property value from the list or by opening the property record.

<table id="table_rt3_cy2_n1b"><thead><tr><th>

Property Name

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

glide.help.default.page

</td><td>

The default URL the help icon directs to when no help context is specified. This is the base URL of the ServiceNow help system and opens to the welcome page. Do not change this value.

</td><td>

http://servicenow.com/docs/

</td></tr><tr><td>

help.base.default

</td><td>

The base URL for custom help contexts in which the **ServiceNow Product Documentation** check box is cleared, and an absolute URL is not specified. When the base URL is set, the system creates the address of a help conext record by appending the target page or file name to the base URL. Custom help contexts using this base URL overwrite the help provided by default in your instance for the same table. For details, see [set base URLs](c_ContextSensitiveHelp.md).

</td><td>

http://servicenow.com/docs/?context=

</td></tr><tr><td>

help.base.servicenow

</td><td>

The base URL for help contexts in which the **ServiceNow Wiki** check box is selected. This is the base URL for the help provided in your instance by default. Do not change this value. For details, see [Create a new help context](../task/t_CreateANewHelpContext.md).

</td><td>

http://servicenow.com/docs/?context=

</td></tr></tbody>
</table>-   **[Create a new help context](../task/t_CreateANewHelpContext.md)**  
You can create new help contexts to supplement or replace the default help contexts. For example, if your organization has heavily customized a form, you might create a new help context for that form. The customized help context could link to more relevant information, such as a company knowledge base article.
-   **[Help context types and prioritization](../reference/r_HelpContextTypes.md)**  
You can create a help context with the type **Form**, **List**, or **Record**, and link it to a particular table in your ServiceNow instance. If you have multiple help contexts, prioritization determines which help contexts apply to what a user views.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

