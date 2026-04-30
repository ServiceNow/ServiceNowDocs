---
title: Configure contract template rules
description: Configure a rule to identify the contract document template used for generating the contract document for a request.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure contract template rules

Configure a rule to identify the contract document template used for generating the contract document for a request.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## About this task

If you want the variables related to contract request to be available in condition builder, add the contract request reference to your application table. For more information, see [Provide access to contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Administration** &gt; **Contract Template Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_nbm_c44_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the contract template rule.

</td></tr><tr><td>

Description

</td><td>

Description of the contract template rule.

</td></tr><tr><td>

Requested table

</td><td>

Table in which the contract requests are saved.**Note:** The Contract Request table \[sn\_cm\_core\_contract\_request\] is selected by default to centralize the configuration on a single table and improve and reusability across product lines. You can choose to configure the template rules on a different table.

</td></tr><tr><td>

Category

</td><td>

Category of the document template.

</td></tr><tr><td>

Template

</td><td>

The published and active contract template that will be used to generate the contract document.

</td></tr><tr><td>

Order

</td><td>

Order in which the selection rule is run.If multiple rules meet the conditions from a contract request, the template rule with the lowest- order number is run for selecting the template.

</td></tr><tr><td>

Request type

</td><td>

Type of request the template rule is applicable to.For contract requests, select **New Contract**; for amendment requests, select **Amendment**.

</td></tr><tr><td>

Active

</td><td>

Option for marking the rule active. Only active rules are considered while submitting a request and identifying the appropriate template

</td></tr><tr><td>

Applies to

</td><td>

Conditions under which the contract template is selected. For example, to apply a rule when a contract request is submitted in an NDA category, you would enter the condition **\[Category\]\[is\]\[NDA\]**.

</td></tr></tbody>
</table>4.  Select **Submit**.

    ![Configure contract template rules](../image/cmpro-ct-rules.png "Contract template rules")


## What to do next

[Create a contract configuration](cncore-contract-config.md)

