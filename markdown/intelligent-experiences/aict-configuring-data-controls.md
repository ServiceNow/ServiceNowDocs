---
title: Configuring data controls
description: Choose whether your instance contributes data that ServiceNow uses to improve its AI products, and whether ServiceNow Otto traffic can move to Microsoft Azure datacenters during traffic spikes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configuring-data-controls.html
release: australia
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring ServiceNow AI settings, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configuring data controls

Choose whether your instance contributes data that ServiceNow uses to improve its AI products, and whether ServiceNow Otto traffic can move to Microsoft Azure datacenters during traffic spikes.

## Data sharing

AI models learn from data. When data sharing is active, ServiceNow collects the inputs, outputs, and edits to outputs of the generative AI capabilities on your instance, along with data used or generated in connection with them, such as the script or record in which a capability is called. ServiceNow uses this data to improve model accuracy and tailor its AI products to business needs.

Personally identifiable information \(PII\) and sensitive data are anonymized and cleansed from any data collected, and ServiceNow doesn't resell or share your data.

Data sharing is active by default. Opting out stops your instance from contributing data, and your instance keeps its access to AI features. Opting out is a one-way change on the instance. To opt back in, you must work with your account executive or Customer Service and Support.

Data sharing isn't enabled on Government Community Cloud \(GCC\) or self-hosted instances, so there's nothing to opt out of on those instances.

## Data overflow processing

ServiceNow Otto traffic is processed in ServiceNow datacenters. To keep performance consistent during traffic spikes, the traffic bursts to Microsoft Azure datacenters. This bursting is called data overflow processing.

Data overflow processing is active by default. If your policies require all traffic to stay in ServiceNow datacenters, you can opt out. Opting out can cause processing delays or capacity overflow errors during high-traffic periods. Unlike data sharing, you can opt back in at any time.

For details on how ServiceNow processes this data, see the [Data Processing FAQ \[KB1584492\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base.

-   **[Opt out of data sharing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configure-opt-out-data-sharing.md)**  
Stop your instance from contributing data that ServiceNow uses to improve its AI models and products.
-   **[Change the data overflow processing setting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configure-data-overflow.md)**  
Keep all ServiceNow Otto traffic in ServiceNow datacenters by opting out of data overflow processing, or opt back in to restore bursting to Microsoft Azure during traffic spikes.

**Parent Topic:**[Configuring ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-servicenow-ai-settings.md)

