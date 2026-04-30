---
title: Getting advice from Now Assist on CMDB governance
description: Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to ensure that users can trust the data that they use for their work.
locale: en-US
release: yokohama
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-12-01"
reading_time_minutes: 5
breadcrumb: [Use agentic workflows, Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Getting advice from Now Assist on CMDB governance

Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to ensure that users can trust the data that they use for their work.

## Access the workflow

See [Get advice on CMDB governance from Now Assist](../task/na-cmdb-awf-cmdb-governance.md) for information on accessing the workflow.

## Provide advice on CMDB governance agentic workflow

The Configuration Management Database \(CMDB\) is the central repository of your organization's IT assets, services, and their relationships. The Provide advice on CMDB governance agentic workflow helps to ensure CMDB accuracy, completeness, and integrity to maximize the value and performance of your ServiceNow AI Platform products. The results are faster incident resolution, enhanced compliance, and a reduced risk of service disruption. The agentic workflow evaluates CIs updated in the last 90 days.

The Provide advice on CMDB governance agentic workflow supports admins and owners with information on data health and ongoing guidance for governance as data models and integrations grow. The workflow calls on AI agents.

![AI agents used by the CMDB principal class manager AI agent](../image/na-cmdb-governance-flow.png)

## Agentic workflows

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

-   **CMDB principal class manager AI agent**

    The CMDB principal class manager AI agent determines whether you can set Cl classes as principal, suggests principal classes, and can set or unset a class as principal. Setting a class as a principal class is a practical way to save time because you can configure ServiceNow AI Platform products to display only principal classes in list views. The workflow helps you to decide which CIs you are most likely to work with day-to-day and then provides a link to enable you to set the associated classes as principal classes. For more information, see [Update the list of classes in the Principal Class filter](../../configuration-management/task/update-principal-class-filter.md).

-   **CMDB life cycle manager AI agent**

    The CMDB life cycle manager AI agent helps admins to ensure that CMDB life-cycle policies are in place for principal classes or for specified classes. For more information, see [Working with CMDB Data Manager](../../configuration-management/concept/cmdb-data-management.md).

-   **CMDB data certification and attestation manager AI agent**

    The CMDB data certification and attestation manager AI agent retrieves the data certification and attestation policies for a CI class and for similar classes. It can also create a data certification and an attestation policy. For more information, see [Data Certification](../../data-certification/concept/c_DataCertification.md).

-   **CMDB health metrics manager AI agent**

    The CMDB health metrics manager AI agent displays information on CMDB Health Dashboard jobs, health metrics status, and health scores. If the jobs are not configured, the workflow provides a link to the setup instructions. For more information, see [CMDB Health](../../configuration-management/concept/c_CMDBHealth.md).

-   **CMDB data ownership manager AI agent**

    The CMDB data ownership manager AI agent helps you to assess the quality of CI ownership data for a CI class to determine ownership, validate ownership, and evaluate ownership quality. You can validate fields that reference sys\_user or sys\_user\_group like **Assigned To**, **Managed by Group** \(default\), **Support Group**, and so on. The agent answers the following questions:

    -   Is CI ownership specified? Is the **Managed by group** attribute value set for the CI? Does it point to an active and correctly configured record? The value of the system property for ownership is a default field for the evaluation. For the **Managed by group** CI attribute, you can specify the percentage values that classify the result as `Poor`, `Average`, or `Healthy`. For more information, see [Property settings for Now Assist for CMDB](../reference/na-data-fdn-properties.md).
    -   If you provide a user referencing value: Does the **User Referencing** value point to an active record? This evaluation identifies CIs that have inactive users and CIs with no **User** value.
    -   If you provide a user referencing value: Does the **Group Referencing** value point to an active record? This evaluation identifies CIs that have inactive groups, empty groups \(no users\), and CIs with no **Group** value.

-   **[Get advice on CMDB governance from Now Assist](../task/na-cmdb-awf-cmdb-governance.md)**  
Work through the process of improving CMDB data accuracy, completeness, and health. The objective is to ensure that users can trust the data that they use for their work.

**Parent Topic:**[Using agentic workflows in Now Assist for CMDB](../../configuration-management/concept/now-assist-cmdb-using.md)

