---
title: Discovering a license key in a file-based discovery framework
description: License key discovery across Windows, Linux, and macOS enables ACC to automatically identify and create an inventory of license keys stored in files on managed computers. A license key proves that software installation is legitimate and is being used within the boundaries the vendor agreed to at the time of purchase.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/license-key-discovery-fbd.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [license key discovery, file-based discovery, ACC, software asset management]
breadcrumb: [ACC File-Based Discovery, ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Discovering a license key in a file-based discovery framework

License key discovery across Windows, Linux, and macOS enables ACC to automatically identify and create an inventory of license keys stored in files on managed computers. A license key proves that software installation is legitimate and is being used within the boundaries the vendor agreed to at the time of purchase.

## What is a license key

A license key is a unique string associated with a piece of software. License keys typically encode constraints such as the number of permitted users or devices, the expiration date, or the product edition or tier purchased.

Organizations track license keys for compliance audits, renewal discussions, and licensing cost management. Without visibility into license keys, organizations can't reliably determine whether they are compliant, or whether they have purchased the right number of licenses.

## Why file-based discovery is necessary

License keys are stored in different locations depending on the vendor and product architecture. The following broad storage categories exist:

|Storage location|Example vendors/products|Discoverable on-machine?|
|----------------|------------------------|------------------------|
|Windows Registry \(Windows only\)|Microsoft Office, Windows operating system|Yes — via registry-based discovery \(previously released\)|
|Files on disk \(cross-platform\)|AutoCAD, MATLAB, Quest|Yes — via file-based discovery \(current release\)|
|Cloud or user-based authentication|Modern subscription-licensed applications|No — nothing is stored on the machine|

Beginning in version 2.0.0, file-based discovery identifies license keys stored in files on any operating system, including Linux and macOS.

## How file-based discovery operates

File-based license key discovery acts as a framework rather than a single reader because every vendor's license file format differs. The framework provides the underlying mechanism to find a candidate file and pass its content for processing, while administrators supply configuration that specifies what to look for and how to read it.

This architecture enables support for new vendors and file formats through configuration alone — no platform code changes are required.

-   **[Configure a license key discovery rule and write a parser script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/configure-license-key-rule.md)**  
Enable license key discovery to verify the legitimacy of your software installation. Set up support for a new vendor's license file format by creating a parser script and defining a matching rule.

**Parent Topic:**[Agent Client Collector File-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/file-based-discovery-overview.md)

