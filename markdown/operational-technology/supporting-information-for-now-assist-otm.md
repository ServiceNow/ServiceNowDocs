---
title: Supporting information for the OT Manager Foundation
description: Get a quick overview of the important information that is related to the Operational Technology \(OT\) Manager Foundation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, OT Manager Foundation, Operational Technology]
---

# Supporting information for the OT Manager Foundation

Get a quick overview of the important information that is related to the Operational Technology \(OT\) Manager Foundation.

## Supported language models for all OT Manager Foundation skills and AI agents

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Supported user interfaces

The OT Manager Foundation includes the features that are listed in the following table.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

<table id="table_fc3_kbl_fdc"><thead><tr><th>

Interface

</th><th>

Feature

</th></tr></thead><tbody><tr><td>

Industrial Workspace

</td><td>

-   Operational Technology \(OT\) Configuration Management Database \(CMDB\) search feature to search for OT device records using the Now Assist panel.

The OT CMDB search feature leverages the following agentic workflow and skill:

    -   Now Assist for CMDB's Search CMDB agentic workflow. For more information, see [Use Now Assist to search the CMDB](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Note:**

You must have the **cmdb\_ot\_viewer** role at minimum to use the CMDB search agentic workflow.

    -   ServiceNow AI Platform's Analytics Query Generator skill. For more information, see the [Query Generation store listing](https://store.servicenow.com/store/app/b779efee1be06a50a85b16db234bcb4e#description) and [Query Generation skills](https://www.servicenow.com/docs/access?context=enable-query-generation&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).
-   Agentic workflow for uploading, importing, and validating your OT device data with the Service Graph Connector for Microsoft Excel.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring the OT Manager Foundation](configuring-na-otm.md)

