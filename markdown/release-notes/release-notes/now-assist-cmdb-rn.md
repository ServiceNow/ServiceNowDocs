---
title: Now Assist for CMDB release notes
description: The Now Assist for CMDB application enables you to improve the quality of CMDB data, search the CMDB quickly, find and remedy issues with Service Graph Connector import sets, view comprehensive summaries for configuration items \(CIs\), accelerate the process of remediating duplicate CIs, and manually create CIs. Now Assist for CMDB was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-04"
reading_time_minutes: 7
---

# Now Assist for CMDB release notes

The Now Assist for CMDB application enables you to improve the quality of CMDB data, search the CMDB quickly, find and remedy issues with Service Graph Connector import sets, view comprehensive summaries for configuration items \(CIs\), accelerate the process of remediating duplicate CIs, and manually create CIs. Now Assist for CMDB was enhanced and updated in the Zurich release.

## Now Assist for CMDB highlights for the Zurich release

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Get AI-powered answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace.
-   Search queries can now span multiple tables and relationships between CIs.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills and agentic workflows are now turned on by default.
-   Agentic workflows and AI agents included with Now Assist applications now require additional security configuration.
-   Reduce the debugging time and effort when you resolve issues with Service Graph Connector import sets.
-   Find and resolve de-duplication tasks.
-   Speed the process of manually creating CIs.
-   Methodically work through the process of improving CMDB data governance.
-   Search for CIs by specifying any of several attributes of the CI of interest.
-   View a concise summary of the key CI data on a CI form in a workspace page or on any list view.

[Zurich Patch 3](../quality/zurich-patch-3.md)

[Zurich Patch 2](../quality/zurich-patch-2.md)

[Zurich Patch 1](../quality/zurich-patch-1.md)

See [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

**Important:** Now Assist for CMDB is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for CMDB to Zurich

The installation \(activation\) process has changed for the Now Assist for CMDB v2.1 plugin. See [Configuring Now Assist for CMDB](https://www.servicenow.com/docs/access?context=now-assist-cmdb-configuring&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for the new instructions.

## Changed in this release

-   **[View CI attribute descriptions on CI forms](https://www.servicenow.com/docs/access?context=na-cmdb-skill-ci-form-help&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".


-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Create a CI using Now Assist](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Verbal interaction with this feature has improved. Occasionally, you might need to create a CI manually. To help you, the CI creator agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow ensures that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI.

-   **[Getting advice from Now Assist on CMDB governance](https://www.servicenow.com/docs/access?context=na-cmdb-awf-governance&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    To help users understand the value of each step in the process, responses now include richer context. The CMDB Governance agentic workflow supports administrators and service owners by improving CMDB data governance. Before starting in on each governance task, the workflow presents the reasons for the task to help you better understand the importance and benefits of the activity. The objective is to ensure that CMDB data is accurate and complete so that users can trust the data.

-   **[Use Now Assist to search the CMDB for CIs](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Verbal interaction with this feature has improved. Users can now select the CI inline when multiple CIs are returned as matches. A summary of the CI now appears in the conversation. The CMDB search agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then generates a keyword search, a single-table search with dot walks, or a multi-table search, depending on the information that you provided. The workflow can infer CI relationship data to generate an appropriate query.

-   **[View CI information with the Now Assist CI summarization skill](https://www.servicenow.com/docs/access?context=na-cmdb-agent-ci-summarizer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Verbal interaction with this feature has improved. You can now view a concise summary of the key CI data by selecting the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.

-   ****

    Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template.

-   **[Fix SGC import set issues with the Now Assist SGC diagnosis skill](https://www.servicenow.com/docs/access?context=now-assist-sgc-diagnose&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Verbal interaction with this feature has improved. You can now diagnose a failed import set that is associated with a Service Graph Connector to get a summary of the errors and recommendations for resolving the issues.


## Activation information

Now Assist for CMDB is a ServiceNow AI Platform feature that is available with activation of plugins that you get from the ServiceNow Store. For details, see [Configuring Now Assist for CMDB](https://www.servicenow.com/docs/access?context=now-assist-cmdb-configuring&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Use a Service Graph Connector to import and integrate third-party data into CMDB and non-CMDB tables.

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the conversational interface in Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

