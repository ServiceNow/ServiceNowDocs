---
title: Telecom Customer Enterprise Graph
description: The Telecom Customer Enterprise Graph connects telecom customer and service data to provide context for AI agents in the Smart Actions for Telecom agentic workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-telecom-customer-enterprise-graph.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-07-31"
reading_time_minutes: 1
keywords: [telecom customer enterprise graph, knowledge graph, enterprise graph tag, AI agent context, customer service data]
breadcrumb: [Smart Actions for Telecom, Use agentic workflows, ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# Telecom Customer Enterprise Graph

The Telecom Customer Enterprise Graph connects telecom customer and service data to provide context for AI agents in the Smart Actions for Telecom agentic workflow.

## Telecom Customer Enterprise Graph overview

The Telecom Customer Enterprise Graph is an enterprise graph tag available in the Knowledge Graph Designer. It connects account and consumer records to their associated contacts, products, services, incidents, work orders, and billing data.

The Smart Actions for Telecom agentic workflow uses this graph to enrich customer context at runtime. When the workflow runs, it queries the graph to retrieve service-related data such as service problem cases and sold product details.

You can use the Telecom Customer Enterprise Graph as a starting point for your own knowledge graph. To add tables, modify paths, or create a custom graph tag based on this one, see [Using Knowledge Graph Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/using-knowledge-graph-designer.md).

## Tables tagged in the Telecom Customer Enterprise Graph

|Table|Description|
|-----|-----------|
|Customer Account \[customer\_account\]|Account record that serves as the entry point for account-based queries. Links to contacts, products, and cases.|
|Consumer \[csm\_consumer\]|Consumer record that serves as the entry point for consumer-based queries. Operates independently from the account chain with no shared traversal path.|
|Customer Contact \[customer\_contact\]|Contacts associated with the account, including name and email.|
|Customer Service Case \[sn\_customerservice\_case\]|Customer service cases opened for the account or consumer.|
|Service Problem Case \[sn\_sprb\_mgmt\_case\]|Service problem cases — a specialized case type that extends Customer Service Case \[sn\_customerservice\_case\].|
|Incident \[incident\]|Incidents associated with the customer's configuration items.|
|Work Order \[wm\_order\]|Work orders associated with the customer's configuration items.|
|Configuration Item \[cmdb\_ci\]|Configuration items that link the account or consumer to their associated incidents and work orders.|
|Sold Product \[sn\_install\_base\_sold\_product\]|Products sold to the account or consumer.|
|Installed Product Junction \[sn\_install\_base\_m2m\_installed\_product\]|Junction record linking a sold product to its corresponding installed asset.|
|Installed Asset \[sn\_install\_base\_item\]|The physical or logical items that a sold product resolves to.|
|Product Inventory \[sn\_prd\_invt\_product\_inventory\]|Product inventory records that extend the Sold Product \[sn\_install\_base\_sold\_product\].|

**Related topics**  


[ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) Smart Actions for Telecom agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-smart-actions-agentic-workflow.md)

