---
title: Creating an API connector with generative ai
description: Use the SPC Setup Connector generative AI skill in USEM to help your developers quickly and automatically create an API connector that you can publish and use in the Security Posture Control workspace. This skill automatically selects an API template, populates request and header parameters, and maps sample response attributes to SPC attributes based on API documentation you provide.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/using-now-assist-api-connector.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 2
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Creating an API connector with generative ai

Use the SPC Setup Connector generative AI skill in USEM to help your developers quickly and automatically create an API connector that you can publish and use in the Security Posture Control workspace. This skill automatically selects an API template, populates request and header parameters, and maps sample response attributes to SPC attributes based on API documentation you provide.

To view and use the generative AI skills agentic workflows in the Unified Security Exposure Management you must upgrade to Unified Security Exposure Management. See [Unified Security Exposure Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/release-notes/secops-sem-rn.md) for more information.

You must have Zurich Patch 4 of Now Assist for Vulnerability Response to view the SPC Setup Connector skill.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

You have the option to use Now Assist to help you automatically complete the following steps in the Connector builder in the Security Posture Control workspace.

-   [Select template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/spc-sgc-template-stepper-3.md) \(Step 3\)- A template is selected to support your API's structure based on vendor documentation that you provide.
-   [Provide inputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/spc-sgc-template-stepper-4.md) \(Step 4\)- Input parameters are provided, the connection is tested, and a sample response is generated based on the vendor documentation that you provide.
-   [Map response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/spc-sgc-stepper-5.md) \(Step 5\)- Mapping the sample response parameters to SPC attributes and policies is provided.

You must complete steps 1-2 manually to enter connector metadata and credentials in the Connector builder in the Security Posture Control workspace before you can invoke the SPC Setup Connector Now Assist skill for steps 3-5.

See [Creating your own API connectors in Security Posture Control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/spc-creating-sgc-template.md) for more information about completing the first two steps manually in the Connector builder.

See [Create an API connector with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/select-api-template.md) for the steps in the Connector builder that use Now Assist for Vulnerability Response.

-   **[Create an API connector with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/select-api-template.md)**  
Use the SPC Setup Connector skill to help you automatically complete configuration steps 3-5 in the Connector builder in the Security Posture Control Workspace.

**Parent Topic:**[Using Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/using-unified-security-exposure-management.md)

