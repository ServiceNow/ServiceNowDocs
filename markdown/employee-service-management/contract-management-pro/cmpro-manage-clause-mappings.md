---
title: Manage clause mappings for contract analysis
description: Manage clause mappings for contract analysis by updating the mapped clause for a field group, deactivating the mappings when not in use, or deleting them when no longer required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-manage-clause-mappings.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Update clause mappings, Modify clause mappings, Edit clause mappings, Delete clause mappings, Deactivate clause mappings]
breadcrumb: [Manage skills, ServiceNow Otto for Contract Management Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Manage clause mappings for contract analysis

Manage clause mappings for contract analysis by updating the mapped clause for a field group, deactivating the mappings when not in use, or deleting them when no longer required.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_contract\_config

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **AI Admin Hub** to access the **AI Skills** tab of the AI Admin Hub console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  On the **Contract analysis** tile, select **Edit Configuration**.

    \[Omitted image "cmpro-na-active-skills.png"\] Alt text: Active skills in Contract management pro.

4.  In the skill guided setup, select **Clause mappings**.

5.  Select the actions icon \[Omitted image "cmpro-na-three-dot-icon.png"\] Alt text: Actions icon on the clause mapping that you want to update, delete, or deactivate.

    \[Omitted image "cmpro-na-edit-clause-map.png"\] Alt text: Actions available on clause mappings for contract analysis.

    -   **Edit**

        Update the field group to clause mappings for a use case.

        For more information on clause mapping, see [Map a field group to a clause](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-map-fieldgrp-clause.md).

    -   **Deactivate**

        Deactivate a clause mapping to temporarily make it unavailable for the skill.

        The **Reactivate** option appears when a clause mapping is deactivated. Use this option to activate a clause mapping.

    -   **Delete**

        Delete a clause mapping when it is no longer required for the skill.


## Result

AI uses the updated clause mappings to display suggestions for non-standard or missing clauses in a contract document.

**Parent Topic:**[Managing skills for ServiceNow Otto for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-manage-na-skills.md)

**Related topics**  


[Manage use cases for ServiceNow Otto for Contract Management Pro]()

[Manage use case mappings for ServiceNow Otto for Contract Management Pro]()

[Manage expected response mappings for contract analysis]()

[Deactivate skills for ServiceNow Otto for Contract Management Pro]()

[Map a field group to a clause](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-na-map-fieldgrp-clause.md)

