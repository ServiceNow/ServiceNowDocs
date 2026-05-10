---
title: Map a use case for contract analysis
description: Map a use case to specific tables, and define conditions to apply the use case for contract analysis.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Contract analysis, Contract use case mapping, Contract analysis use case mapping, Now Assist use case mapping, Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro]
breadcrumb: [Configure contract analysis, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Map a use case for contract analysis

Map a use case to specific tables, and define conditions to apply the use case for contract analysis.

## Before you begin

Ensure that the application is in Global or Now Assist in Contract Management scope. If you are configuring the use case mapping in different application scope, add the scoped ACL to the Use Case Mapping table \(sn\_cm\_gen\_ai\_usecase\_configuration\).

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  Select **Activate skill** on the skill you want to activate.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

4.  In the General details page, view the skill details and select **Save and continue**.

5.  In the Use case page, select **Save and continue**.

    For more information on creating a use case, see [Create use cases for contract analysis](cmpro-na-usecase-ca.md).

6.  In the Clause mappings page, select **Save and continue**.

    For more information on mapping a field group to a clause, see [Map a field group to a clause](cmpro-na-map-fieldgrp-clause.md).

7.  In the Expected response mappings page, select **Save and continue**.

    For more information on mapping a field to an expected response, see [Map a field to an expected response](cmpro-na-exp-res-mapping.md).

8.  In the Use case mappings page, select **New**.

9.  On the form, fill in the fields.

<table id="table_lxd_sm1_wcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the use case mapping.

</td></tr><tr><td>

Use case

</td><td>

The use case used to analyze contract for non-standard or missing clauses.**Note:** Only active use cases for contract analysis are displayed in the list.

</td></tr><tr><td>

Contract type

</td><td>

The contract type for which the use case will apply.**Note:** Only active contract types are displayed in the list.

</td></tr><tr><td>

Order

</td><td>

Order in which the use case will apply.If multiple use cases meet the same conditions, the use case with the lowest order number is applied first.

</td></tr><tr><td>

Request table

</td><td>

The Contract Request table \[sn\_cm\_core\_contract\_request\] is selected by default to centralize the configuration on a single table and improve reusability across product lines. You can choose to configure the use case mapping on a different table.

</td></tr><tr><td>

Request conditions

</td><td>

Conditions under which the use case is applicable.For more information on using the condition builder, see [Create a condition statement using the condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/create-cond-state-using-cond-build.md).

</td></tr></tbody>
</table>10. Select **Save**.


## Result

The use case is mapped to specific tables and conditions. Now Assist applies the use case for contract analysis when the conditions are met.

**Parent Topic:**[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

**Related topics**  


[Create use cases for contract analysis](cmpro-na-usecase-ca.md)

[Map a field group to a clause](cmpro-na-map-fieldgrp-clause.md)

[Map a field to an expected response](cmpro-na-exp-res-mapping.md)

[Create use cases for contract analysis](cmpro-na-usecase-ca.md)

