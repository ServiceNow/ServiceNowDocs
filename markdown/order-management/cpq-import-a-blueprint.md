---
title: Import a blueprint
description: Import a blueprint by uploading it as a ZIP file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-import-a-blueprint.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Import a blueprint

Import a blueprint by uploading it as a ZIP file.

## Before you begin

Role required: admin

## Procedure

1.  In your Salesforce org, create the configurable product that you want to migrate the configuration to.

2.  Note the Product2 ID of the product in the org.

    You can find the Product2 ID by selecting the product in Salesforce and locating the ID in the URL.

    \[Omitted image "cpq-blueprints-product2-id.png"\] Alt text: Import blueprint

3.  Unzip the blueprint ZIP file you downloaded.

4.  In the unzipped blueprint folder, open the blueprint.yaml file for editing.

    \[Omitted image "cpq-blueprints-blueprint-yaml-file.png"\] Alt text: Select blueprintLocate the line that reads `-id: <oldProduct2Id>`.

5.  In the -id line, replace the Product2 ID from the old org with the new one you created, and save the blueprint.yaml file.

    \[Omitted image "cpq-blueprints-old-product2-id.png"\] Alt text: Products

6.  Rezip your exported blueprint with the updated blueprints.yaml file, blueprints folder, fields folder, and rules folder.

    You will drag the ZIP file into the file upload area in the Matrix Loader in a later step.

7.  Open the Matrix Loader from the Admin area of the environment you are migrating the blueprint into.

8.  Drag the ZIP file into the file upload area in the Matrix Loader.

    \[Omitted image "cpq-blueprints-file-import-drag.png"\] Alt text: Matrix loader

9.  In the new org, navigate to **Utilities** &gt; **Settings**.

    \[Omitted image "cpq-blueprints-utilities-and-settings.png"\] Alt text: Menu

10. Check the value in the **Product ID** field.

    If it's set to **Product Code**, the process is complete.

    \[Omitted image "cpq-blueprints-product-id-field.png"\] Alt text: Product code

11. If the **Product ID** field is set to **Partner Id**, for all the product rules in your blueprint, replace the Product ID in their actions with the Product2 IDs of the products in the new org.

    \[Omitted image "cpq-blueprints-partner-id.png"\] Alt text: Select partner screen


## What to do next

Keep the following notes in mind:

-   After the import, configurable product IDs will not be the same as in the original blueprint. They are unique across organizations. To keep the references in rules accurate, if the setting for the **Product Id** field is set to **Product Code**, you can create configurable products as needed and assign them the same product code.
-   Importing a blueprint does not replace the current blueprint if it already exists in the target environment. Any items removed in the older environment, such as rules, must be manually removed in the target environment unless they are specified in the YAML file.

**Related topics**  


[Migrate a blueprint between environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Export a blueprint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-export-a-blueprint.md)

