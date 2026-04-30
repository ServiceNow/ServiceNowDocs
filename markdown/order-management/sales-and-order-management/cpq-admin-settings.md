---
title: ServiceNow CPQ admin settings
description: Explore the admin settings in ServiceNow CPQ.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 2
breadcrumb: [ServiceNow CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# ServiceNow CPQ admin settings

Explore the admin settings in ServiceNow CPQ.

Several settings in ServiceNow CPQ control how ServiceNow CPQ interacts with the rest of your application. To get to the Settings page in ServiceNow CPQ, navigate to the ServiceNow CPQ Admin screen, click the arrow to expand the Utilities section, and then click the Settings tab near the bottom of the menu.

![Admin settings user interface](../images/cpq-admin-settings.png)

1.  Admin Version: Determines which UI theme is used for the Admin interface. The setting is maintained at the user level; each administrator can select their preference. If your ServiceNow CPQ environment contains both Configuration Manager and Transaction Manager, we highly recommend you use the new Admin UI.
    -   The new Admin UI introduces top-level navigation and color theming that helps administrators easily identify and access different administration areas.
    -   The Legacy setting retains the administration platform UI used since the application’s inception.
2.  Product Id Field: Determines the field that ServiceNow CPQ uses to match products when using product rules. Select one of the following:
    -   Product Code: Corresponds to the `Product2.ProductCode` field in Salesforce
    -   Partner Id: Corresponds to the `Product2.Id` field in Salesforce

        **Note:** the value of this field will change between environments, such as a Salesforce sandbox org and a production org. For ease of migration across environments, consider using either Product Code or External Id.

    -   External Id: Corresponds to the `Product2.ExternalId` field in Salesforce
3.  Roll Up Partner Data: When enabled, this option combines and averages the price for all items with the same partner ID when responding with easyXDM. This makes each line unique in the payload instead of representing the information individually.
4.  BOM Types to Include in Save Request: Choose BOM types to include in API request when saving the configuration. Select from the menu or type to enter custom BOM types. The default options are Sales and Manufacturing.

    The following video explains how to include multiple BOM types in API requests: [Multi BOM Enhancements](https://www.youtube.com/watch?v=arAYgupt9eU)

5.  Push BOM Data to Logik Salesforce Object: When enabled, ServiceNow CPQ creates records in Salesforce of the `LGK ConfigurationLineItem_c` object containing the BOM data when saving a configuration.
6.  Push Config Data to Logik Salesforce Object: When enabled, ServiceNow CPQ creates records in Salesforce of the `LGK ConfigurationFieldData_c` object that contains the config data when saving a configuration.
7.  Save Configurations Asynchronously: When disabled, ServiceNow CPQ waits until the configuration is saved in the database before closing the session. When enabled, ServiceNow CPQ starts the save process and immediately closes the session. In most cases, enabling this setting leads to faster workflows, but if a high volume of configurations is being edited simultaneously, disabling this setting ensures that all configurations are saved when returning.
8.  Refresh Token Username: This is the user name that ServiceNow CPQ uses for API syncing of configuration line data, configuration data, and to populate the caches for Product2, pricebook, and pricebook entries.

    Salesforce objects are synchronized every thirty minutes. If you have an issue synchronizing product, pricebook, or pricebook entries, reset the user name and wait thirty minutes to see whether the issue has been resolved.


