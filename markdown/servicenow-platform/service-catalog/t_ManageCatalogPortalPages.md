---
title: Multiple service catalogs setup
description: Multiple service catalogs enable your organization to offer different sets of services to different teams within the organization, such as IT services, human resources, and facilities management.Using Service Catalog, you can create a catalog and define items and categories within the catalog.Using Service Catalog, you can view and manage items within a catalog.Using Service Catalog, you can create and manage multiple portal pages for a catalog.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using the content management system with the service catalog, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Multiple service catalogs setup

Multiple service catalogs enable your organization to offer different sets of services to different teams within the organization, such as IT services, human resources, and facilities management.

Administrators and catalog administrators can define and manage multiple service catalogs. End users can access multiple catalogs from a single homepage, can search across all catalogs, or can search directly within each catalog.

## Enabling access for catalogs

You can enable read access to the catalogs by applying the rule **read ACL** on Catalog \(sc\_catalog\) table. See [Access Control Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md) for more information.

**Parent Topic:**[Service catalog setup](../topic/p_ServiceCatalogs.md)

## Create a catalog

Using Service Catalog, you can create a catalog and define items and categories within the catalog.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Catalogs**.

2.  Select **New**.

    ![Service Catalog Details](../image/CreateNewCatalog.png)

3.  Enter the new catalog details \(see table\).

4.  Right-click the form header and select **Save**.

5.  Define catalog items and categories to include in the catalog.

6.  Define additional portal pages for the catalog.

7.  [Manage sites](../task/t_ManageCatalogSites.md) if you are using a CMS system.

<table id="table_wbl_3mg_dq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Descriptive name for the catalog.

</td></tr><tr><td>

Application

</td><td>

The application scope for this catalog. For information on the application scope, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationScope.md) .

</td></tr><tr><td>

Manager

</td><td>

Name of the catalog manager assigned to this catalog.The manager is able to edit and update the catalog, as well as the categories and catalog items within the catalog. The manager can assign editors and also a different manager for the catalog, if desired.

 Only one manager can be assigned to a catalog and must have the catalog manager role or catalog\_admin role assigned.

</td></tr><tr><td>

Active

</td><td>

Select the check box to make the catalog available to end users.

</td></tr><tr><td>

Editors

</td><td>

Name of the catalog editor. The editor is able to edit and update the catalog, as well as categories and catalog items within the catalog. The editor can assign other editors, but cannot change the manager.

 Multiple editors can be assigned to a catalog. Each user must have the catalog editor role assigned.

</td></tr><tr><td>

Enable Wish List

</td><td>

Select the check box to enable the wish list feature for the catalog.

</td></tr><tr><td>

Description

</td><td>

Information about the catalog, displayed on the multi-catalog homepage.

</td></tr><tr><td>

Background Color

</td><td>

The background color used for the catalog on the multi-catalog homepage.

</td></tr><tr><td>

Desktop image

</td><td>

The larger image to display with the catalog on the multi-catalog homepage. This image is only shown if image display is included in the [renderer](../task/t_CreatingOrModifyingRenderers.md#) selected, such as the default **Title and Image** renderer.

</td></tr><tr><td>

'Catalog Home' page

</td><td>

The location to direct service catalog users to when they click the **Catalog Home** button. This field is designed to reference a content page url suffix.

</td></tr><tr><td>

'Continue Shopping' page

</td><td>

The location to direct service catalog users to when they click the **Continue Shopping** button. This field is designed to reference a content page url suffix.

</td></tr></tbody>
</table>
### What to do next

To add a module in the navigator for the new catalog, see [Create a module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/test-steps-app-navigator-category.md).

## Manage items in a catalog

Using Service Catalog, you can view and manage items within a catalog.

### Before you begin

Role required: admin

### About this task

Use the **Catalog Items** related list on the Catalog form to view and manage the items available in the catalog.

![Catalog items list.](../image/SC_ManageItemsCatalog.png)

To define a new catalog item for the catalog, click **New** and [enter the details](../task/t_DefineACatalogItem.md#) for the item.

## Manage catalog portal pages

Using Service Catalog, you can create and manage multiple portal pages for a catalog.

### Before you begin

Role required: admin

### About this task

A catalog portal page provides a [homepage](c_ManagingTheHomepageForACatalog.md) for a specific catalog. You can use portal pages to create different catalog views for different user groups. Each portal page accesses the same catalog content and presents that content in different ways.

Catalog portal page details include the owner, title, and view to use for that page.

### Procedure

1.  The Catalog Portal Pages related list shows portal pages available for that catalog.

    Each catalog has a default page, created automatically when the catalog is created.

2.  Select an appropriate action:

    -   Click **New** to create a new portal page.
    -   Click **Edit** to select another portal page for the catalog.
    -   Select a portal page to view and edit details for that page.

**Parent Topic:**[Using the content management system with the service catalog](../topic/p_ConfigureContentManagementSystem.md)

**Related topics**  


[Manage catalogs in CMS sites](../task/t_ManageCatalogSites.md)

[Set up catalog portal pages](c_SettingCatalogPortalPages.md)

