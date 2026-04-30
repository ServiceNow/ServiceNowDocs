---
title: Using Agent Client Collector for Visibility - Content
description: When Agent Client Collector for Visibility - Content \(ACC-VC\) is installed on your Windows, Linux, or macOS servers, various information is collected depending on what other features or products you have installed.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Agent Client Collector for Visibility - Content, Agent Client Collector, IT Operations Management]
---

# Using Agent Client Collector for Visibility - Content

When Agent Client Collector for Visibility - Content \(ACC-VC\) is installed on your Windows, Linux, or macOS servers, various information is collected depending on what other features or products you have installed.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Using push-based Discovery and horizontal IP-based Discovery together](using-enhanced-discovery-and-agent-less-discovery-together.md)**  
Discovery performed by Agent Client Collector for Visibility - Content \(ACC-VC\) is compatible and can coexist with horizontal IP-based Discovery. You may have ACC installed on a given target host and still have that host as part of a horizontal IP-based Discovery schedule as well.
-   **[Using push-based Discovery and Intel Endpoint Management Assistant \(EMA\) together](using-pushed-based-discovery-and-intel-endpoint-management-assistant-ema-together.md)**  
Agent Client Collector for Visibility - Content \(ACC-VC\) can collect data for uses cases with the Intel vPro® platform when the Intel ® EMA application is installed on Windows endpoints. You can install the Intel EMA application from the ServiceNow store. Attributes are stored in the CMDB when enabled. Currently, data for Intel EMA can only be fetched for Windows endpoints.
-   **[Application patterns for the Agent Client Collector](application-patterns-acc.md)**  
Application patterns gather details on the applications that run on the Agent Client Collector \(ACC\) host. Application patterns are supported only for servers, and are triggered after the Agent Client Collector host Discovery is complete.
-   **[Discovering DNS names using push-based discovery](acc-v-discover-dns-names.md)**  
CMDB owners need CIs to contain all domain system names \(DNS\) associated with their system. Starting in Agent Client Collector for Visibility - Content \(ACC-VC\) version 2.3.0, ACC-VC can discover DNS name lists for Windows and Linux CIs.
-   **[Detecting portable applications using push-based discovery](acc-v-detect-portable-apps.md)**  
Portable applications are those applications that don’t need to be installed on the target system. Starting in ACC-VC version 2.3.0, push-based Discovery can detect portable applications, such as Firefox, VLC, Notepad++ etc, for Windows only.
-   **[Setting exclusion lists for IPs and NICs](acc-v-set-exclusion-lists-for-ips-and-nics.md)**  
Agent Client Collector for Visibility - Content \(ACC-VC\) version 1.3.0 supports exclusion list for IPs and Network Interface Controllers \(NICs\) with a flexible mechanism for filtering out values for IPs and or NICs when creating or updating the host CI and related items.
-   **[Populating Assigned To attribute in Computer CI for Agent Client Collector for Visibility - Content](../task/fetching-logged-in-user-information-for-acc-v.md)**  
To update the Assigned To attribute of the Computer CI, you need to collect information from the logged in user.
-   **[Populating users based on type for Agent Client Collector for Visibility - Content](../task/filter-list-of-users-for-acc-v.md)**  
You can persist the type of users that populate the CMDB depending on your particular interests. Currently, local and system are supported for Windows, Linux, and macOS.
-   **[Run Certificate Discovery via Agent Client Collector for Visibility - Content](../task/run-cert-discovery-accvc.md)**  
Discover TLS/SSL certificates used by ports running on the agent's server. The Certificate Inventory and Management application uses this information to manage TLS/SSL certificates.
-   **[Cloud Native Operations for Visibility](../../cloud-native-operations-visibility/concept/cnov-landing.md)**  
Cloud Native Operations for Visibility \(CNO for Visibility\) has been renamed Kubernetes Visibility Agent. The term Cloud Native Operations for Visibility has been deprecated.

**Parent Topic:**[Agent Client Collector for Visibility - Content](acc-visibility-landing-page.md)

