---
title: AI Service Graph Connector for Amazon release notes
description: Version history for the ServiceNow AI Service Graph Connector for Amazon application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-ai-sgc-amazon.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# AI Service Graph Connector for Amazon release notes

Version history for the ServiceNow® AI Service Graph Connector for Amazon application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 2.1.9 - September 2026**
    -   New:
        -   Certificate-based authentication support to reduce reliance on client secrets and access keys, especially for enterprise customers with stricter security requirements.
        -   Tenant-wide discovery support for discovering AI assets across an entire enterprise environment rather than requiring resource-by-resource configuration.
-   **Version 2.1.2 - August 2026**
    -   New:
        -   Admins can now configure all AWS AI discovery services using a single credential page. The playbook presents one unified configuration page for Bedrock, SageMaker, and AgentCore, creating a single connection alias reused across all services. Discovery runs successfully for all services using the shared connection, and existing separate configurations remain supported. A new connection alias and template are created, acting as the parent for all connection aliases.
        -   Admins can enable automatic rotation of AWS access keys for AI SGC connections. When enabled, a scheduled job periodically rotates IAM access keys for Bedrock, SageMaker, AgentCore, and CloudWatch connections, updating credentials and tracking rotation status per connection.
        -   Admins can discover multiple explicit AWS accounts by specifying a comma-separated list of account IDs. The connection property now supports multiple account IDs, allowing discovery across all listed accounts without using Organizations ListAccounts. Each account is discovered individually, and accounts missing the required role are skipped and logged.
    -   Changed:
        -   The playbook connection form UI has been improved. Field hints and activity descriptions are updated for clarity, and service names are revised for consistency. The scheduled imports page now covers all connections.
        -   The connection property for standalone AWS account discovery has been renamed. The property is now called "Target Account IDs" and supports comma-separated values. Existing connections using the legacy property remain compatible and display the value in the updated form.
        -   The script execution step is moved to setup instructions KB in Review step of playbook. The script download is available through the setup instructions KB in prerequisites section and its execution process.
-   **Version 1.2.1 - June 2026**

    New: Tenant Wide Discovery support

-   **Version 1.0.6 - April 2026**
    -   Integration with Amazon which would allow discovery and inventory of Workflows with AI Agents,related models, prompts, and toolinformation across Amazon Bedrock, Amazon Bedrock Agentcore, Amazon Sagemaker.
    -   The AI Control Tower \(AICT\) imports the discovered artifacts into its AI inventory, where the AI steward and Product Owner can access and review them.
-   **Version 1.0.4 - March 2026**

    This integration connects AI Control Tower’s AI Discovery capabilities with Amazon Bedrock, Amazon Bedrock Agentcore, Amazon Sagemaker, enabling automated discovery and governance of AI assets across enterprise Amazon environment


**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

