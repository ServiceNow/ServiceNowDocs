---
title: Discover portable software installed by package managers
description: Agent Client Collector for Visibility Content \(ACC-VC\) can discover software on Windows, Linux, and macOS endpoints that is not discoverable by traditional ACC-VC checks and policies. ACC-VC uses third-party package managers to track essential tools and development packages for software asset management \(SAM\) and IT asset management \(ITAM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/accvc-package-discovery.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-07-20"
reading_time_minutes: 1
breadcrumb: [ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Discover portable software installed by package managers

Agent Client Collector for Visibility Content \(ACC-VC\) can discover software on Windows, Linux, and macOS endpoints that is not discoverable by traditional ACC-VC checks and policies. ACC-VC uses third-party package managers to track essential tools and development packages for software asset management \(SAM\) and IT asset management \(ITAM\).

## Portable software discovery - overview

The Agent Client Collector software discovery policies discover software that has a dedicated executable file. The Software Discovery via Running Processes check detects software installed by package managers \(containing .js files or .py modules\) that is not detected by other ACC-VC checks, For details on ACC-VC policies and checks, see [Agent Client Collector for Visibility Content default checks and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-visibility-checks-policies.md).

With portable software package discovery, the ACC-VC agent identifies and reports portable software installed through a package manager. This includes globally-installed npm packages, which enrich your software asset inventory with Node.js-based tools and utilities.

## What gets discovered

For each package found on a host, the agent captures the following information:

-   Package name: The display name configured in the Portable Software Package Discovery \(**sn\_acc\_vis\_content\_process\_based\_sw\_config**\) table, or the actual npm package name if no display name is specified.
-   Version: The installed version of the package. Populated only if the number is available; otherwise, this field is blank.
-   Vendor/Publisher: The vendor name from the configuration. Populated only if the vendor/publisher is available; otherwise, this field is blank.
-   Installation directory: The file system path where the package is installed.

## Configuring npm package discovery

To begin discovering packages, you must configure package discovery. See [Configure portable software discovery in Agent Client Collector for Visibility Content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/configure-package-discovery-accvc.md) for step-by-step instructions.

-   **[Configure portable software discovery in Agent Client Collector for Visibility Content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/configure-package-discovery-accvc.md)**  
Configure portable software the Agent Client Collector for Visibility Content \(ACC-VC\) agent discovers by updating the config table. This ensures that only portable software that was configured is searched for and discovered.

**Parent Topic:**[Deploying Agent Client Collector on endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-endpoint-deployment.md)

