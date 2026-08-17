---
title: Configure ServiceNow Otto for Operational Sustainability
description: If you have the admin role, you can configure the ServiceNow Otto for Operational Sustainability application so that your users can use the generative AI skills in the Operational Sustainability Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/configure-now-assist-for-esg.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [ServiceNow Otto, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Configure ServiceNow Otto for Operational Sustainability

If you have the admin role, you can configure the ServiceNow Otto for Operational Sustainability application so that your users can use the generative AI skills in the Operational Sustainability Workspace.

## ServiceNow Otto for Operational Sustainability Configuration overview

Use the AI Admin Hub console to configure ServiceNow Otto for Operational Sustainability. This console contains everything that you must install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

You can access the **Document Intelligence for Utility Invoices** skill from the AI Admin Hub console.

**Note:** Now LLM Service is the only provider for this Now Assist application's skills.

For earlier versions, go to [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager.md) to upgrade it to a later version.

## ServiceNow Otto for Operational Sustainability plugins

You can install the ServiceNow Otto for Operational Sustainability plugin \(com.sn\_esg\_gen\_ai\). This store app has the following dependencies:

-   ServiceNow Otto for Platform
-   Operational Sustainability Management

For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

**Note:** For more information on Retrieval Augmented Generation \(RAG\) and Retention policies, see [Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/indexed-sources-ais.md) and [User data usage policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/user-data-usage-policy-now-assist.md).

-   **[Activate the document intelligence for utility invoices skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/activate-the-document-intelligence-for-utility-invoices-skill.md)**  
Activate and then configure document intelligence for utility invoices skill from Now Assist to automate the extraction of metrics data from utility invoices. Once activated, map the extracted data to the correct metric definitions and entities.
-   **[Activate carbon calculations agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/activate-carbon-calculations-agentic-workflow.md)**  
Configure and activate the carbon calculation workflow that uses AI agents and tools. It automates the creation of calculated metric definition \(CMD\) records and formulas for Scope 3 carbon emissions.

**Parent Topic:**[ServiceNow Otto for Operational Sustainability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/now-assist-for-esg.md)

