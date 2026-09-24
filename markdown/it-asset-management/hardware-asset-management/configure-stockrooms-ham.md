---
title: Configure stockrooms
description: Stockrooms are physical locations where hardware assets are stored before deployment or after return. Configure stockrooms before stockroom technicians begin receiving assets, fulfilling requests, or running inventory audits.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/configure-stockrooms-ham.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Configure stockrooms

Stockrooms are physical locations where hardware assets are stored before deployment or after return. Configure stockrooms before stockroom technicians begin receiving assets, fulfilling requests, or running inventory audits.

Complete the following tasks with the inventory\_admin role to configure a stockroom.

|Configuration task|Purpose|Required|
|------------------|-------|--------|
|[Create a stockroom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/view-create-stockroom.md)|Creates the stockroom record that defines the name, type, and location of the stockroom|Yes|
|[Create a stockroom type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/t_CreateANewStockroomType.md)|Defines a custom stockroom type when default types don't meet your organization's needs|If needed|
|[Create a stock rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/t_CreateAStockRule.md)|Sets minimum and maximum inventory thresholds to trigger automatic replenishment orders|Yes|
|[Associate a stockroom with service locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/associate-stockroom-with-service-locations.md)|Determines which locations the stockroom serves for asset sourcing|Yes|
|[Link stockrooms into a distribution channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/associate-stockroom-with-distribution-channels.md)|Controls automated stockroom selection when fulfilling asset requests|Yes|
|[Configure stockroom auto-sourcing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/configure-stockroom-auto-sourcing.md)|Enables AI agents to source hardware assets automatically from the stockroom|If using agentic workflow for sourcing hardware requests|
|[Remove service locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/remove-service-locations.md)|Removes service locations that the stockroom no longer supports|If needed|
|[Exclude a stockroom from service locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/exclude-stockroom-from-service-locations.md)|Prevents a stockroom from appearing in the Stockrooms missing service locations actions card in the Inventory view|If needed|
|[Exclude a stockroom from distribution channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/exclude-stockroom-from-distribution-channel.md)|Prevents a stockroom from appearing in the Stockrooms missing distribution channels actions card in the Inventory view|If needed|
|[Delete a stockroom with assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/t_DeleteAStockroomWithAssets.md)|Removes a stockroom record that contains assets|Only when removing a stockroom|
|[Delete a stockroom with no assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/t_DeleteAStockroomWithNoAssets.md)|Removes a stockroom record with no remaining assets|Only when removing a stockroom|

-   **[Create a stockroom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/view-create-stockroom.md)**  
Create stockrooms to assign places to assets.
-   **[Create a stockroom type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/t_CreateANewStockroomType.md)**  
If you need stockroom types that are not included in the base system, you can create a custom stockroom type.
-   **[Create a stock rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/t_CreateAStockRule.md)**  
Create a stock rule to control what happens when the inventory of a particular asset in a particular stockroom reaches a specified threshold.
-   **[Associate a stockroom with service locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/associate-stockroom-with-service-locations.md)**  
Manage sourcing requests that consume from local stockrooms effectively by associating your stockroom with multiple service locations. Optimize your loaner asset workflow and automated asset tasks by serving multiple locations using a single stockroom.
-   **[Link stockrooms into a distribution channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/associate-stockroom-with-distribution-channels.md)**  
Link two geographically related stockrooms to create a distribution channel and make the distribution of assets more efficient. You can assign a preference order for each channel to source assets to the stockroom.
-   **[Configure a stockroom for automated sourcing by AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/configure-stockroom-auto-sourcing.md)**  
Configure a stockroom to enable AI agents in the Manage hardware asset requests agentic workflow to source hardware assets automatically.
-   **[Remove service locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/remove-service-locations.md)**  
Remove service locations when the associated stockroom doesn't support those locations.
-   **[Exclude a stockroom from service locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/exclude-stockroom-from-service-locations.md)**  
Exclude a stockroom from service locations so that the stockroom isn't shown in the Stockrooms missing service locations important actions card in the Inventory view.
-   **[Exclude a stockroom from distribution channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/exclude-stockroom-from-distribution-channel.md)**  
Exclude a stockroom from distribution channels so that the stockroom isn't shown in the Stockrooms missing distribution channels important actions card in the Inventory view.
-   **[Delete a stockroom with assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/t_DeleteAStockroomWithAssets.md)**  
You can delete a stockroom. If the stock room has assets, you must remove the assets from the stockroom first.
-   **[Delete a stockroom with no assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/t_DeleteAStockroomWithNoAssets.md)**  
You can delete a stockroom that has no assets.

**Parent Topic:**[Configuring Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/configuring-ham.md)

