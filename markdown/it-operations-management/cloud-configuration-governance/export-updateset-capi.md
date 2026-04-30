---
title: Move a cloud API from one environment to the other
description: Use update sets to move a cloud API from one environment to another. Update sets let you group a cloud API and its dependencies into a named set and then move them as a unit to other systems for testing or deployment. For example, you can move a cloud API from a development environment to a production environment.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Moving Cloud Provisioning and Governance content across environments, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Move a cloud API from one environment to the other

Use update sets to move a cloud API from one environment to another. Update sets let you group a cloud API and its dependencies into a named set and then move them as a unit to other systems for testing or deployment. For example, you can move a cloud API from a development environment to a production environment.

## Before you begin

-   Users with the sn\_cmp.cloud\_service\_designer role can only export data sets.
-   Users with the admin role can export and import update sets.

Role required: sn\_cmp.cloud\_service\_designer or admin

## About this task

Package the cloud API as an update set. Then export the update set from its current environment and import it to the other environment.

**Note:** If a cloud API that you export from the source environment exists in the target environment, when you import this cloud API, it results in two cloud APIs with the same name: one cloud API that existed before the import and another cloud API which you just imported. For example, if you export the Ansible Configuration API from the development environment and you already have a cloud API with the same name in the production environment, when you import the Ansible Configuration API to the production environment, two cloud APIs with the same name, Ansible Configuration API, reside in the production environment.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud API** &gt; **API**.

    All cloud APIs appear in the Cloud API window.

2.  Export the cloud API.

    1.  Click the Export Cloud API icon \(![Export Cloud API icon](../image/export-resource-block.png)\) for the cloud API to export.

        ![Cloud API Exporter window](../image/capi-exporter.png "The Cloud API Exporter window")

    2.  In the Cloud API Exporter window, click an object in the Type column.

        In the right column, select the corresponding entries for the object that you want to export with the cloud API. For example, if you select MID Script, all the corresponding MID scripts appear in the right column.

    3.  Click **Next**.

        A window opens with a summary of the indirect dependencies of the cloud API that you chose to include in the export update set.

    4.  Click **Export Update Set**.

        The Cloud API Exporter window opens with the **Success** check box selected in green indicating that the cloud API has been successfully exported along with all its dependencies. By default, all the files listed under Exported Update Se\(t\)s get downloaded onto your system automatically.

        ![Cloud API Exporter success window](../image/capi-export-success.png)

        **Note:** The number of update sets created is based on the scope of records that are being exported. For example, assume the cloud API that you are exporting has 100 records in all: 60 records are in scope one, 20 records are in scope two, and the remaining 20 records are in scope three. In such a scenario, three update sets are created. One update set for each scope.

3.  Make sure that the files are downloaded.

    If the files are not downloaded, complete these steps:

    1.  Click the metadata file.

        The metadata file mentions the order in which the exported files should be imported. In this example, the file titled `Ansible Tower Configuration API0` is the first file to be exported, followed by the file titled `Ansible Tower Configuration API1`.

    2.  Based on the order mentioned in the metadata file, click the appropriate file to open it.

        A window opens with a list of all the files contained in the update set.

    3.  To download the first XML file \(in this example, the file is `API0 2018-05-03`\) onto your system, click **Export to XML**.

    4.  Open the other XML file \(in this example, the file is `API1 2018-05-03`\), and download that file onto your system.

        Import all the exported files into another environment. For example, you may have created the export update set in a system that runs the development environment and want to import it into another system that runs the production environment.

4.  Import the cloud API.

    1.  In the environment and the new instance where you want to import the files, enter `Retrieved Update Sets` in the filter navigator and then press the Enter key.

    2.  Click the **Import Update Set from XML** related link.

    3.  In the Import XML window that appears, click **Choose File**, select the export file, and click **Upload**.

        The cloud API gets imported to your new environment.

5.  To verify that the blueprint is imported into the new environment, go to your instance in the new environment and in the Cloud Admin Portal, navigate to **Design** &gt; **Cloud API** &gt; **API**.

    The cloud API you imported should appear in the list of cloud APIs.


