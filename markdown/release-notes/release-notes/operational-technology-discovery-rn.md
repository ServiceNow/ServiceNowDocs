---
title: Operational Technology Discovery release notes
description: The ServiceNow Operational Technology Discovery application increases visibility of OT devices in your system. Operational Technology Discovery was enhanced and updated in the Australia release.The ServiceNow Operational Technology Discovery application increases visibility of OT devices in your system. Operational Technology Discovery was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-08-31"
reading_time_minutes: 3
---

# Operational Technology Discovery release notes

The ServiceNow® Operational Technology Discovery application increases visibility of OT devices in your system. Operational Technology Discovery was enhanced and updated in the Australia release.

## About Operational Technology Discovery

**Important:** Operational Technology Discovery is being prepared for future deprecation. For more information, see the "Deprecated in this release" section of these release notes.

-   Create a backup ZIP file of the Console database from the Console web interface.
-   Use Entra ID integration to log in to the Console with your organization's Microsoft Entra ID.
-   Use the updated Console UI for an enhanced Appliances page.
-   Identify open ports using the enhanced Open Port section of the Assets page.

For more information, see [Operational Technology Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-discovery-landing.md).

## Activation and other requirements

**Note:** Operational Technology Discovery is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install the following Operational Technology Discovery applications using the Service Graph Connector for ServiceNow OT Discovery Guided Setup page. You must install the Service Graph Connector for ServiceNow OT Discovery before installing the following applications:

    -   Discovery Console
    -   Discovery Sensor
    -   Discovery Collector
    Install Operational Technology Discovery by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).


**Parent Topic:**[Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/operational-technology-rn-landing.md)

## Australia

The ServiceNow® Operational Technology Discovery application increases visibility of OT devices in your system. Operational Technology Discovery was enhanced and updated in the Australia release.

### What's new

-   **[Create a backup for the Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/create-console-backup-concept.md)**

    To support disaster recovery, the Discovery Console for OT generates backup files containing restore data, configuration, and logs.

-   **[Install containerized OT Discovery packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/install-containerized-ot-discovery-packages.md)**

    Containerized versions of the Console and the Collector are available to download from the OT Discovery Downloads page. For more information, see [Air-gapped networks and OT Discovery installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/air-gapped-networks-installation.md).

-   **[Generate a certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/generate-new-certificate-discovery-for-ot.md)**

    You can now select the link **Download Console Certificate Bundle \(.ZIP\)**. The bundle contains the Console certificate and the web browser certificate. These certificates establish trust between these applications and confirm their communications are secure and encrypted.

-   **[Set up a Microsoft Entra ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/users-entra-id-setup.md)**

    The Entra ID integration enables you to log in to the Console using your organization's Microsoft Entra ID cloud identity access management \(IAM\) credentials. This eliminates managing separate usernames and passwords within the application. This integration supports secure authentication using Microsoft Entra ID, improving the user experience and aligning with enterprise identity management practices.


### What's changed

-   **[Edit an Appliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/edit-an-appliance.md)**

    Navigate to the Appliances page where the individual Sensors and Collectors with their status and location are displayed. The page displays the component type, its endpoint, and CPU usage. Select the appliance name to see its details and additional settings.

-   **[Filter results for Host Status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/results-filter-host-status.md)**

    In the Scan Results filtering types, the **Host Status** helps you view query results based on whether the queried host was **Up** or **Down**. This filter is derived from the Nmap XML status field inside the Raw scan output.


-   **[Requirements for Discovery Console for OT installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/reqs-ot-console-installation.md)**

    The required dependency version changed from .NET 8 to .NET 10.


### What's deprecated or removed

Starting with the Australia release, Operational Technology Discovery is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For more information, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   Service Graph Connector for ServiceNow OT Discovery \(com.sn\_otdiscsgc\)
-   Discovery Console
-   Discovery Sensor
-   Discovery Collector

