---
title: Regulatory taxonomy overview
description: Regulatory taxonomy simplifies identifying necessary changes in a customer’s regulatory library by enabling algorithms to match incoming regulatory intelligence to existing content using taxonomy terms.
locale: en-US
release: xanadu
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Overview of RSS feeds, Explore, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Regulatory taxonomy overview

Regulatory taxonomy simplifies identifying necessary changes in a customer’s regulatory library by enabling algorithms to match incoming regulatory intelligence to existing content using taxonomy terms.

Regulatory change management products can integrate intelligence data from multiple vendors. However, these vendors differ in:

1.  Delivery mode: File-based feeds vs. stream-based feeds.
2.  Data format: XML, JSON, CSV, and so on
3.  Taxonomy information: Contextual metadata added to regulatory intelligence, such as geography, sector, or regulatory body.

**Note:** To integrate with any regulatory intelligence provider, you need an active subscription and a connector to ingest the provider’s data. You can use connectors from the ServiceNow Store or build your own.

Some examples of taxonomy are as follows.

-   Geography: Identifies applicable regions, for example, North America, Paris, or New Delhi.
-   Sector: Defines relevant industries, for example, Banking, IT, or Logistics.
-   Regulatory Body: Lists regulatory organizations, for example, NIST, European Central Bank.

Some vendors include additional categories like regulatory themes or topics.

**Note:** Access to external content requires an end-user license to authorize the credentials granted by technology partners.

## Benefits of mapping taxonomy

Users of Regulatory Change Management often use their own terms for business reasons, creating mismatches between external and internal taxonomies. For example, the vendor term could be North America while the users may term it as USA and Canada or vendor term could be Singapore and the user term could be Southeast Asia. To ensure accurate mapping, administrators must manually align external taxonomy terms with their internal taxonomy. This process is known as taxonomy mapping. Mapping taxonomies can sometimes be a challenge for many users. Regulatory Change Management provides the ability to integrate taxonomy-mapping capabilities. For more information, refer to [Map the taxonomy](../task/manage-taxonomy.md).

**Parent Topic:**[RSS feeds overview](rss-feeds.md)

