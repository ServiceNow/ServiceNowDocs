---
title: Map a field to an expected response
description: Map a field of a use case to an expected response. Now Assist executes the fields \(prompt questions\) on a contract document to identify a non-standard clause.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-03-27"
reading_time_minutes: 3
breadcrumb: [Configuring contract analysis, Configure, Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Map a field to an expected response

Map a field of a use case to an expected response. Now Assist executes the fields \(prompt questions\) on a contract document to identify a non-standard clause.

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

7.  In the Expected response mappings page, select **New response**.

8.  On the form, fill in the fields.

<table id="table_hgz_nng_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use case

</td><td>

Use case that the field is associated with.**Note:** Only active use cases for contract analysis are displayed in the list.

</td></tr><tr><td>

Request table

</td><td>

Table that the contract analysis is executed from.

</td></tr><tr><td>

Field

</td><td>

Field \(question prompt\) that is mapped to the expected response.**Note:** Only active fields are displayed in the list.

</td></tr><tr><td>

Expected response

</td><td>

Expected response:-   Yes: When Now Assist returns the same response as expected, the system considers the field as standard.
-   No: When Now Assist returns a response that differs from the expected answer, the system considers the field as non-standard.

All such fields within a field group are categorized as non-standard and are displayed in transaction results with AI-generated comments in both the workspace and Word Add-in.

</td></tr><tr><td>

Applies when

</td><td>

Conditional fields that are based on an expected response.**Note:** If this condition fails, the expected answer isn't considered.

For more information on using the condition builder, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Order

</td><td>

Order in which the expected response is evaluated if a field has been mapped to multiple responses.Now Assist evaluates the expected response from the lowest ordered number to the highest ordered number. Now Assist stops evaluating when the expected response is satisfied.

</td></tr></tbody>
</table>9.  Select **Save**.


**Parent Topic:**[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

**Related topics**  


[Create use cases for contract analysis](cmpro-na-usecase-ca.md)

[Map a field group to a clause](cmpro-na-map-fieldgrp-clause.md)

[Map a use case for contract analysis](cmpro-na-usecase-mappings-ca.md)

