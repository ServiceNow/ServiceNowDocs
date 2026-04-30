---
title: Exploring Now Assist for Configuration Management Database \(CMDB\)
description: With the Now Assist for Configuration Management Database \(CMDB\) application, you can use generative AI to summarize the discovery and ownership details and related information for a configuration item \(CI\). Now Assist for CMDB can also generate step-by-step guidance to help you remediate duplicate CIs.
locale: en-US
release: xanadu
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring Now Assist for Configuration Management Database \(CMDB\)

With the Now Assist for Configuration Management Database \(CMDB\) application, you can use generative AI to summarize the discovery and ownership details and related information for a configuration item \(CI\). Now Assist for CMDB can also generate step-by-step guidance to help you remediate duplicate CIs.

## Supporting information for Now Assist for CMDB

Now Assist for CMDB is supported starting with Xanadu patch 3.

Now Assist for SGC supports the following LLM models:

-   Gemini
-   Claude

## Now Assist for CMDB overview

Now Assist for CMDB provides the following skills:

-   **CI summarization skill**

    View a concise summary of key configuration item \(CI\) data directly on a CI form, in the workspace, or from any list. The summary can include discovery and class details, associated business services, security vulnerabilities, and related records like incidents, alerts, problems, and change requests. Summary information is useful while working in applications such as Incident Management, Change Management, and Event Management.

    The summary includes discovery \(most recent discovery and last discovered time\), ownership, and key related items, such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.

    ![Summary information.](../image/na-cmdb-ci-summary-example.png)

-   **Manage duplicate CIs skill**

    Duplicate CIs interfere with the integrity, reliability, and general health of CMDB. Resolve deduplication tasks with support from Now Assist. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template. The manage duplicate CIs skill accelerates the work that you normally perform manually.

    In this example, the manage duplicate CIs skill presents a list of classes with duplicate CIs and suggests possible actions. You can select an option or enter the action text in your own words:

    -   Review deduplication tasks, create deduplication templates, assign tasks to templates, and run the templates.
    -   Preview the results of applying a deduplication template before you decide to apply it.
    -   Identify the root cause of duplications so that you can review the groups of deduplication tasks that share a common cause and possibly avoid the issue in the future.
    ![Selecting duplicate CIs to remediate.](../image/na-cmdb-mng-dupe-cis-example.png)


## Service Graph Connector diagnosis

Service Graph Connectors are integrations that facilitate data ingestion from third-party sources into the CMDB. Errors in Service Graph Connectors can disrupt the flow of configuration item \(CI\) data resulting in inconsistencies between the actual state of CIs and their CMDB records.

The Service Graph Connector diagnosis skill automates error diagnosis and recommendation generation, enabling CMDB installation administrators to identify and resolve the issues. This automation reduces manual effort and saves time in debugging Service Graph Connectors issues.

To learn more, see [Use Now Assist to diagnose a Service Graph Connector issue](../task/now-assist-sgc-diagnose.md).

## Learn more

-   Learn about the deduplication process in CMDB Workspace. For more information, see [Learn about the deduplication process in CMDB workspace](dedup-ci-exp-cmdb-workspace.md).
-   Learn how IRE detects duplicate CIs and creates deduplication tasks. For more information, see [Learn how IRE detects duplicate CIs and creates deduplication tasks](id-detect-dup-ci.md).
-   Learn how CMDB Health uses the duplicate metric to track duplicate CIs. For more information, see [Learn how CMDB Health uses the duplicate metric to track duplicate CIs](../reference/r_CMDBHealthMetrics.md).
-   Learn how to manage and remediate deduplication tasks by using deduplication templates in CMDB Workspace. For more information, see [Learn how to manage and remediate deduplication tasks by using deduplication templates in CMDB Workspace](de-duplication-tasks.md).

**Related topics**  


[Getting started with Service Graph Connectors](cmdb-sgc-intro.md)

