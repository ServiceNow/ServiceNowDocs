---
title: Employee document management bulk imports
description: Use the Employee Document Management Bulk Imports feature to copy your employee documents from an external third-party cloud-based storage or a local network directory to Employee Document Management. Having your employee documents within HR Service Delivery makes administration efficient and convenient.
locale: en-US
release: australia
product: Employee Document Management
classification: employee-document-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Employee Document Management, Employee Document Management, HR Documents, HR Service Delivery, Employee Service Management]
---

# Employee document management bulk imports

Use the Employee Document Management Bulk Imports feature to copy your employee documents from an external third-party cloud-based storage or a local network directory to Employee Document Management. Having your employee documents within HR Service Delivery makes administration efficient and convenient.

**Note:** Starting with the Zurich release, Bulk Import for EDM is being prepared for deprecation. If you're an existing customer, you can continue using this feature as-is, with no new functionality. New customers will not have access to this feature.

-   You can use the **Stage local files** workflow in Employee document management to import files using the SSH protocol through MID server.
-   The **Stage local files** workflow will be available only if you have installed the Orchestration plugin \(com.snc.runbook\_automation\). The SSH related activities in this workflow are available as part of the Orchestration plugin only.

If you currently store your employee documents outside of HR Service Delivery, you can consolidate and maintain these documents over the duration of your employees tenure.

## Your current document repository

Where you currently store your employee documents determines bulk import configuration. The Employee Document Management bulk imports feature provides integration with:

-   Local document storage solution.
-   Third-party, cloud-based document storage solutions.

## Configuring local document storage

Activating the Orchestration \[com.snc.runbook\_automation\] plugin is required for importing employee documents from a local document repository.

**Note:** Java JRE 6 or later is also required.

![EDM — Local directory diagram](../image/edm-local-diagram.png)

The process for configuring HR Service Delivery with a local document repository is:

1.  Configure HR Service Delivery to communicate with the source location from Employee Document Import Configuration.

    Before you can configure a local document storage, ensure that a [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) is configured and available. A MID server is required to facilitate communication and movement of data between a ServiceNow instance and applications, data sources, and services.

    **Important:** By default, this feature expects the file server to be UNIX. If the file server is any OS other than UNIX, then you must customize the solution.

    -   Only Secure Shell Protocol \(SSH\) credentials are supported.
    -   The MID server can be on a Windows or Linux server. The server that hosts the files to be imported must be non-windows.

        **Note:** Other methods of configuring your local document storage requires custom development.

    Create a credential to use for authentication with the local document storage. See [Set up SSH credentials to the MID Server](https://www.servicenow.com/docs/access?context=set-up-and-config-MID-server&version=australia&pubname=australia-security-management&ft:locale=en-US).

    **Note:** When connecting to a local document repository, you may need to grant admin rights.

2.  Create or edit the Verify source step. This step creates a source step required to validate the connection between your local directory and Employee Document Management.

    **Note:** Having your source employee documents in a central repository, simple directory structure, and consistent file naming convention is highly recommended and reduces errors.

3.  Run the Start verify source job to verify the connection and validate source employee documents are identified and located.
4.  Create or edit the Employee Document Import Sources. This step identifies the source documents you want to import from your local document storage to Employee Document Management.
5.  Run the staging job. This step saves information about your source employee documents into the Employee Document Staging \[sn\_hr\_ef\_import\_staging\] table. All required information to import the employee document is contained in this record.
6.  Verify that steps 3 and 4 are correct by viewing your staging records. You can fix errors in the staging table.
7.  Create or edit the Capture Source step. This source step imports the staging records and source employee documents to Employee Document Management.
8.  Start the Capture job that processes the staging records that have a state of **Ready** and pulls or looks up the source employee documents. Your source employee documents are copied to Employee Document Management.

## Configuring third-party, cloud-based document storage

Activating the ServiceNow IntegrationHub Installer \[com.glide.hub.integrations\] plugin is required for importing employee documents from a third-party, cloud-based document repository.

**Note:** Integrating with a third-party, cloud-based document storage is considered a custom implementation. Employee document management bulk imports provides a basic framework to integrate with third-party, cloud-based document storage. You may need to consult with your ServiceNow Solution Consultant.

![EDM — Cloud diagram](../image/edm-cloud-diagram.png)

You need the following to configure with your third-party cloud-based \(source\) document repository:

-   The URL to your source document repository.
-   Credential alias.

The process for configuring HR Service Delivery with a third-party cloud-based document storage is:

1.  Configure HR Service Delivery to communicate with the third-party, cloud-based source document repository.
2.  Create or edit the Verify source step. This step creates a source step required to validate the connection between your third-party, cloud-based document repository and Employee Document Management.

    **Note:** Having your source employee documents in a simple directory structure and consistent file naming convention is highly recommended and reduces errors.

3.  Run the Start verify source job to verify your connection from your third-party, cloud-based document repository is communicating with Employee Document Management.
4.  Create or edit the Directory import sources step. This step identifies the directory your source documents are located in your third-party, cloud-based document storage.
5.  Create or edit the File import sources step. This step identifies the source documents you want to import from your third-party, cloud-based document storage to Employee Document Management.
6.  Run the staging job. This step saves information about your source employee documents into the Employee Document Staging \[sn\_hr\_ef\_import\_staging\] table. All required information to import the employee document is contained in this record.
7.  Verify that steps 3 and 4 are correct by viewing your staging records. You can fix errors in the staging table.
8.  Create or edit the Capture Source step. This source step imports the staging records and source employee documents to Employee Document Management.
9.  Start the Capture job that processes the staging records that have a state of **Ready** and pulls or looks up the source employee documents. Your source employee documents are copied to Employee Document Management.

## File size limitations

The base system allows you to import employee documents that are 30 megabytes or smaller.

Use the **sn\_hr\_ef.max\_file\_size** field in the Properties for Employee Document Management Application to set the maximum file size allowed.

**Note:** Increasing the maximum size can affect system performance.

For more information, see [Properties for Employee Document Management application](../reference/employee-doc-properties.md).

-   **[Use import mapping to locate and transform source employee documents](import-mapping.md#)**  
Import mapping locates your source employee documents from your source document repository and transforms them to import them to Employee Document Management.
-   **[Configuring employee document management bulk import with source document repository](../task/edm-bulk-configuration.md#)**  
Use Employee Document Import Configuration to identify and communicate with the source document repository. The source document repository is where you currently store your employee documents.
-   **[Bulk import map examples](../reference/edm-map-examples.md)**  
Mapping your source employee documents to required elements in Employee Document Management is crucial for a successful bulk import.
-   **[Correcting employee documents in the staging table](../task/edm-doc-staging.md)**  
Use the Employee Document Staging form to correct staging records prior to importing to HR Service Delivery. Staging records are created after you have mapped your source employee documents and the Start staging job has run.

**Parent Topic:**[Using Employee Document Management](using-employee-document-management.md)

**Related topics**  


[Managing employee documents](hr-doc-management-admin.md#)

