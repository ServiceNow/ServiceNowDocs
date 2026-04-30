---
title: Import a blueprint
description: Import a blueprint by uploading it as a ZIP file.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 2
breadcrumb: [Set up blueprints, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Import a blueprint

Import a blueprint by uploading it as a ZIP file.

## Before you begin

Role required: Admin

## Procedure

1.  In your SFDC org, create the configurable product that you want to migrate the configuration to.

2.  Note the Product2 ID of the product in the org.

    You can find the Product2 ID by selecting the product in Salesforce and checking the URL.

    ![Import blueprint](../images/cpq-blueprints-product2-id.png)

3.  Unzip the blueprint ZIP file you downloaded.

4.  In the unzipped blueprint folder, open the blueprint.yaml file for editing.

    ![Select blueprint](../images/cpq-blueprints-blueprint-yaml-file.png)Near the end, a line reads `-id: <oldProduct2Id>`.

5.  In the line just mentioned, replace the Product2 ID from the old org with the new one you just created, and save the blueprint.yaml file.

    ![Products](../images/cpq-blueprints-old-product2-id.png)

6.  Rezip your exported blueprint with the updated blueprints.yaml file, blueprints folder, fields folder, and rules folder included together, then drag the ZIP file into the designated area for file upload in the Matrix Loader.

7.  Open the Matrix Loader from the Admin area of the environment you are migrating the blueprint into.

8.  Drag the ZIP file into the file upload area in the Matrix Loader.

    ![Matrix loader](../images/cpq-blueprints-file-import-drag.png)

9.  In the new org, click to open the **Utilities** menu, and then click **Settings**.

    ![Menu](../images/cpq-blueprints-utilities-and-settings.png)

10. Check the value of the Product ID field.

    If itʼs set to “Product Code,” the process is complete.

    ![Product code](../images/cpq-blueprints-product-id-field.png)

11. If the Product ID field is set to Partner Id, for all the product rules in your blueprint, replace the Product ID in their actions with the Product2 IDs of the products in the new org.

    ![Select partner screen](../images/cpq-blueprints-partner-id.png)


## What to do next

Keep the following notes in mind:

-   After the import, configurable product IDs will not be the same as in the original blueprint—they are unique across organizations. To keep the references in rules accurate, if the setting for the Product Id field is set to Product Code, you can create new configurable products as needed and assign them the same product code.
-   Importing a blueprint does not replace the current blueprint if it already exists in the target environment. Any items removed in the older environment, such as rules, also need to be manually removed in the target environment unless they are specified in the YAML file.

**Related topics**  


[Migrate a blueprint from environment to environment](../task/cpq-migrating-env-to-env.md)

[Export a blueprint](cpq-export-a-blueprint.md)

