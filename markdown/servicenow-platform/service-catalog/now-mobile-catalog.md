---
title: Request experience in Now Mobile
description: You can enable users to request for an item or service, and track or approve requests on mobile using the Now Mobile app.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Service Catalog in mobile, Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Request experience in Now Mobile

You can enable users to request for an item or service, and track or approve requests on mobile using the Now® Mobile app.

## Activation of Now Mobile for Service Catalog

If you have the admin role, activate the ServiceNow Mobile Request Native Application Screens and Applet Launcher plugin \(com.glide.mobile-employee\). See [Now Mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-mobile-employee-experience/mobile-employee-experience.md). This plugin enables the Service Catalog functionality by default.

## For Me tab

When you log into Now Mobile, the following functionality related to Service Catalog is available:

-   **My To-Dos**: Displays approval records of requests and requested items assigned or delegated to the user.
-   **My Requests**: Displays requests based on the filters defined for mobile in the **My Requests Filter**. By default, the Incident Mobile and Service Catalog Request Mobile filters are available. For information about configuring filters, see [Define filters for My Requests](../task/configure-my-requests.md) and [Configure My Requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-mobile-employee-experience/set-up-my-requests.md).

    **Note:** It is recommended to include only open requests.


## Services tab

You can submit or track requests.

-   **Recent Services**: Displays the items and services \(10 items and services in the last 12 months\) that were requested recently by the logged-in user.
-   **Popular Services**: Displays the most requested items and services \(10 items and services in the last 12 months\) that are visible to the user. Displays the 10 recent items and services in the last 12 months.
-   **Browse Services**: Displays the categories of items and services that you can browse through and order.

    **Note:**

    -   If a category contains both items and sub-categories, the items specific to the category are displayed under **Others**.
    -   The category listings do not display the catalog information for users who do not have the roles that have permissions to read the records in the sc\_category table. For such users, an ACL can be added to provide read permission for the Title field of the sc\_catalog table.

**Note:**

-   You cannot request these item types in the mobile app.
    -   Content items
    -   Wizard
    -   Standard change template
-   All items hidden in Service Portal are also hidden in the mobile app.
-   In the RITM and record view, these variable types are not supported.
    -   HTML
    -   Custom
    -   Custom with Label
    -   UI Page
-   In the RITM and request view, a multi-row variable set is not supported. A message is displayed in this view that this variable set is not viewable.
-   On-load catalog UI policies \(non-scripted\) are supported for variables in record views, for example, requested item and incident.

    -   Only the visibility condition is considered.
    -   A variable with no value is not displayed.
    -   These policies are also applicable for container variables and a group of check boxes.
    -   Since the multi-row variable set is displayed with a message that it is not viewable, these policies can be used to display or hide that message.

From Now Mobile, you can also perform the following tasks:

-   Browse catalog items using the catalog hierarchy in addition to the category hierarchy. For information about its configuration, see [Browse catalog items using the catalog hierarchy](../task/now-mob-browse-cat-item-catalog.md).
-   Change the label of the **Submit** button for a record producer. For information on editing the button label, see [Edit the label of Submit button for a record producer](../task/edit-recprdcr-submit-label.md).
-   Use the mobile camera to scan bar codes for identifying a variable value of a catalog item. This is only applicable by using the **barcode** attribute for the Single Line Text variable. For information about this variable attribute, see [Service Catalog variable attributes](../reference/variable-attributes.md).

## Quick actions

You can provide easy access to a catalog item by creating a quick action. For information on creating a quick action in Now Mobile, see [Create a quick action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-mobile-employee-experience/add-quick-action.md).

## Siri shortcuts

iOS users can use Siri shortcuts to open the following pages in the mobile app.

-   Browse items and services.
-   Open my requests

See [Siri shortcuts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-mobile-employee-experience/setup-mobile-employee.md).

## Now Mobile properties

You can define the following behavior for various catalog entities by configuring the Now Mobile properties. For information about configuring these properties, see [Configure Now Mobile properties](../task/config-now-mob-properties.md).

-   Sort categories by the **Order** field.
-   Define the availability of a catalog item in one of the following ways:
    -   Include the catalog item with **Availability** set to `Desktop only` in Now Mobile.
    -   Specify catalog item types to exclude in Now Mobile.
-   Define the non-availability behavior of a catalog item by making it discoverable but not viewable, or not available at all.
-   Specify colors for buttons to match your mobile theme.

-   **[Configure catalogs](../../../administer/mobile-employee/task/configure-catalog.md)**  
Enable your users to view and request their associated items in the Now Mobile app. If no catalogs are selected, users can view and request items from all catalogs in the system. By default, the app uses Service Catalog.
-   **[Browse catalog items using the catalog hierarchy](../task/now-mob-browse-cat-item-catalog.md)**  
In addition to the category hierarchy, browse catalog items using the catalog hierarchy for proper context.
-   **[Submit and track a request](../../../administer/mobile-employee/task/order-item.md)**  
Submit a request for an item or service and track the progress of your request with the Now Mobile app.
-   **[Create a quick action in your mobile applications](../../../administer/mobile-employee/task/sc-quick-action.md)**  
Provide easy access to an important item by creating a quick action. For example, you can create a quick action that opens a Service Catalog item.
-   **[Enable notifications in Now Mobile](../task/enable-notification-mobile.md)**  
Allow push notifications on your mobile device when there is an update for a request.
-   **[Enable the cart in Now Mobile](../task/enable-cart-mobile.md)**  
Allow a requester to add or edit items in the cart. By default, the cart is disabled in Now Mobile.
-   **[Edit the label of Submit button for a record producer](../task/edit-recprdcr-submit-label.md)**  
For a record producer submission experience that you can relate to, edit the label of the **Submit** button.
-   **[Configure Now Mobile properties](../task/config-now-mob-properties.md)**  
Define the behavior of various catalog entities in Now Mobile.

**Parent Topic:**[Service Catalog in mobile](catalog-experience-mobile.md)

**Related topics**  


[Fulfiller experience in Mobile Agent](../../../administer/service-administration/concept/itsm-mobile-request-approval.md)

[Now Mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-mobile-employee-experience/mobile-employee-experience.md)

[Mobile plugins and upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/plugins-upgrades.md)

