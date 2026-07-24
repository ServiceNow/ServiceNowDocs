---
title: Data center infrastructure allocation placement policies
description: Data center policies and rack policies are stored in the Knowledge Base and are applied to racks during the data center infrastructure allocation process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-allocation-placement-policies.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Data center infrastructure allocation placement policies

Data center policies and rack policies are stored in the Knowledge Base and are applied to racks during the data center infrastructure allocation process.

## Default policies

Data center policies and rack policies are stored as articles in Knowledge Base and are applied to racks during the data center infrastructure allocation process. In the case where both levels of policy exist, rack policies take priority. If no custom policies are defined, built-in default policies apply. These default policies are not editable. You can override them by defining custom policies in the Knowledge Base for your data center or individual racks.

|Parameter|Level|Default|Effect|
|---------|-----|-------|------|
|maxFillPercent|Data center default and per-rack|100|Caps how full a rack can be filled. To allow the rack to be filled up to its full capacity, use the default value of 100. Setting this value to 0 makes the rack unavailable for allocation.|
|reserveRU|Data center default and per-rack|0|Number of rack units kept free. The reserve floor is checked before scoring — racks that cannot meet the reserve requirement are excluded.|
|balanceLoad|Data center default and per-rack|False|When true, the emptiest rack is preferred. When false, the tightest-fit rack is preferred.|
|preferBottomPlacement|Data center default only|True|When true, equipment is placed from the bottom of the rack upward. When false, equipment is placed from the top of the rack downward. This parameter is not honored as a per-rack override.|

## Custom placement policies

Each Knowledge Base article is linked to a configuration item — either a data center or a specific rack. Articles must be published and the latest version to be read by data center infrastructure allocation. Unpublished or non-latest articles are ignored.

Write the recognized parameters in plain language in the article. Data center infrastructure allocation interprets them automatically. Keep articles focused on the following four parameters:

-   **maxFillPercent**
-   **reserveRU**
-   **balanceLoad**
-   **preferBottomPlacement**

To apply different policies to individual racks within the same data center, structure the Knowledge Base article with a default section for data center-wide values and a section that maps individual racks to their overrides using each rack's unique system identifier. To find a rack's system identifier, open the rack record in the CMDB and copy the value from the sys\_id field. A rack override identified by display name or rack number is not applied, and the rack silently falls back to the data center default. Values not listed for a rack fall back to the data center default.

**Note:** Custom policies are optional. Data center infrastructure allocation runs normally with no custom policies defined.

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Data center infra allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/data-center-rack-allocation.md)

[Data center infrastructure allocation failure cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-allocation-failure-cases.md)

[Data center infrastructure rack allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-rack-allocation.md)

