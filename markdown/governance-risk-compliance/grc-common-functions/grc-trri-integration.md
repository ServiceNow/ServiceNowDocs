---
title: GRC integration with Thomson Reuters Regulatory Intelligence
description: The ServiceNow Regulatory Change Management application helps you to gather, monitor, and analyze regulatory data and track developments in a complex regulatory environment.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [GRC integrations, Common GRC features, Governance, Risk, and Compliance]
---

# GRC integration with Thomson Reuters Regulatory Intelligence

The ServiceNow® Regulatory Change Management application helps you to gather, monitor, and analyze regulatory data and track developments in a complex regulatory environment.

## Benefits of integrating with Thomson Reuters Regulatory Intelligence

Use the ServiceNow® GRC integration with Thomson Reuters Regulatory Intelligence application to integrate with the Thomson Reuters platform and to consume the Thomson Reuters Regulatory Intelligence \(TRRI\) feeds into your ServiceNow instance.

This integration helps you gather, monitor, and analyze regulatory data in a rapidly changing and complex regulatory environment. It enables you to efficiently manage and mitigate risks. GRC integration with Thomson Reuters Regulatory Intelligence involves an additional licensing cost.

Thomson Reuters Regulatory Intelligence Integration \(TRRI\) delivers regulatory feeds that include various regulatory changes. The Regulatory Change Management application transforms and maps the feeds. The Regulatory Change Management application provides the information in regulatory feed tables.

With the Thomson Reuters guided setup, you can do the following:

-   Receive regulatory feeds from the Thomson Reuters platform that are relevant to your organization.
-   Transform and map the regulatory taxonomy from the Thomson Reuters platform to your internal regulatory taxonomy.
-   Load the transformed data into your ServiceNow instance and manage regulatory changes.

In the guided setup, you can do multiple tasks and subtasks:

-   Create a Connection: Create a connection and validate it. The connection is required for integration with the Thomson Reuters platform. Tasks in this step include the following:
    -   Create Connection
    -   Validate Connection
    -   Submit OAuth Credentials
-   Activate Integration Flows: Set up a schedule and activate the flows at different times. Run the flows with a time gap, such as a gap of 12 hours between the flows. Tasks in this step include the following:
    -   Configure the flow that inserts feed files into the feed registry.
    -   Configure the flow that moves processed feeds into the destination directory.
-   Create an Internal Taxonomy: Create your taxonomy to categorize and classify the regulatory content. An internal taxonomy can be a multi-hierarchical structure.
-   Map an External Taxonomy to an Internal Taxonomy: Map the source taxonomy from the Thomson Reuters platform with the internal taxonomy that you have created.

When setting up the integration, you go through the following stages:

1.  Configure feed settings: Configure and set up the feed content, delivery settings, and delivery location in the Thomson Reuters Regulatory Intelligence \(TRRI\) feeds platform. The delivery location is where the feeds are delivered.
2.  Set up a MID Server: The Thomson Reuters platform sends the regulatory feed files to the SFTP server that's configured on the Thomson Reuters portal. An administrator should set up a MID Server with SSH capabilities for the GRC integration with Thomson Reuters Regulatory Intelligence application.

    The MID Server ingests the feed file data from the SFTP server into the ServiceNow instance. The MID Server runs as a Windows service or as a UNIX daemon to facilitate communication between an instance and the external applications.

3.  Set up SFTP connection: The Thomson Reuters platform deposits the regulatory feed files at an SFTP location that is configured in the Thomson Reuters platform portal. Create an SFTP connection and import the feed files into your ServiceNow instance. To learn more, see [Establish an SFTP or REST API connection](../task/create-conn-record-tr-int.md).

Import sets enable administrators to import data from various data sources, and then map that data into ServiceNow tables.

## Bringing series data from Thomson Reuters into the Regulatory Change Management application

The Documents in Series related list enables you to track the development of a regulatory change from the proposed stage to the final stage. You can see related events in a single place. In the Regulatory Feed form, the series name, and the regulatory events that are part of the Thomson Reuters series are displayed. You can view the Thomson Reuters series data in the Series Data section in the Regulatory Feed form. The series name and the sequence number of the feed are displayed under the Series Data section in the Regulatory Feed form. This section helps you to get more context on the regulatory events and to make decisions regarding the applicability of the events.

The Regulatory Feed table appears in the Series Data section in the Regulatory Feed form. The following new columns are added to the Regulatory Feed table for the Thomson Reuters series data:

-   Series Name: Displays the series name of the regulatory event.
-   Sequence Number: Displays the sequence number of the regulatory event.
-   Series ID: Displays the series identification number of the regulatory event. You can select the series ID from the list view. The series ID is then displayed.

The Documents in Series related list is part of the regulatory feed form. It displays the following details on the feed:

-   Number: The number of the regulatory feed as received from Thomson Reuters. For example, REG0001023.
-   Title: The title of the regulatory feed as received from Thomson Reuters. For example, CFPB-2019-0021 Home Mortgage Disclosure \(Regulation C\).
-   Sequence Number: The sequence number of the regulatory feed as received from Thomson Reuters. For example, sequence number 7. If you have all the data, then the prior six events are displayed in the related list and the seventh event in the series is displayed.

**Note:** The Series Data section and the Documents in Series related list are displayed in the Regulatory Feed form only if the feed type is regulatory event and the source of the regulatory feed is Thomson Reuters.

The regulatory data that is received from the Thomson Reuters platform is processed and brought into the staging tables in a ServiceNow instance.

## Actions to automate the integration tasks

The GRC integration with Thomson Reuters Regulatory Intelligence application provides the following actions to automate the Thomson Reuters integration tasks:

-   Get the related source documents for the regulatory events.
-   Get the Thomson Reuters  platform to feed file names from the SFTP source path.
-   Move the files processed by the Thomson Reuters platform to the destination path.
-   Trigger the scheduled import job in the Thomson Reuters  platform after getting the file names from the SFTP server.
-   Validate the path and credentials for the new SFTP connection.

The instructions for automation are covered in detail in the guided setup files that are sent with the software.

-   **[Install the GRC integration with Thomson Reuters Regulatory Intelligence application](../task/install-trri-integration.md)**  
Install the GRC integration with Thomson Reuters Regulatory Intelligence application \(com.sn\_grc\_int\_tr\). The application includes demo data. It installs related ServiceNow Store applications and plugins if they are not already installed.
-   **[Establish an SFTP or REST API connection](../task/create-conn-record-tr-int.md)**  
Establish an SFTP or REST API connection for the GRC integration with Thomson Reuters Regulatory Intelligence application. You can create an SFTP or REST API connection with the SFTP server by using the Connection &amp; Credential aliases that are shipped with the Thomson Reuters platform.
-   **[Modules in the GRC integration with Thomson Reuters Regulatory Intelligence application](../reference/modules-in-the-application.md)**  
The GRC integration with Thomson Reuters Regulatory Intelligence application includes various modules.

**Parent Topic:**[Governance, Risk, and Compliance integrations](../../grc-common/reference/grc-integrations.md)

