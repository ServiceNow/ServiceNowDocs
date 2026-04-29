---
title: Configure Now Assist for Operational Sustainability \(formerly ESG\)
description: If you have the admin role, you can configure the Now Assist for Operational Sustainability application so that your users can use the generative AI skills in the Operational Sustainability Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [Now Assist, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Configure Now Assist for Operational Sustainability \(formerly ESG\)

If you have the admin role, you can configure the Now Assist for Operational Sustainability application so that your users can use the generative AI skills in the Operational Sustainability Workspace.

## Now Assist for Operational Sustainability Configuration overview

Use the Now Assist Admin console to configure Now Assist for Operational Sustainability. This console contains everything that you must install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-platform/concept/configuring-now-assist.html).

You can access the **Document Intelligence for Utility Invoices** skill from the Now Assist Admin console.

**Note:** Now LLM Service is the only provider for this Now Assist application's skills.

For earlier versions, go to [Application Manager](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/build/applications/reference/application-manager.html) to upgrade it to a later version.

## Now Assist for Operational Sustainability plugins

You can install the Now Assist for Operational Sustainability plugin \(com.sn\_esg\_gen\_ai\). This store app has the following dependencies:

-   Now Assist Platform
-   Environmental, Social, Governance Management

For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-admin/task/install-now-assist-feature-plugins.html).

**Note:** For more information on Retrieval Augmented Generation \(RAG\) and Retention policies, see [Indexed sources in AI Search](https://www.servicenow.com/docs/access?context=indexed-sources-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [User data usage policy for Now Assist](https://www.servicenow.com/docs/access?context=user-data-usage-policy-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   **[Activate the document intelligence for utility invoices skill](activate-the-document-intelligence-for-utility-invoices-skill.md)**  
Activate and then configure document intelligence for utility invoices skill from Now Assist to automate the extraction of metrics data from utility invoices. Once activated, map the extracted data to the correct metric definitions and entities.
-   **[Activate carbon calculations agentic workflow](../task/activate-carbon-calculations-agentic-workflow.md)**  
Configure and activate the carbon calculation workflow that uses AI agents and tools. It automates the creation of calculated metric definition \(CMD\) records and formulas for Scope 3 carbon emissions.

**Parent Topic:**[Now Assist for Operational Sustainability \(formerly ESG\)](now-assist-for-esg.md)

