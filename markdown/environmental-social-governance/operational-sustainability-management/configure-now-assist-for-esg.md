---
title: Configure Now Assist for Operational Sustainability \(formerly ESG\)
description: If you have the admin role, you can configure the Now Assist for Operational Sustainability application so that your users can use the generative AI skills in the Operational Sustainability Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/operational-sustainability-management/configure-now-assist-for-esg.html
release: australia
product: Operational Sustainability Management
classification: operational-sustainability-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [Now Assist, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Configure Now Assist for Operational Sustainability \(formerly ESG\)

If you have the admin role, you can configure the Now Assist for Operational Sustainability application so that your users can use the generative AI skills in the Operational Sustainability Workspace.

## Now Assist for Operational Sustainability Configuration overview

Use the Now Assist Admin console to configure Now Assist for Operational Sustainability. This console contains everything that you must install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configuring-now-assist.md).

You can access the **Document Intelligence for Utility Invoices** skill from the Now Assist Admin console.

**Note:** Now LLM Service is the only provider for this Now Assist application's skills.

For earlier versions, go to [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/application-manager.md) to upgrade it to a later version.

## Now Assist for Operational Sustainability plugins

You can install the Now Assist for Operational Sustainability plugin \(com.sn\_esg\_gen\_ai\). This store app has the following dependencies:

-   Now Assist Platform
-   Environmental, Social, Governance Management

For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md).

**Note:** For more information on Retrieval Augmented Generation \(RAG\) and Retention policies, see [Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/indexed-sources-ais.md) and [User data usage policy for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/user-data-usage-policy-now-assist.md).

-   **[Activate the document intelligence for utility invoices skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/activate-the-document-intelligence-for-utility-invoices-skill.md)**  
Activate and then configure document intelligence for utility invoices skill from Now Assist to automate the extraction of metrics data from utility invoices. Once activated, map the extracted data to the correct metric definitions and entities.
-   **[Activate carbon calculations agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/activate-carbon-calculations-agentic-workflow.md)**  
Configure and activate the carbon calculation workflow that uses AI agents and tools. It automates the creation of calculated metric definition \(CMD\) records and formulas for Scope 3 carbon emissions.

**Parent Topic:**[Now Assist for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/now-assist-for-esg.md)

