---
title: Migrate a blueprint between environments
description: Move blueprints between CPQ environments to maintain consistent configuration management. Export, update, and import blueprint packages using the Matrix Loader to promote tested configurations from development to production.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-migrating-env-to-env.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [blueprint migration environment export import Matrix Loader]
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Migrate a blueprint between environments

Move blueprints between CPQ environments to maintain consistent configuration management. Export, update, and import blueprint packages using the Matrix Loader to promote tested configurations from development to production.

## Before you begin

Review CPQ upgrade windows, described in [CPQ Upgrade Schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/logik_io_upgrade_schedule.md). Schedule your migration to avoid published upgrade windows. If you have questions regarding this topic, contact your customer Support team.

Role required: admin

## About this task

Understand the following terms:

-   Source: The environment from which functionality is migrated.
-   Destination: The environment to which functionality is migrated.
-   Migration package: The file or files exported from the source environment to be imported to the destination environment.

## Procedure

1.  Export the blueprint from the source environment.

    1.  In the source environment, select the blueprint to move.

        \[Omitted image "cpq-blueprints-export-1.png"\] Alt text: Blueprints list with check box selection

    2.  Select **Export**.

        \[Omitted image "cpq-blueprints-export-2.png"\] Alt text: Export blueprint button

        The first notification indicates that the export process has started. After the export completes, a second notification indicates that the blueprint is ready for download. Watch for notifications on the bell icon in the lower-left corner.

    3.  In the bell icon menu, select the **Download** link.

        \[Omitted image "cpq-blueprints-export-download.png"\] Alt text: Download blueprint link in notification menu

    4.  Save the blueprint to your local machine or a central repository such as Git.

        If your environment is integrated with Salesforce and you are migrating the blueprint for the first time, verify the prerequisites. Then perform step 1 in [Migrate a blueprint to an SFDC-integrated destination](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

2.  Modify the migration package.

    1.  Unzip the blueprint ZIP file you downloaded in step 1.

        The file unzips to a blueprint.yaml file.

        \[Omitted image "cpq-blueprints-blueprint-yaml-file.png"\] Alt text: blueprint.yaml file selection

    2.  Open the blueprint.yaml file in a text editor.

        When migrating a blueprint to a destination with an earlier version, add the following line to the bottom of the file to avoid conflicts:

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

        For a description of how this parameter affects the blueprint migration, see [The fullBlueprintMigration parameter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-fullblueprintmigration-param.md). If your environment is integrated with Salesforce and you are migrating the blueprint for the first time, perform step 2 in [Migrate a blueprint to an SFDC-integrated destination](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

    3.  Save your edits and close the blueprint.yaml file.

3.  Compress all components of the migration package to a new ZIP file.

    Include blueprint.yaml, the blueprints folder, the fields folder, the rules folder, and any other artifacts from the migration package. Do not include the parent folder. \[Omitted image "cpq-blueprints-migration-package.png"\] Alt text: Migration package contents for compression

    **Warning:** When compressing, select only the contents of the unzipped blueprint export, not the parent folder itself. If the parent folder is selected, you receive an error when uploading to the CPQ Admin.

    \[Omitted image "cpq-blueprints-upload-error.png"\] Alt text: Import error message

4.  Migrate components related to the blueprint to the production tenant.

    For example, migrate managed tables and external connections used by the blueprint.

5.  Import the blueprint to the destination environment.

    1.  Log in to the administration area of the CPQ destination environment.

    2.  Open the Matrix Loader.

    3.  Drag the edited migration package ZIP file into the Matrix Loader drop area.

    4.  Select **Next**, then select **Import**.

    If you encounter errors after the import, follow the on-screen instructions to review the error logs.

6.  Test the migration.

    1.  If your environment is integrated with Salesforce and you are migrating the blueprint for the first time, perform steps 3 and 4 in [Migrate a blueprint to an SFDC-integrated destination](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

    2.  Review your migrated blueprint from the end-user UI in the destination CPQ environment.


**Related topics**  


[CPQ Upgrade Schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/logik_io_upgrade_schedule.md)

[Migrate a blueprint to an SFDC-integrated destination](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

