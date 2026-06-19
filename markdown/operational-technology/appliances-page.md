---
title: Appliances page
description: The Appliances page displays active appliances in the Discovery Console for OT.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/appliances-page.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: concept
last_updated: "2026-04-07"
reading_time_minutes: 1
breadcrumb: [Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Appliances page

The Appliances page displays active appliances in the Discovery Console for OT.

## Appliances

The Appliances page displays the current Sensors and Collectors that have run or are running your queries. The information displayed includes the following:

-   Name
-   Type
-   Endpoint
-   Status
-   Queue
-   CPU
-   Configuration Status
-   Update Available?

\[Omitted image "appliances-page.png"\] Alt text: Appliances page

Selecting the appliance name in the list, opens its record. See [Edit an Appliance record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/edit-appliance-record.md) for more information.

## Search by type

You can search for a type of appliance by entering the type in the Search field. Or you can open the Filter and select by the available labels. For example, if you want to view just the Collectors, you can type Collector in the Search field or check the box next to Type in the filter and then choose Collector. The Appliances list now shows only the current Collectors.

\[Omitted image "appliances-sort-collector.png"\] Alt text: Sort Collectors

## Using Appliances in Queries

The Discovery Sensor for OT executes the query to discovery assets and creates the OT environment inventory. The OT Discovery Collector is used to discover assets within segments of the OT network where a Sensor can't reach. It is deployed deep within the network zones in your OT environment.

When you create an Auto Query in the Console, you can choose specific Appliances in the Assets section. When choosing Assets for the query, you can assign the Target to all appliances, specific appliances, or auto targeting. If you select **Specific Appliances**, you can select the appliances you want from a provided list. One restriction is that you must select at least one Sensor from the list as well.\[Omitted image "use-appliances-create-auto-query.png"\] Alt text: Select Assets and Targets

For more information on Auto Queries and creating an Auto Query, see [Auto Query page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/auto-query-console.md) and [Create an Auto Query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/add-auto-query-console.md).

