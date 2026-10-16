---
title: AI Agent Topology Mapping release notes
description: Version history for the ServiceNow AI Agent Topology Mapping application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-ai-agent-topology-mapping.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Operations Management version history release notes, ServiceNow Store version history release notes]
---

# AI Agent Topology Mapping release notes

Version history for the ServiceNow® AI Agent Topology Mapping application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - October 2026**
    -   New:
        -   Microsoft Foundry \(new\) discovery
            -   Discovers AI Agents, Models, Prompts, and Tags
            -   Creates Product and Asset Models for each discovered item, with AICT populated
            -   Establishes relationships between Agent and Model
        -   Microsoft Foundry Hub discovery
            -   Discovers AI Assistants, Prompts, Models, Hub Projects, and Tags
            -   Creates Product and Asset Models for each discovered item, with AICT populated
            -   Establishes relationships between Assistant and Model, and between Assistant and Hub Project
    -   Changed:
        -   Amazon Bedrock
            -   Version is now populated in the object ID and product instance ID fields
            -   Vendor is populated in AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] and AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]
            -   Manufacturer now populates from the glide.appcreator.company.friendly\_namesystem property instead of a hardcoded value in the AI System Component Product Model \[cmdb\_ai\_system\_component\_product\_model\] and AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\] tables
        -   Microsoft Foundry \(classic\)
            -   Vendor is populated in AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] and AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]
            -   Manufacturer now populates from the glide.appcreator.company.friendly\_namesystem property instead of a hardcoded value in the AI System Component Product Model \[cmdb\_ai\_system\_component\_product\_model\] and AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\] tables
-   **Version 2.1.0 - June 2026**
    -   New:
        -   Discover the following AI models:
            -   Amazon Bedrock AI Foundation Models
            -   Microsoft Foundry Models
-   **Version 2.0.0 - April 2026**
    -   As organizations rapidly embrace AI technologies, the number of AI agents operating across diverse cloud platforms such as Amazon Bedrock, Microsoft Foundry, Google Vertex AI, and others continues to grow. This surge brings new regulatory challenges, with frameworks like the EU AI Act, Colorado AI Act, and Canada’s Artificial Intelligence and Data Act \(AIDA\) requiring greater transparency and oversight of AI agents, including clear tracking of their business ownership.
    -   Leveraging AI Agent Topology Mapping, enterprises can achieve comprehensive visibility into their deployed AI agents across hyperscaler environments. Powered by ITOM discovery technology, this solution systematically collects detailed inventories of AI agents, large language models, and essential system prompts, all of which are crucial for enabling robust AI Control Tower outcomes and meeting compliance obligations.

**Parent Topic:**[ServiceNow Store - IT Operations Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)

