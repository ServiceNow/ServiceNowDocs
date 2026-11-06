---
title: Regulatory taxonomy
description: Regulatory taxonomy simplifies identifying necessary changes in a customer's regulatory library by enabling algorithms to match incoming regulatory intelligence to existing content using taxonomy terms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/regulatory-change-management-service-portal/regulatory-taxonomy-overview.html
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Overview of RSS feeds, Integrate, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Regulatory taxonomy

Regulatory taxonomy simplifies identifying necessary changes in a customer's regulatory library by enabling algorithms to match incoming regulatory intelligence to existing content using taxonomy terms.

Regulatory intelligence providers deliver regulatory content in different ways. To match incoming content to the regulatory library in Regulatory Change Management, the application uses taxonomy terms. The providers differ in:

-   Delivery mode: file-based feeds vs. stream-based feeds.
-   Data format: XML, JSON, CSV, and so on.
-   Taxonomy information: contextual metadata added to regulatory intelligence, such as geography, sector, or regulatory body.

**Note:** To integrate with any regulatory intelligence provider, a connector is required to ingest the provider's data. You can use connectors from the ServiceNow Store or build your own.

Some examples of taxonomy are as follows.

-   Geography: Identifies applicable regions, for example, North America, Paris, or New Delhi.
-   Sector: Defines relevant industries, for example, banking, IT, or logistics.
-   Regulatory Body: Lists regulatory organizations, for example, NIST, European Central Bank.

Some vendors include additional categories like regulatory themes or topics.

**Note:** Access to external content requires an end-user license to authorize the credentials granted by technology partners.

## Delivery modes: file-based and stream-based feeds

-   **File-based feeds**

    The provider delivers regulatory content in files at set intervals, and the content is imported in batches.

-   **Stream-based feeds**

    The provider sends regulatory content continuously as changes occur, and the content is ingested as it arrives.


## Process flow

The following steps describe how regulatory intelligence becomes a regulatory alert:

1.  A provider delivers regulatory content through a file-based or stream-based feed.
2.  A connector ingests the content.
3.  Taxonomy terms in the content are mapped to your internal taxonomy.
4.  The mapped content appears as a regulatory alert.

\[Omitted image "creation-of-alerts.png"\] Alt text: Process flow showing four steps: a provider delivers content via feed, a connector ingests the content, terms are mapped to internal taxonomy, and the content appears as a regulatory alert.

## Benefits of mapping taxonomy

Users of Regulatory Change Management often use their own terms for business reasons, creating mismatches between external and internal taxonomies. For example, a vendor may use the term North America while users refer to it as USA and Canada. Similarly, a vendor may use Singapore while users refer to it as Southeast Asia. To align these differences, administrators must manually map external taxonomy terms to their internal taxonomy. This process is known as taxonomy mapping. Regulatory Change Management integrates taxonomy-mapping capabilities to support this alignment.

**Parent Topic:**[RSS feeds overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/regulatory-change-management-service-portal/rss-feeds.md)

**Related topics**  


[Map the taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/regulatory-change-management-service-portal/manage-taxonomy.md)

[Manage the taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/regulatory-change-management-service-portal/manage-taxonomy-using-ws.md)

