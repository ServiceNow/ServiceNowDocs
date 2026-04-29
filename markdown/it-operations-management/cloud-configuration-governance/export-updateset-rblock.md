---
title: Move a resource block from one environment to the other
description: Use update sets to effortlessly transfer resource blocks and their dependencies between environments. Group them into a named set, facilitating seamless movement for testing or deployment. Simplify processes such as transferring a resource block from development to production, ensuring efficient and organized transitions across different systems.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Moving Cloud Provisioning and Governance content across environments, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Move a resource block from one environment to the other

Use update sets to effortlessly transfer resource blocks and their dependencies between environments. Group them into a named set, facilitating seamless movement for testing or deployment. Simplify processes such as transferring a resource block from development to production, ensuring efficient and organized transitions across different systems.

## Before you begin

-   Users with the sn\_cmp.cloud\_service\_designer role can only export update sets.
-   Users with the admin role can export and import update sets.

Role required: sn\_cmp.cloud\_service\_designer or admin

## About this task

Package the resource block as an update set. Then export the update set from its current environment and import it to the other environment.

**Note:** If a resource block that you export from the source environment exists in the target environment, when you import this resource block, it results in two resource blocks with the same name: one resource block that existed before the import and another resource block which you just imported. For example, if you export the AWS Datacenter resource block from the development environment and you already have a resource block with the same name in the production environment, then when you import the AWS Datacenter resource block to the production environment, two resource blocks with the same name, AWS Datacenter, reside in the production environment.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

    All resource blocks, in published and draft mode, appear in the Resource Blocks window.

2.  Export the resource block.

    1.  Click the Export Resource block icon \(![Export resource block icon](../image/export-resource-block.png)\) for the resource block to export.

        ![Resource block exporter window](../image/export-resource-block-aws.png "Resource block exporter window")

    1.  In the Resource Block Exporter window, click an object in the Type column.

        In the right column, select the corresponding entries for the object that you want to export with the resource block. For example, if you select MID Server Script Includes, all the corresponding script includes appear in the right column.

        If a workflow contains subworkflows, select the parent workflow and all the subworkflows in order for the worklow to be exported. If there are any custom activities associated with a workflow, export those activities first and then export the workflow.

    2.  Click **Next**.

        A window opens with a summary of the indirect dependencies that you chose to include in the export update set.

    3.  Click **Export Update Set**.

        The Resource Block Exporter window opens with the **Success** check box selected in green indicating that the resource block has been successfully exported along with all its dependencies. By default, all the files listed under Exported Update Set\(s\) get downloaded onto your system automatically.

        ![Resource Block Exporter window](../image/resourceblock-export-success.png)

        **Note:** The number of update sets created is based on the scope of records that are being exported. For example, assume the resource block that you are exporting has 100 records in all: 60 records are in scope one, 20 records are in scope two, and the remaining 20 records are in scope three. In such a scenario, three update sets are created. One update set for each scope.

3.  Make sure that the files are downloaded.

    If the files are not downloaded, complete these steps.

    1.  Click the metadata file.

        The metadata file mentions the order in which the exported files should be imported. In this example, the file `Azure Datacenter0` is the first file to be exported followed by the file `Azure Datacenter1`.

    2.  Based on the order mentioned in the metadata file, click the appropriate file to open it.

        A window opens with a list of all the files contained in the update set.

    3.  To download the first XML file \(in this example, the file is `Azure Datacenter0`\) onto your system, click **Export to XML**.

    4.  Open the other XML file \(in this example, the file is `Azure Datacenter1`\), and download that file onto your system.

        You must import all the exported files into another environment. For example, you may have created the export update set in a system that runs the development environment and want to import it into another system that runs the production environment.

4.  Import the resource block.

    1.  In the environment and the new instance where you want to import the files, enter `Retrieved Update Sets` in the filter navigator and then press the Enter key.

    2.  Click the **Import Update Set from XML** related link.

    3.  In the Import XML window that appears, click **Choose File**, select the export file, and click **Upload**.

        **Note:** If a resource block that you exported from the source environment exists in the target environment, and both the resource blocks have a different sys\_id, when you import the resource block, an error appears and the import process stops. Export a different resource block from the source environment or delete the resource block with the same name in the target environment. If a resource block that you exported from the source environment exists in the target environment and both the resource blocks have the same sys\_id, then the resource block in the target environment gets updated with the resource block that you exported from the source environment.

5.  To verify that the resource block is imported into the new environment, go to your instance in the new environment and in the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

    The resource block you imported should appear in the listed resource blocks.


