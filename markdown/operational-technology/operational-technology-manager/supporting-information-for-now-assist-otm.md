---
title: Supporting information for OT Manager Foundation
description: Review language model support, user interfaces, and skill availability for the Operational Technology \(OT\) Manager Foundation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-manager/supporting-information-for-now-assist-otm.html
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Configuring the OT Manager Foundation, Configure, Operational Technology Manager, Operational Technology]
---

# Supporting information for OT Manager Foundation

Review language model support, user interfaces, and skill availability for the Operational Technology \(OT\) Manager Foundation.

## Supported language models for all OT Manager Foundation skills and AI agents

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md).

## Supported user interfaces

The OT Manager Foundation includes the features that are listed in the following table.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see .

<table id="table_fc3_kbl_fdc"><thead><tr><th>

Interface

</th><th>

Feature

</th></tr></thead><tbody><tr><td>

Industrial Workspace

</td><td>

-   Operational Technology \(OT\) Configuration Management Database \(CMDB\) search feature to search for OT device records using the ServiceNow Otto panel.

The OT CMDB search feature uses the following agentic workflow and skill:

    -   ServiceNow Otto for CMDB's Search CMDB agentic workflow. For more information, see [Search the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/na-cmdb-awf-search.md).

**Note:** You must have the cmdb\_ot\_viewer role at minimum to use the CMDB search agentic workflow.

    -   ServiceNow AI Platform's Analytics Query Generator skill. For more information, see the [Query Generation store listing](https://store.servicenow.com/store/app/b779efee1be06a50a85b16db234bcb4e#description) and [Query Generation skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/enable-query-generation.md).
-   Agentic workflow for uploading, importing, and validating your OT device data with the Service Graph Connector for Microsoft Excel.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring the OT Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/configuring-na-otm.md)

