---
title: CMS to Service Portal transition
description: Your CMS may include complex forms and customizations that do not render as expected in Service Portal. Use this guide to understand how best to modify your CMS and Service Catalog implementation for Service Portal adoption, and to understand how a conversion may affect your users.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Content Management and Service Portal, Understanding Service Portal, Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# CMS to Service Portal transition

Your CMS may include complex forms and customizations that do not render as expected in Service Portal. Use this guide to understand how best to modify your CMS and Service Catalog implementation for Service Portal adoption, and to understand how a conversion may affect your users.

If you are considering transitioning from CMS to Service Portal, make sure that you understand the impact of moving to a mobile environment. Review the Mobile client GlideForm \(g form\) scripting and migration.

**Note:** For information about redirecting CMS users to Service Portal, see the [How to automatically redirect users who navigate to any CMS pages to Service Portal \[KB0722455\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0722455) article in the Now Support Knowledge Base.

## Support level and transition actions

<table id="table_vsy_zyn_z1b"><thead><tr><th>

CMS component

</th><th>

Service Portal support

</th><th>

Possible transition actions

</th></tr></thead><tbody><tr><td>

Data lookups

</td><td>

The client-side component of a data lookup is not supported in Service Portal. However, the data lookup is applied in the platform when a record is submitted or updated in Service Portal.

</td><td>

While data lookups are not applied in the Service Portal, the record updates as expected in the platform UI when submitted or updated in the Service Portal. If your CMS is used by requesters only, this limitation may not affect your implementation.

</td></tr><tr><td>

Content blocks

</td><td>

Because Content blocks use Jelly, they are not supported in Service Portal

.

</td><td>

In the Service Portal, content blocks are replaced by widgets. Widgets are highly customizable components that can query record data, display and update records, and gather user input.

 Base system widgets generally cover most use cases. Just as you add content blocks to a page in your CMS, you can add widgets to a page using the Service Portal Designer.

</td></tr><tr><td>

UI Macros

</td><td>

Because UI Macros use Jelly, they are not supported in Service Portal.

</td><td>

-   In Service Portal, you can use widgets instead of UI Macros. Base system widgets generally cover most use cases, but for custom solutions, you can develop new widgets using AngularJS.
-   If your implementation includes UI Macros in Service Catalog forms that reference other fields or variables in the form, you can embed the widget inside a Service Catalog variable. Learn more: [Replace a Service Catalog form script with a widget](../task/ui-macro-widget.md).

</td></tr><tr><td>

UI actions

</td><td>

All server-side UI actions are supported in Service Portal, although setRedirectURL\(\) operations are ignored because Service Portal forms handle redirection in a different way than the platform.

 The form widget ignores all UI actions marked as Client.

</td><td>

-   Refactor any UI actions to remove setRedirectURL\(\) operations.
-   Check that UI actions are not marked as client.

</td></tr><tr><td>

Catalog client scripts

</td><td>

Only UI Type options **Mobile / Service Portal** and **All** are supported. UI type **Desktop** is not supported in Service Portal. For a list of supported APIs, see [Service Portal and client scripts](unsupported_client_scripts.md).

 **Note:** Synchronous JavaScript calls are not supported in Service Portal and must be replaced by asynchronous calls. For example, the getXMLWait\(\) method of the GlideAjax class is not supported in Service Portal. Instead, use one of the following supported asynchronous methods:

-   getXML\(Function callback\)
-   getXMLAnswer\(Function callback\)

For additional information on GlideAjax, refer to GlideAjax.

 To understand the impact of updating your CMS to work in a mobile environment, review Mobile client GlideForm \(g form\) scripting and migration.

</td><td>

-   Update your scripts to remove any unsupported client APIs.
-   Check that the script UI Type is set to **Mobile / Service Portal** or **All**.

</td></tr><tr><td>

UI policies

</td><td>

Scripted UI policies can only use APIs supported in Service Portal. For a list of supported APIs, see [Service Portal and client scripts](unsupported_client_scripts.md).

</td><td>

Update your scripts to remove any unsupported client APIs.

</td></tr><tr><td>

Service Catalog variables

</td><td>

Service Catalog variables are supported in Service Portal with the following exceptions:

 -   UI Macros and UI pages variable types are not supported.
-   Validation Scripts for variables are not supported. Supported validation types include:
    -   The **Mandatory** field on the variable form.
    -   Read-only variables.
    -   All fields in the **Availability** tab of the variable form.
-   Default variable size is not supported.
-   Expanding and collapsing help text is not supported. Rather, the **Help text** and **Instructions** fields defined in the Annotations tab on the variable form are always expanded. The **Help tag** does not display.
-   The List Collector variable displays as a choice list instead of a slushbucket in the Service Portal.

</td><td>

-   If embedding a widget in a catalog item form, you can use the UI Macro variable type. Learn more: [Replace a Service Catalog form script with a widget](../task/ui-macro-widget.md).
-   If using variable with annotations, make sure to test your catalog items in Service Portal to ensure that help text displays as expected.

</td></tr><tr><td>

Order guides

</td><td>

Order Guides in Service Portal use the Order Guide widget.

</td><td>

Large order guides can cause performance issues in the Service Portal. If you have large order guides, you can:

 -   Break them into multiple order guides.
-   Simplify variables used in the order guides.
-   As a temporary solution, you can render the Service Catalog item using an iFrame. See [Service Catalog forms in Service Portal](sc-forms-in-sp.md).

</td></tr><tr><td>

Record producers

</td><td>

Record producers are used in Service Portal with the following differences:

 -   The sort order for catalog items in record producers is not honored.
-   Date values do not honor time zone when the record producer submits a record.

</td><td>

Make sure to test all record producers used in Service Portal to make sure that they behave as expected.

</td></tr><tr><td>

Login scenarios and redirects

</td><td>

In CMS, you used the CMSEntryPage script include to define login scenarios. Instead, Service Portal uses the SPEntryPage script include and related system properties to define login scenarios. Redirects are not supported in Service Portal.

</td><td>

In Service Portal, define login behavior by modifying the SPEntryPage script include and setting system properties.

 For more information, see [Single sign-on, logins, and URL redirects](c_SPSSOLoginAndRedirects.md#).

</td></tr><tr><td>

Service Catalog forms

</td><td>

Service Catalog forms such as catalog items and record producers are rendered within widgets in a two-column layout. Complex forms may not display as expected.

 -   Only the top-level container settings are honored. If there are other containers within the top-level container, they are rendered as a single column. If there are container splits or nested containers within these additional containers, they are rendered as a single column. A top-level container is not a child of any other container.
-   There can be a maximum of two columns in Service Portal. If your implementation includes forms with more than two columns, the fields are reorganized into two-columns in Service Portal.
-   Variable sets are treated as containers. All previously listed rules apply to variable sets as well as any containers within them.
-   Default variable size is not supported in Service Portal.

</td><td>

-   Simplify any complex forms in your Service Catalog.
-   As a temporary solution, you can render the Service Catalog item using an iFrame. See [Service Catalog forms in Service Portal](sc-forms-in-sp.md).

</td></tr><tr><td>

Shopping cart

</td><td>

The Service Portal includes a base system Shopping Cart widget.

</td><td>

Use the Shopping Cart widget.

</td></tr></tbody>
</table>**Parent Topic:**[Content Management and Service Portal](c_CMSAndSP.md)

