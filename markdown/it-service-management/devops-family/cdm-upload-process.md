---
title: Uploading your config data
description: You first create a new CDM application structure and then upload the existing config data into the structure.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring DevOps Config, DevOps Config, IT Service Management]
---

# Uploading your config data

You first create a new CDM application structure and then upload the existing config data into the structure.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## How it works: Performing the initial upload of your existing config data into CDM data tables

![Uploading config data into a new CDM application](../image/cdm-upload-process.png)

1.  Open the CDM user interface and create a new application. For example, let's create the Bookstore application to support an online bookstore. An application in CDM is the full collection of config data for an application service, application model, or dynamic CI group \[infrastructure\] in the CMDB.

    ![Create a CDM application](../image/cdm-create-new-app-page.png)

2.  Now open the Bookstore application and generate a new changeset so you can begin to put the data structure in place. \(A more detailed overview of this process appears in [Preparing an application for config data upload](cdm-prep-app-for-upload.md).\)

    ![Create a changeset](../image/cdm-generate-new-changeset.png)

    In the changeset, define the data structure that includes a node for each set of config data that you will upload. This process is called modeling the data. You add components, collections, deployables, and CDIs as needed. For information on each of these items, see [CDM data model](../reference/cdm-data-model.md). For additional information on adding nodes to an application, see [Preparing an application for config data upload](cdm-prep-app-for-upload.md).

    In this example, two components and two collections have been added. Now, the **PaymentSvc-1.0** component is included in the **Release-1.0** collection. As with all collections, this means that any data in the **PaymentSvc-1.0** component is now included in the **Release-1.0** collection.

    ![Create a changeset](../image/cdm-add-component-to-collection.png)

    When you are satisfied with the structure \(you can update at any time\), you open the REST Explorer to begin the process of uploading the source config data into the CDM data tables. Do not commit the changeset — it remains open so you can upload data.

3.  Using the REST APIs or the config data editor, set parameter values that specify the name of the application to upload to, the path within the CDM application data structure to place the data, the format of the source data \(JSON in the example\), and so on.

    **Note:** When you upload your existing config from an XML file and the **ignoreAttributes** is set to **false**, the CDM XML Parser retains the attributes in JSON using identifiers. For more information, see [Parsing of XML files in CDM](cdm-parsing-xml-file.md).

    This example shows the REST API Explorer platform utility for clarity. This is an example of how you might construct an Upload to components REST POST request that creates a `dbProperties.json` node in the **PaymentSvc-1.0** component and then adds the source data to the new node. \(You specify the source data to upload in another field.\) The APIs are described in [CdmApplicationsApi](https://www.servicenow.com/docs/access?context=applications-api&version=australia&pubname=australia-api-reference&ft:locale=en-US), [CdmChangesetsApi](https://www.servicenow.com/docs/access?context=changesets-api&version=australia&pubname=australia-api-reference&ft:locale=en-US), and [CdmSnapshotApi](https://www.servicenow.com/docs/access?context=snapshot-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

    ![REST API Explorer form.](../image/cdm-rest-explorer-components-2.png)

4.  When you select **Send**, the API reads the original config data, uploads it and aligns it into the CDM data structure.

    **Note:** Uploaded data items are sorted alphabetically within the structural folders to enable you to locate particular items quickly.

    The system places the following limits on the count of config data items \(CDIs\):

    -   An application can contain a maximum total of 100,000 CDIs.
    -   Any single deployable can contain a maximum of 10,000 CDIs.
    See [CDM system properties](../reference/cdm-system-properties.md) for information on configuring the **sn\_cdm.max\_allowed\_cdi\_per\_application** and **sn\_cdm.max\_allowed\_cdi\_per\_deployable** property settings.

    **Important:** Each time you submit a POST request, the API performs the POST and also generates an upload script. You can specify one of several script languages. The purpose is for you to use the code in your pipeline system to automate the upload process for this application in future uploads.

5.  Back to CDM: Review and update the config data as described in [Preparing an application for config data upload](cdm-prep-app-for-upload.md).
6.  When you are satisfied that the application is a full and correct representation of the config data, you can commit the changeset. The commit action generates a snapshot of each deployable and causes the API to store the data in CDM tables.

    Now that the application is fully in place, you can manage the data as needed: Update config settings, apply policies to validate the data, export valid snapshots of config data, and so on.

    While you export any snapshot, the system can generate API code that you can use to automate the export process. See [Generate API invocation code for an exporter](../task/cdm-exporter-gen-api-code.md) for details.


**Related topics**  


[Preparing an application for config data upload](cdm-prep-app-for-upload.md)

[Parsing of XML files in CDM](cdm-parsing-xml-file.md)

[Parsing of CSV files in CDM](cdm-parsing-csv-file.md)

