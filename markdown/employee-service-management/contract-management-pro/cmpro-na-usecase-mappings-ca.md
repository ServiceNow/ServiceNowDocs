---
title: Map a use case for contract analysis
description: Map a use case to specific tables, and define conditions to apply the use case for contract analysis.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-03-27"
reading_time_minutes: 2
breadcrumb: [Configuring contract analysis, Configure, Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Map a use case for contract analysis

Map a use case to specific tables, and define conditions to apply the use case for contract analysis.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_contract\_config

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  On the tile for your skill, select **Activate skill**.

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

The parent table from which the contract request is created.

</td></tr><tr><td>

Request conditions

</td><td>

Conditions under which the use case is applicable.For more information on using the condition builder, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>10. Select **Save**.


**Parent Topic:**[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

**Related topics**  


[Create use cases for contract analysis](cmpro-na-usecase-ca.md)

[Map a field group to a clause](cmpro-na-map-fieldgrp-clause.md)

[Map a field to an expected response](cmpro-na-exp-res-mapping.md)

