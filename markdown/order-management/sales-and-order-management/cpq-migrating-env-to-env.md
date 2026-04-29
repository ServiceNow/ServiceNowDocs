---
title: Migrate a blueprint from environment to environment
description: Migrate blueprints between CPQ environments to ensure consistent configuration management. Export, update, and import blueprint packages safely using the Matrix Loader to promote tested configurations from development to production.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Migrate a blueprint from environment to environment

Migrate blueprints between CPQ environments to ensure consistent configuration management. Export, update, and import blueprint packages safely using the Matrix Loader to promote tested configurations from development to production.

## Before you begin

Understand CPQ upgrade windows, described in [CPQ Upgrade Schedule](../concept/logik_io_upgrade_schedule.md). Schedule your migration to avoid published upgrade windows. If you have questions regarding this topic, reach out to your Customer Success Manager.

The following terms are used in this task:

-   **Source**

    The environment from which functionality is migrated.

-   **Destination**

    The environment to which functionality is migrated.

-   **Migration package**

    The file or files exported from the source environment to be imported to the destination environment.


This task assumes that migration is performed on one or more blueprints at a time.

Role required: \(unknown\)

## Procedure

1.  Export the blueprint from the source.

    1.  In the source environment, select the blueprint you want to move by clicking the check box next to its name.![Bleprints](../images/cpq-blueprints-export-1.png)

    2.  Click **Export**.![Export blueprint](../images/cpq-blueprints-export-2.png)

        Watch for notifications on the bell icon located in the lower-left corner. The first notification indicates that the export process has started. After the export is complete, a second notification indicates that the blueprint is ready for download.

    3.  To download the blueprint, click the **Download** link in the bell icon menu.![Download blueprint](../images/cpq-blueprints-export-download.png)

    4.  Save the blueprint to your local machine or a central repository such as Git.

    5.  If your environment is integrated with Salesforce and you are migrating the blueprint for the first time, confirm the prerequisites and perform step 1 in [Migrate a blueprint to an SFDC-integrated destination](cpq-migrating-to-sfdc.md).

2.  Modify the migration package.

    1.  Unzip the blueprint ZIP file you downloaded in step 1.

        The file unzips to a blueprint.yaml file.

        ![blueprint.yaml file selection](../images/cpq-blueprints-blueprint-yaml-file.png)

    2.  Open the blueprint.yaml file in a text editor.

        When migrating a blueprint to a destination in which an earlier version of the blueprint resides, we recommend adding the following line to the bottom of the file:

        ```
        fullBlueprintMigration: true
        ```

        Sample edited blueprint.yaml file:

        ```
        ---
        blueprints:
        - variableName: someBlueprint
          related Fields:
          - field1
          - field2
          - field3
          lastModifiedBy: dev5@dev.logik.io
          name: someBlueprintName
          description: BP description goes here
          relatedSets: null
          scripts: null
          layouts: null
          products: null
        productPickers: /fields/productPickers.yaml
        sets: null
        fieldOptions: /fields/fieldOptions.csv
        rules: /rules/rules.csv
        fields: /fields/fields.csv
        fullBlueprintMigration: true
        ```

        For a description of how this parameter affects the blueprint migration, see [The fullBlueprintMigration parameter](../reference/cpq-fullblueprintmigration-param.md).

    3.  If your environment is integrated with Salesforce and you are migrating the blueprint for the first time, perform step 2 in [Migrate a blueprint to an SFDC-integrated destination](cpq-migrating-to-sfdc.md).

    4.  Save your edits and close the blueprint.yaml file.

3.  Compress all components of the migration package \(including blueprint.yaml, the blueprints folder, the fields folder, the rules folder, and any other artifacts that may have been present in the migration package, but not the parent folder\) to a new ZIP file.![Download blueprint](../images/cpq-blueprints-migration-package.png)

    **Important:** When compressing, make sure to select only the contents of the unzipped blueprint export, and not the parent folder itself. If the parent folder is selected, you will receive an error when you upload it to the CPQ Admin.

    ![Import logs](../images/cpq-blueprints-upload-error.png)

4.  Migrate components related to the blueprint you are migrating \(for example, managed tables and external connections used by the blueprint\) to the production tenant.

5.  Import the blueprint to the destination.

    1.  Log into the administration area of the CPQ destination environment.

    2.  Open the Matrix Loader.

    3.  Drag the edited migration package ZIP file into the Matrix Loader drop area.

    4.  Click **Next**, and then click **Import**.

    If you encounter errors after the import, follow the on-screen instructions to review the error logs.

6.  Test the migration.

    1.  If your environment is integrated with Salesforce and you are migrating the blueprint for the first time, perform steps 3 and 4 in [Migrate a blueprint to an SFDC-integrated destination](cpq-migrating-to-sfdc.md).

    2.  Review your migrated blueprint from the end-user UI in the destination CPQ environment.


**Related topics**  


[CPQ Upgrade Schedule](../concept/logik_io_upgrade_schedule.md)

[Migrate a blueprint to an SFDC-integrated destination](cpq-migrating-to-sfdc.md)

