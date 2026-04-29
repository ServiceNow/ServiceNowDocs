---
title: Service Catalog terms and roles
description: The Service Catalog application uses these roles to manage different aspects of the application.Can manage all aspects of the Service Catalog application, including scripting functions such as creating UI macros or business rules.Can manage the Service Catalog application, including catalogs, categories, and items, but not including scripting functions available to administrators.Can edit and update a service catalog, as well as the categories and catalog items within the catalog. The manager can assign editors and also a different manager for the service catalog. You can perform these actions only on catalogs for which you are assigned as the manager.Can edit and update a service catalog, as well as categories and catalog items within the catalog. The editor can assign other editors, but cannot change the catalog manager. You can perform these actions only on catalogs for which you are assigned as the editor.Can create and maintain advanced catalog items in Catalog Builder such that they can create, edit, or delete client scripts in Catalog Builder.Can create and maintain items in the catalog builder using the templates that the user has access to.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog terms and roles

The Service Catalog application uses these roles to manage different aspects of the application.

## Service Catalog terms

-   **Execution Plans**

    Define how something gets delivered. For example, a PDA could go through procurement / activation / and installation of the desktop software.

-   **Execution Plan Tasks**

    Plan Tasks represent a step in the Execution Plan, are associated with a Fulfillment Group, and have an approximate duration.

-   **Fulfillment Groups**

    Fulfillment Groups work execution tasks. For example, one group can activate a cell phone while a different group installs the desktop software.

-   **Tickets**

    Tickets represent work done by Fulfillment Groups as part of an Execution Plan.


**Parent Topic:**[Service Catalog Reference](../concept/service-catalog-reference.md)

## Administrator \[admin\]

Can manage all aspects of the Service Catalog application, including scripting functions such as creating UI macros or business rules.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Catalog administrator \[catalog\_admin\]

Can manage the Service Catalog application, including catalogs, categories, and items, but not including scripting functions available to administrators.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Catalog manager \[catalog\_manager\]

Can edit and update a service catalog, as well as the categories and catalog items within the catalog. The manager can assign editors and also a different manager for the service catalog. You can perform these actions only on catalogs for which you are assigned as the manager.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Catalog editor \[catalog\_editor\]

Can edit and update a service catalog, as well as categories and catalog items within the catalog. The editor can assign other editors, but cannot change the catalog manager. You can perform these actions only on catalogs for which you are assigned as the editor.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Catalog builder developer \[catalog\_builder\_developer\]

Can create and maintain advanced catalog items in Catalog Builder such that they can create, edit, or delete client scripts in Catalog Builder.

### Contains Roles

List of roles contained within the role.

catalog\_builder\_editor

### Groups

A list of groups this role is assigned to by default.

None.

### Special considerations

The catalog builder developer can do everything that a catalog builder editor can do. But additionally, the catalog builder developer has access to other advanced features, such that a person with this role can add or edit the following in Catalog Builder:

-   Dynamic and advanced reference qualifiers in the Additional details tab of a question
-   Variable attributes
-   Scriptable default values
-   Availability sections
-   Catalog client scripts

Also, the catalog builder developer can create a new catalog item without using a template. This behavior is managed by the **glide.sc.builder.allow\_create\_from\_scratch** property, which is enabled by default. If the property is turned off, the catalog builder developer must use a template to create a new catalog item.

## Catalog builder editor \[catalog\_builder\_editor\]

Can create and maintain items in the catalog builder using the templates that the user has access to.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

