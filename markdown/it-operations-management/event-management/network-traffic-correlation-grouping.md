---
title: Network traffic based alert grouping
description: The Network traffic based alert grouping method groups alerts by analyzing network traffic connections between processes across hosts. It leverages service candidates identified by ML Service Mapping to group alerts related to network traffic issues. This ensures alerts from directly connected processes within the same service candidate are grouped together, offering a more contextual view of network incidents.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Network traffic based alert grouping

The Network traffic based alert grouping method groups alerts by analyzing network traffic connections between processes across hosts. It leverages service candidates identified by ML Service Mapping to group alerts related to network traffic issues. This ensures alerts from directly connected processes within the same service candidate are grouped together, offering a more contextual view of network incidents.

Service candidates are potential collections of processes within your IT environment that are identified based on their network connections and interactions. They represent different services or functions that your IT systems provide, even if they are not fully detailed in your system’s configuration database. For example, service candidates might group together all the processes involved in email delivery, even if the configuration details are incomplete.

ML Service Mapping uses machine learning to automatically discover and map out these service candidates. It identifies how different processes and components are connected and grouped together based on their network traffic and interactions. This helps in understanding and organizing the IT services and their components, making it easier to manage and troubleshoot issues. For example, ML Service Mapping might automatically identify and map the connections between email servers and mail clients based on their network interactions.

**Note:** Network traffic based alert grouping is enabled for new customers starting with the Zurich release. Existing customers need to enable the property Enable Network Traffic correlation \(**sa\_analytics.agg.query\_network\_traffic\_correlation\_enabled**\) manually.

## How it works

-   Host identification: Alerts related to network issues are generated from various sources.
-   Network context identification: The correlation process uses horizontal discovery results and ML Service Mapping to identify the most relevant service candidates and network connections.

    This process uses the results of the scheduled job **Event Management - Populate Service candidate process to process mapping - Daily**, which runs once a day and is used to store process-to-process connections for Host CIs in the format required by the alert grouping algorithm.

-   Alert grouping: Alerts are grouped based on direct process-to-process connections within the context of the same service candidate. Grouping is updated in real-time as new alerts are received.

## Benefits

-   Improved accuracy: By leveraging network traffic connections and service candidates, this method provides high accuracy in grouping alerts, minimizing false positives.
-   Enhanced coverage: It effectively groups alerts even in environments with low CMDB maturity, covering a broader range of alerts and issues.
-   Streamlined resolution: IT teams can quickly identify and resolve related issues in bulk, reducing the volume of alerts to manage and improving operational efficiency.

