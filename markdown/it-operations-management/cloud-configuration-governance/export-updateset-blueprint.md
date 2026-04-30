---
title: Move a blueprint from one environment to another
description: Use update sets to move a blueprint and its dependencies from one environment to another. Update sets let you group a blueprint and its dependencies into a named set and then move them as a unit to other systems for testing or deployment. For example, you can move a blueprint from a development environment to a production environment.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Moving Cloud Provisioning and Governance content across environments, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Move a blueprint from one environment to another

Use update sets to move a blueprint and its dependencies from one environment to another. Update sets let you group a blueprint and its dependencies into a named set and then move them as a unit to other systems for testing or deployment. For example, you can move a blueprint from a development environment to a production environment.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer or admin

-   Users with the sn\_cmp.cloud\_service\_designer role can only export update sets.
-   Users with the admin role can export and import update sets.

## About this task

Package the blueprint as an update set. Then export the update set from its current environment and import it to another environment.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Blueprints**.

    All blueprints, in published and draft mode, appear in the Blueprints window.

2.  Export the blueprint.

    1.  Click the Export icon \(![Blueprint export icon](../image/export-resource-block.png)\) for the blueprint that you want to export.

        ![Blueprint exporter window](../image/blueprint-exporter-madrid.png "Blueprint exporter window")

        The Blueprint Exporter window has a list of all the indirect dependencies \(Policy, MID Server Script Includes, MID Server Script Files, Script Includes, and Workflows\) for the blueprint. Objects such as policies, pools, MID scripts, script includes, and workflows are not directly a part of a blueprint, but a blueprint might depend on these objects to work correctly.

    2.  In the Blueprint Exporter window, click an object in the Type column.

        In the right column, select the object's corresponding entries that you want to export with the blueprint. For example, if you select MID Server Script Includes, all the corresponding script includes appear in the right column. If a workflow contains subworkflows, select the parent workflow and all the subworkflows in order for the workflow to be exported. If there are any custom activities associated with a workflow, export those activities first and then export the workflow.

    3.  Click **Next**.

        A window opens with a summary of the indirect dependencies that you chose to include in the export update set.

    4.  Click**Export Update Set**.

        The Blueprint Exporter window opens with the **Success** check box selected in green indicating that the blueprint has been successfully exported along with all its dependencies. By default, all the files listed under Exported Update Set\(s\) get downloaded onto your system automatically. However, if the files are not automatically downloaded, follow these steps.

        ![Blueprint Exporter success window](../image/blueprint-export-success.png)

        **Note:** The number of update sets created is based on the scope of records that are being exported. For example, assume the blueprint that you are exporting has 100 records in all: 60 records are in scope one, 20 records are in scope two, and the remaining 20 records are in scope three. In such a scenario, three update sets are created. One update set for each scope.

3.  Make sure that the files are downloaded.

    If the files are not downloaded, complete these steps.

    1.  Click the metadata file.

        The metadata file mentions the order in which the exported files should be imported. In this example, the file `blueprint10` is the first file to be exported followed by the file `blueprint11`.

    2.  Based on the order mentioned in the metadata file, click the appropriate file to open it.

        A window opens with a list of all the files contained in the update set.

    3.  To download the first XML file \(in this example, the file is `blueprint10`\) onto your system, click **Export to XML**.

        Import all the exported files into another environment. Users with the admin role can import the files. For example, you may have created the export update set in a system that runs the development environment and want to import it into another system that runs the production environment.

    4.  Open the other XML file \(in this example, the file is `blueprint11`\) and download that file onto your system, too.

4.  Import the blueprint.

    1.  In the environment and the new instance where you want to import the files, enter `Retrieved Update Sets` in the filter navigator and then press the Enter key.

    2.  Click the **Import Update Set from XML** related link.

    3.  In the Import XML window that appears, click **Choose File**, select the export file, and click **Upload**.

    **Note:** If a blueprint that you exported from the source environment exists in the target environment, and both the blueprints have a different sys\_id, when you import the blueprint, an error appears and the import process stops. Export a different blueprint from the source environment or delete the blueprint with the same name in the target environment. If a blueprint that you exported from the source environment exists in the target environment and both the blueprints have the same sys\_id, then the blueprint in the target environment gets updated with the blueprint that you exported from the source environment.

5.  To verify that the blueprint is imported into the new environment, go to your instance in the new environment and in the Cloud Admin Portal, navigate to **Design** &gt; **Blueprints**.

    The blueprint you imported should appear in the listed blueprints.


