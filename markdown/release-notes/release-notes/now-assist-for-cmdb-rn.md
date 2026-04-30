---
title: Now Assist for Configuration Management Database \(CMDB\) release notes
description: The ServiceNow Now Assist for CMDB application displays comprehensive summaries for configuration items \(CIs\) and accelerates the process of remediating duplicate CIs. Now Assist for CMDB was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-02-12"
reading_time_minutes: 4
---

# Now Assist for Configuration Management Database \(CMDB\) release notes

The ServiceNow® Now Assist for CMDB application displays comprehensive summaries for configuration items \(CIs\) and accelerates the process of remediating duplicate CIs. Now Assist for CMDB was enhanced and updated in the Yokohama release.

## Now Assist for CMDB highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   Select **Summarize** on a CI form, in the workspace, or from any list to view a concise summary of key CI data directly on the form: discovery and class details, associated business services, security vulnerabilities, and related records like incidents, alerts, problems, and change requests.
-   The 'Manage duplicate CIs' skill identifies duplicate CIs, populates remediation tasks, and then assigns the tasks to the appropriate group. You follow step-by-step guidance and can preview remediation results before selecting a template. The updated CI correctness scores enable the CMDB Health Dashboard to display accurate information.

See [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

**Important:** Now Assist for CMDB is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Now Assist for CMDB release

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Preview deduplication template results](https://www.servicenow.com/docs/access?context=now-assist-cmdb-mng-dupe-cis-skill&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US#li-preview-template-results)**

    While you're working in the manage duplicate CIs skill, select **Review existing templates** to help you to decide which deduplication template to apply. Now Assist generates a summary of the results of applying a template without actually running the remediation process. You can preview the results for any existing template. When you see the desired result in a preview, you can specify that template and proceed with the deduplication process.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Install Now Assist for CMDB by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Use a Service Graph Connector to import and integrate third-party data into CMDB and non-CMDB tables.

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

