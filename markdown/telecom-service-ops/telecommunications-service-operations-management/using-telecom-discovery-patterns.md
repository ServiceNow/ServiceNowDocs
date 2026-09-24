---
title: Use Telecom Discovery patterns
description: Use Telecom Discovery patterns to identify and classify network functions \(xNFs\) from vendor devices such as Cisco, Juniper, routers, or switches. Use pattern-based discovery to map telecom resources into the CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/using-telecom-discovery-patterns.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use, Telecommunications Service Operations Management]
---

# Use Telecom Discovery patterns

Use Telecom Discovery patterns to identify and classify network functions \(xNFs\) from vendor devices such as Cisco, Juniper, routers, or switches. Use pattern-based discovery to map telecom resources into the CMDB.

Telecom Discovery Patterns automatically classify some discovered network attributes into standardized CMDB values, so that patterns from different vendors produce consistent CI data.

## Port bandwidth classification

When a Telecom Discovery pattern discovers a network interface \(port\), it uses the reported bandwidth to automatically assign an interface hardware model to the **Model ID** field. The assignment is based on the following fixed set of bandwidth values:

|Discovered bandwidth|Assigned interface model|
|--------------------|------------------------|
|100000|100 GigabitEthernet|
|40000|40 GigabitEthernet|
|25000|25 GigabitEthernet|
|10000|10 GigabitEthernet|
|1000|GigabitEthernet|
|10–100|FastEthernet|
|0|1/10/25G Ethernet|

A bandwidth value of **0** is not treated as "no bandwidth" or an error—it resolves to the **1/10/25G Ethernet** model. A discovered bandwidth that doesn't match any value in this table is left without a model assignment.

**Note:** The interface model is only assigned if a matching Product Model \(`cmdb_model`\) record already exists in your instance. If the corresponding model record is missing, the Model ID field is left blank even for a recognized bandwidth value.

-   **[Classify xNFs for Telecom Router Pattern](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/classifying-xnfs-pattern-tsom-visibility.md)**  
To access a full list of OIDs that will be classified.
-   **[Classify xNFs for Telecom Cisco 7613 Router Pattern](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/classifying-xnfs-telecom-cisco.md)**  
To access a full list of OIDs that will be classified.
-   **[Classify xNFs for Telecom Juniper MX SSH Router Pattern](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/classifying-xnfs-juniper-router-pattern.md)**  
To access a full list of OIDs that will be classified.
-   **[Classify xNFs for Telecom Cisco Switch Pattern](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/classifying-xnfs-cisco-switch-pattern.md)**  
To access a full list of OIDs that will be classified.
-   **[Classify xNFs for Telecom Switch Pattern](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/classifying-xnfs-pattern-switch-pattern.md)**  
To access a full list of OIDs that will be classified.

**Parent Topic:**[Using Telecommunications Service Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/using-tsom.md)

