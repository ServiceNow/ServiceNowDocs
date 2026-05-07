---
title: Using agentic workflows in Now Assist for CMDB
description: Users with the sn\_cmdb\_user role can access several Now Assist for CMDB agentic workflows.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Using agentic workflows in Now Assist for CMDB

Users with the sn\_cmdb\_user role can access several Now Assist for CMDB agentic workflows.

## Agentic workflows

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

<table id="table_lxk_lck_h2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Create configuration item

</td><td>

Occasionally, you might create a CI manually. To help you, the Create configuration item agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow ensures that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI. For more information, see [Create a CI using Now Assist](../../now-assist-cmdb/task/na-cmdb-awf-ci-creator.md)

</td><td>

CI creator

</td></tr><tr><td>

Provide advice on CMDB governance

</td><td>

Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to help users to trust the data that they use for their work. For more information, see [Getting advice from Now Assist on CMDB governance](../../now-assist-cmdb/concept/na-cmdb-awf-governance.md).

</td><td>

-   CMDB data manager
-   CMDB data certification and attestation manager
-   CMDB data ownership manager
-   CMDB health metrics manager
-   CMDB life cycle manager
-   CMDB principal class manager

</td></tr><tr><td>

Search CMDB

</td><td>

The Search CMDB agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then, depending on the information you provided, generates a keyword search, a single-table search with dot walks, or a multi-table search that involves relationship navigation. The workflow can infer CI relationship data to generate an appropriate query. For more information, see [Use Now Assist to search the CMDB](../../now-assist-cmdb/task/na-cmdb-awf-search.md).

</td><td>

CI search

</td></tr><tr><td>

Remediate duplicate CIs

</td><td>

The Duplicate CI remediator agentic workflow completes the full range of de-duplication tasks. The workflow presents its reasoning for each step so CMDB administrators can review the AI recommendations, modify the remediation actions if needed, and then perform the de-duplication tasks.

</td><td>

 

</td></tr></tbody>
</table>## AI agents used by Now Assist for CMDB

-   **CI creator AI agent**

    The CI creator AI agent creates a new configuration item \(CI\) record in the CMDB.

-   **Configuration item summarizer Al agent**

    Given a CMDB \(Configuration Management Database\) record GUID or' sys\_id" summarize the Cl using an existing skill.

-   **CMDB data certification and attestation manager AI agent**

    The CMDB data certification and attestation manager AI agent retrieves the data certification and attestation policies for a CI class and for similar classes. It can also create a data certification and an attestation policy. For more information, see [Data Certification](../../data-certification/concept/c_DataCertification.md).

-   **CMDB data manager AI agent**

    The CMDB life cycle manager AI agent helps admins to confirm that CMDB life-cycle policies are in place for principal classes or for specified classes. For more information, see [Working with CMDB Data Manager](cmdb-data-management.md).

-   **CMDB data certification and attestation manager AI agent**

    The CMDB data certification and attestation manager AI agent retrieves and applies data certification and attestation policies to manage the data certification and attestation of CI classes. It can the data certification policies and the data attestation policies of a Cl class.

-   **CMDB data ownership manager AI agent**

    The CMDB data ownership manager AI agent helps you to assess the quality of CI ownership data for a CI class to determine ownership, validate ownership, and evaluate ownership quality. You can validate fields that reference sys\_user or sys\_user\_group like **Assigned To**, **Managed by Group** \(default\), **Support Group**, and so on. The agent answers the following questions:

    -   Is CI ownership specified? Is the **Managed by group** attribute value set for the CI? Does it indicate an active and correctly configured record? The value of the system property for ownership is a default field for the evaluation. For the **Managed by group** CI attribute, you can specify the percentage values that classify the result as `Poor`, `Average`, or `Healthy`. For more information, see [Property settings for Now Assist for CMDB](../../now-assist-cmdb/reference/na-data-fdn-properties.md).
    -   If you provide a user referencing value: Does the **User Referencing** value indicate an active record? This evaluation identifies CIs that have inactive users and CIs with no **User** value.
    -   If you provide a user referencing value: Does the **Group Referencing** value indicate an active record? This evaluation identifies CIs that have inactive groups, empty groups \(no users\), and CIs with no **Group** value.
-   **CMDB health metrics manager AI agent**

    The CMDB health metrics manager AI agent displays information on CMDB Health Dashboard jobs, health metrics status, and health scores. If the jobs are not configured, the workflow provides a link to the setup instructions. For more information, see [CMDB Health](c_CMDBHealth.md).

-   **CMDB life cycle manager AI agent**

    The CMDB life cycle manager AI agent performs actions related to life-cycle management of CI classes: retrieve the life-cycle management policy and retirement definition for a CI class and create a life-cycle policy.

-   **CMDB principal class manager AI agent**

    The CMDB principal class manager AI agent determines whether you can set Cl classes as principal, suggests principal classes, and can set or unset a class as principal. Setting a class as a principal class is a practical way to save time because you can configure ServiceNow AI Platform products to display only principal classes in list views. The workflow helps you to decide which CIs you're most likely to work with day-to-day and then provides a link to enable you to set the associated classes as principal classes. For more information, see [Update the list of classes in the Principal Class filter](../task/update-principal-class-filter.md).

-   **CMDB search AI agent**

    The CMDB search AI agent searches the CMDB for a particular CI using single table query search or keyword query search and then displays a link to search results.

-   **CI summarizer AI agent**

    View a concise summary of key CI data. You can select the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.


**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

## Running AI agents autonomously

**Important:** By default, all agentic workflow and AI agent records are read only.

To run the AI agents autonomously, you must first duplicate the agentic workflow and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

-   **[Create a CI using Now Assist](../../now-assist-cmdb/task/na-cmdb-awf-ci-creator.md)**  
The Create configuration item agentic workflow accepts your natural language request to manually generate a valid CI in the class that you specify.
-   **[Getting advice from Now Assist on CMDB governance](../../now-assist-cmdb/concept/na-cmdb-awf-governance.md)**  
Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to help users to trust the data that they use for their work.
-   **[Use Now Assist to search the CMDB](../../now-assist-cmdb/task/na-cmdb-awf-search.md)**  
The Search CMDB agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then, depending on the information you provided, generates a keyword search, a single-table search with dot walks, or a multi-table search that involves relationship navigation. The workflow can infer CI relationship data to generate an appropriate query.

**Parent Topic:**[Now Assist for Configuration Management Database \(CMDB\)](now-assist-landing-cmdb.md)

