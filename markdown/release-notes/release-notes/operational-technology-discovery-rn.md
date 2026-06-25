---
title: Operational Technology Discovery release notes
description: The ServiceNow Operational Technology Discovery application amplifies visibility of OT devices in your system. Operational Technology Discovery was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-06-10"
reading_time_minutes: 2
---

# Operational Technology Discovery release notes

The ServiceNow® Operational Technology Discovery application amplifies visibility of OT devices in your system. Operational Technology Discovery was enhanced and updated in the Australia release.

## Operational Technology Discovery highlights for the Australia release



See [Operational Technology Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-discovery-landing.md) for more information.

**Important:** Operational Technology Discovery is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Create a backup for the Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/create-console-backup-concept.md)**

    To support disaster recovery, the Discovery Console for OT generates backup files containing restore data, configuration, and logs.

-   **[Install containerized OT Discovery packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/install-containerized-ot-discovery-packages.md)**

    Containerized versions of the Console and the Collector are now available to download from the OT Discovery **Downloads** page. For detailed instructions, see [Air-gapped networks and OT Discovery installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/air-gapped-networks-installation.md).

-   **[Generate a certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/generate-new-certificate-discovery-for-ot.md)**

    You can now select the link **Download Console Certificate Bundle \(.zip\)**.The bundle contains the Console's Certificate and the web browser certificate. These certificates establish trust between these applications and confirm their communications are secure and encrypted.

-   **[Set up a Microsoft Entra ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/users-entra-id-setup.md)**

    The Entra ID integration enables you to log in to the Console using your organization’s Microsoft Entra ID cloud identity access management \(IAM\) credentials. This removes the need for managing separate usernames and passwords within the application. This integration supports secure authentication using Microsoft Entra ID, helping to improve user experience and aligning with enterprise identity management practices.


## UI changes

-   ****

    The Appliances page now displays individual Sensors and Collectors with their status and location. The page displays the component type, its endpoint, and CPU usage. Select the appliance name to see its details and additional settings.

-   **[Filter results for Host Status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/results-filter-host-status.md)**

    In the Scan Results filtering types, the **Host Status** helps you view query results based on whether the queried host was **Up** or **Down**. This filter is derived from the **Nmap XML status field** inside the Raw scan output.


## Changed in this release

Version.NET 8 has been removed.

## Activation information

Install the following Operational Technology Discovery applications using the OT Discovery **Downloads** page. For detailed instructions, see [Air-gapped networks and OT Discovery installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/air-gapped-networks-installation.md):

-   Discovery Console
-   Discovery Sensor
-   Discovery Collector

Install the Service Graph Connector for ServiceNow OT Discovery by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

The Console requires .NET 10.

## Related ServiceNow applications and features


**Parent Topic:**[Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/operational-technology-rn-landing.md)

