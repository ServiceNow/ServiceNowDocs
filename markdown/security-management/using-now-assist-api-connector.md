---
title: Creating an API connector with generative AI
description: Developers can use the SPC Setup Connector generative AI skill to help them quickly and automatically create an API connector that they can publish. Use the connector in the Security Posture Control workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/using-now-assist-api-connector.html
release: zurich
topic_type: concept
last_updated: "2026-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Creating an API connector with generative AI

Developers can use the SPC Setup Connector generative AI skill to help them quickly and automatically create an API connector that they can publish. Use the connector in the Security Posture Control workspace.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see .

At a minimum, either Now Assist for Vulnerability Response \(starting with Zurich Patch 4 - Patch 11 and Australia Patch 1- Patch 4\) or ServiceNow Otto for Unified Security Exposure Management \(starting with Zurich patch 12 and Australia Patch 5\) is required if you want to use the SPC Setup Connector with the API Connector builder. See [ServiceNow Otto for Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/now-assist-for-vulnerability-response-vr/now-assist-for-usem-landing-ties.md) for more information.

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

You can use Now Assist to help you automatically complete the following steps in the Connector builder in the Security Posture Control workspace.

-   [Select template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/spc-sgc-template-stepper-3.md) \(Step 3\)- A template is selected to support your API's structure based on vendor documentation that you provide.
-   [Provide inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/spc-sgc-template-stepper-4.md) \(Step 4\)- Input parameters are provided, the connection is tested, and a sample response is generated based on the vendor documentation that you provide.
-   [Map response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/spc-sgc-stepper-5.md) \(Step 5\)- Mapping the sample response parameters to SPC attributes and policies is provided.

Complete steps 1-2 manually to enter connector metadata and credentials in the Connector builder in the Security Posture Control workspace before invoking the SPC Setup Connector Now Assist skill for steps 3-5.

See [Creating your own API connectors in Security Posture Control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/spc-creating-sgc-template.md) for more information about completing the first two steps manually in the Connector builder.

See [Create an API connector with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/select-api-template.md) for the steps in the Connector builder that use ServiceNow Otto for Unified Security Exposure Management.

-   **[Create an API connector with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/select-api-template.md)**  
Use the SPC Setup Connector skill to automatically complete configuration steps 3-5 in the Connector builder in the Security Posture Control Workspace.

**Parent Topic:**[Using Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/using-unified-security-exposure-management.md)

