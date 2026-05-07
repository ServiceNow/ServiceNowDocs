---
title: Exploring Now Assist for CMDB
description: With the Now Assist for Configuration Management Database \(CMDB\) application, you can use Agentic AI to search the CMDB, summarize discovery, ownership and related information for a CI, and fix failed SGC import sets. You can also follow step-by-step guidance to help you remediate duplicate CIs, improve CMDB data accuracy, completeness, and health .
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring Now Assist for CMDB

With the Now Assist for Configuration Management Database \(CMDB\) application, you can use Agentic AI to search the CMDB, summarize discovery, ownership and related information for a CI, and fix failed SGC import sets. You can also follow step-by-step guidance to help you remediate duplicate CIs, improve CMDB data accuracy, completeness, and health .

## Now Assist for CMDB agentic workflows

Now Assist for CMDB provides the following abilities:

-   **Create configuration item agentic workflow**

    Occasionally, you might create a CI manually. To help you, the Create configuration item agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow ensures that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI.

    The Create configuration item agentic workflow is particularly useful for adding CIs to tables accessed by Operational Technology because users might add physical CIs while unaware of the importance of managing CI data in the CMDB.

    To learn more, see [Create a CI using Now Assist](../../now-assist-cmdb/task/na-cmdb-awf-ci-creator.md).

-   **Provide advice on CMDB governance agentic workflow**

    Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to help users to trust the data that they use for their work.

    To learn more, see [Getting advice from Now Assist on CMDB governance](../../now-assist-cmdb/concept/na-cmdb-awf-governance.md).

-   **Search CMDB agentic workflow**

    The Search CMDB agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then, depending on the information you provided, generates a keyword search, a single-table search with dot walks, or a multi-table search that involves relationship navigation. The workflow can infer CI relationship data to generate an appropriate query.

    To learn more, see [Use Now Assist to search the CMDB](../../now-assist-cmdb/task/na-cmdb-awf-search.md).

-   **Duplicate CI remediator agentic workflow**

    The Duplicate CI remediator agentic workflow completes the full range of de-duplication tasks. The workflow presents its reasoning for each step so CMDB administrators can review the AI recommendations, modify the remediation actions if needed, and then perform the de-duplication tasks.


## Now Assist for CMDB skills

-   **Manage duplicate CIs skill**

    Duplicate CIs interfere with the integrity, reliability, and general health of CMDB. Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template. The manage duplicate CIs skill accelerates the work that you normally perform manually.

    In this example, the manage duplicate CIs skill presents a list of classes with duplicate CIs and suggests possible actions. You can select an option or enter the action text in your own words:

    -   Review de-duplication tasks, create de-duplication templates, assign tasks to templates, and run the templates.
    -   Preview the results of applying a de-duplication template before you decide to apply it.
    -   Identify the root cause of duplications so that you can review the groups of de-duplication tasks that share a common cause and possibly avoid the issue in the future.
    ![Selecting duplicate CIs to remediate.](../../now-assist-cmdb/image/na-cmdb-mng-dupe-cis-example.png)

    To learn more, see [Let Now Assist help you to manage duplicate CIs](../task/now-assist-cmdb-mng-dupe-cis-skill.md).

-   **CI summarization skill**

    View a concise summary of key CI data. You can select the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of. Summary information is useful while working in applications such as Incident Management, Change Management, and Event Management.

    ![Summary information.](../../now-assist-cmdb/image/na-cmdb-ci-summary-example.png)

    To learn more, see [View CI information with the Now Assist CI summarization skill](../../now-assist-cmdb/task/na-cmdb-agent-ci-summarizer.md).

-   **Service Graph Connector diagnosis**

    Service Graph Connectors are integrations that facilitate data ingestion from third-party sources into the CMDB. Errors in Service Graph Connectors can disrupt the flow of configuration item \(CI\) data resulting in inconsistencies between the actual state of CIs and their CMDB records.

    The Service Graph Connector diagnosis skill automates error diagnosis and recommendation generation, enabling CMDB installation administrators to identify and resolve the issues. This automation reduces manual effort and saves time in debugging Service Graph Connectors issues.

    To learn more, see the following topics:

    -   [Fix SGC import set issues with the Now Assist SGC diagnosis skill](../task/now-assist-cmdb-sgc-diagnose.md)
    -   [Getting started with Service Graph Connectors](cmdb-sgc-intro.md)
    -   [Learn how IRE detects duplicate CIs and creates de-duplication tasks](id-detect-dup-ci.md)
    -   [Learn how CMDB Health uses the duplicate metric to track duplicate CIs](../reference/r_CMDBHealthMetrics.md).
    -   [Learn how to manage and remediate de-duplication tasks by using de-duplication templates in CMDB Workspace](de-duplication-tasks.md).

-   **[Supporting information for Now Assist for CMDB](now-assist-cmdb-supporting-info.md)**  
Get a quick overview of the important information that is related to the Now Assist for CMDB application.

**Parent Topic:**[Now Assist for Configuration Management Database \(CMDB\)](now-assist-landing-cmdb.md)

