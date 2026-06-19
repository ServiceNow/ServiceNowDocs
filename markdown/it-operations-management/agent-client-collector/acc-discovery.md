---
title: Agent Client Collector Discovery
description: Discover CIs in your environment by using Agent Client Collector for Visibility - Content \(ACC-VC\) Discovery. ACC-VC works with both horizontal IP-based Discovery, and you can also use push-based Discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-discovery.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-02-01"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Discovery

Discover CIs in your environment by using Agent Client Collector for Visibility - Content \(ACC-VC\) Discovery. ACC-VC works with both horizontal IP-based Discovery, and you can also use push-based Discovery.

-   **[Using push-based Discovery and horizontal IP-based Discovery together](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/using-enhanced-discovery-and-agent-less-discovery-together.md)**  
Discovery performed by Agent Client Collector for Visibility - Content \(ACC-VC\) is compatible and can coexist with horizontal IP-based Discovery. You may have ACC installed on a given target host and still have that host as part of a horizontal IP-based Discovery schedule as well.
-   **[Using push-based Discovery and Intel Endpoint Management Assistant \(EMA\) together](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/using-pushed-based-discovery-and-intel-endpoint-management-assistant-ema-together.md)**  
Agent Client Collector for Visibility - Content \(ACC-VC\) can collect data for uses cases with the Intel vPro® platform when the Intel ® EMA application is installed on Windows endpoints. You can install the Intel EMA application from the ServiceNow store. Attributes are stored in the CMDB when enabled. Currently, data for Intel EMA can only be fetched for Windows endpoints.
-   **[Discovering DNS names using push-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-v-discover-dns-names.md)**  
CMDB owners need CIs to contain all domain system names \(DNS\) associated with their system. Starting in Agent Client Collector for Visibility - Content \(ACC-VC\) version 2.3.0, ACC-VC can discover DNS name lists for Windows and Linux CIs.
-   **[Populating Assigned To attribute in Computer CI for Agent Client Collector for Visibility - Content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/fetching-logged-in-user-information-for-acc-v.md)**  
To update the Assigned To attribute of the Computer CI, you need to collect information from the logged in user.
-   **[Populating users based on type for Agent Client Collector for Visibility - Content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/filter-list-of-users-for-acc-v.md)**  
You can persist the type of users that populate the CMDB depending on your particular interests. Currently, local and system are supported for Windows, Linux, and macOS.
-   **[License key discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/license-key-discovery.md)**  
License key discovery in Agent Client Collector for Visibility - Content automatically collects software license keys from the Windows registry on managed endpoints.

**Parent Topic:**[Agent Client Collector deployment - servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-server-deployment.md)

