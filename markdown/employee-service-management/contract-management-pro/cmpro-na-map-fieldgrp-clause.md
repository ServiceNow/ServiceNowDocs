---
title: Map a field group to a clause
description: Map field groups of a use case to clause variations of a clause library. Now Assist uses the mapped clause content to display suggestions for a missing or non-standard clause.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-03-27"
reading_time_minutes: 2
breadcrumb: [Configuring contract analysis, Configure, Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Map a field group to a clause

Map field groups of a use case to clause variations of a clause library. Now Assist uses the mapped clause content to display suggestions for a missing or non-standard clause.

## Before you begin

Ensure that you have active clauses in the clause library.

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_contract\_config

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  On the tile for your skill, select **Activate skill**.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

4.  In the General details page, view the skill details and select **Save and continue**.

5.  In the Use case page, select **Save and continue**.

    For more information on creating a use case, see [Create use cases for contract analysis](cmpro-na-usecase-ca.md).

6.  In the Clause mappings page, select **New clause mapping**.

7.  On the form, fill in the fields.

<table id="table_pkv_1qg_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use case

</td><td>

Use case that you want to map a clause with.**Note:** Only active use cases for contract analysis are displayed in the list.

</td></tr><tr><td>

Request table

</td><td>

Request table that contains the clauses that you want to map.

</td></tr><tr><td>

Field group

</td><td>

Field group that you want to map a clause with.**Note:** Only active field groups are displayed.

</td></tr><tr><td>

Clause

</td><td>

Clause that you want to map the field group to.**Note:** Only active clauses are displayed in the list.

</td></tr></tbody>
</table>8.  Add another field group to a clause variation by selecting **New mapping**.

    ![Clause mapping for contract analysis with the option of adding multiple mappings.](../image/cmpro-na-clause-map.png "Clause mapping for Contract analysis")

9.  Select **Save**.


**Parent Topic:**[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

**Related topics**  


[Create use cases for contract analysis](cmpro-na-usecase-ca.md)

[Map a field to an expected response](cmpro-na-exp-res-mapping.md)

[Map a use case for contract analysis](cmpro-na-usecase-mappings-ca.md)

