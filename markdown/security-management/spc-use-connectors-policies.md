---
title: Service Graph Connectors for Security Posture Control
description: Security Posture Control relies on API integrations or Service Graph Connectors as a key source for the asset data used to identify security gaps.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-18"
reading_time_minutes: 2
breadcrumb: [Explore, Security Posture Control, Security Operations]
---

# Service Graph Connectors for Security Posture Control

Security Posture Control relies on API integrations or Service Graph Connectors as a key source for the asset data used to identify security gaps.

Security Posture Control currently supports service graph connectors \(SGC\)s that can provide you with a wide variety of data about your assets. These integration applications are available from the ServiceNow Store.

Choose the connectors you want to use and download the applications and activate them. The list of supported connectors in the Store will grow as Security Posture Control supports more connectors.

To take full advantage of Security Posture Control features, you might want to download and activate the following Service Graph Connector products to support the categories listed below.

Service graph connectors supported by Security Posture Control currently include the following categories:

-   Digital Employee Experience
-   Discovery
-   Endpoint Management: Microsoft Intune or Jamf Device and Endpoint Management.
-   IT Asset Management
-   Infrastructure Monitoring
-   Networking
-   Network Security
-   Network Performance Monitoring
-   Configuration and Patch Management: Microsoft SCCM or IBM Bigfix.
-   Endpoint Protection: CrowdStrike or SentinelOne.
-   Cloud Provider: Amazon AWS Cloud, Microsoft Azure, GCP.

    **Note:** If Cloud Discovery is activated, these service graph connector products are not required.

-   Application Performance Monitoring
-   Directory Services \(Active Directory\) Microsoft Active Directory
-   Vulnerability Assessment: Qualys, Rapid7, or Tenable.

After you install them, you can view the connectors and their categories on the connector table \[sn\_sec\_spc\_core\_connector\] in your instance.

You can view Asset types and how they map to CI classes and Connectors on the \[sn\_sec\_spc\_core\_asset\_type\_connector\] table.

See [Supported hardware service graph connectors for Security Posture Control](../reference/scp-hw-connectors-ci-classes.md) and [Supported software service graph connectors for Security Posture Control](../reference/spc-connector-types-ci-classes.md) for more information and examples of these tables. Although not extensive lists, you can see how the supported connectors provide a wide variety of data.

Security Posture Control supports ServiceNow products such as Software Asset Management \(SAM\) and Hardware Asset Management \(HAM\) that you can use along with service graph connectors to help you to look for any discrepancies that exist between the installed software reported by your vulnerability scanner products and the software reported by scanners that is already accounted for in SAM and other ServiceNow products.

For more information about downloading, configuring, and activating supported applications for service graph connectors, see the following topics:

-   [Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   [Download an application from the ServiceNow Store for the first time](../../security-incident-response/reference/download-app-first-time.md).
-   [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

