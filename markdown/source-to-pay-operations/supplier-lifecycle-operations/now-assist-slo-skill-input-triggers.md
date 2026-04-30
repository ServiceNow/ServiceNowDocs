---
title: Configure skill input for Now Assist for Supplier Lifecycle Operations \(SLO\)
description: You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [Configure, Now Assist for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure skill input for Now Assist for Supplier Lifecycle Operations \(SLO\)

You can configure some of the inputs for a generative AI skill. Inputs permit you to determine how and when a skill is used.

## Overview of skills

Inputs identify the data used for a skill. Inputs include the table and fields used to generate a case summary.

You can modify inputs, but you can't modify a skill's data source. The data source contains the tables and fields that the skill relies on.

## Now Assist skill for Now Assist for SLO

The Now Assist for SLO includes the following skills:

-   Supplier case summarization
-   Supplier performance summarization

## Supplier case summarization skill

Inputs for the Supplier case summarization skill identify the table and fields that are used when the summary is generated for a supplier request.

The following table lists the inputs for the Supplier case summarization skill from the Choose input for supplier request page in the Now Assist Admin console.

<table id="table_arz_fk3_1cc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input table

</td><td>

Supplier case \[sn\_slm\_case\] table

</td></tr><tr><td>

Base input fields

</td><td>

-   Short description
-   Description
-   State
-   Work notes
-   Additional comments
-   Assigned to
-   Created
-   Created by
-   Due date
-   Case type
-   Supplier
-   Priority
-   Close notes

</td></tr></tbody>
</table>## Supplier performance summarization skill

Inputs for the Supplier performance summarization skill identify the table and fields that are used when the summary is generated for a supplier's KPIs.

The following table lists the inputs for the Supplier performance summarization skill from the Choose input for supplier request page in the Now Assist Admin console.

<table id="table_wtw_13w_j3c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input table

</td><td>

KPI \[sn\_kpi\_kpi\] table

</td></tr><tr><td>

Base input fields

</td><td>

-   Name
-   Active
-   Type
-   Domain
-   Last period data
-   Performance
-   Threshold set
-   Current threshold

</td></tr></tbody>
</table>**Related topics**  


[Customize a Now Assist for Supplier Lifecycle Operations \(SLO\) skill for Case summarization](../task/now-assist-slo-cust-skill.md)

[Customize Now Assist for Supplier Lifecycle Operations \(SLO\) to use the Virtual Agent chat](../task/cust-now-assist-slo-va.md)

