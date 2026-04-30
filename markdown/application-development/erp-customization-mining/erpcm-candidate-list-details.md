---
title: ERP-CM candidate list field descriptions
description: The candidate list in ERP Semantic Mining \(ERP-CM\) displays information on the basic details for each candidate.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ERP-CM field descriptions, ERP Semantic Mining reference, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# ERP-CM candidate list field descriptions

The candidate list in ERP Semantic Mining \(ERP-CM\) displays information on the basic details for each candidate.

For process details, see [Browse an overview of candidates in ERP-CM](../task/erpcm-view-home-page-overview.md).

<table id="table_yct_bl4_vvb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the application candidate, which is the record number on the ServiceNow AI Platform.

</td></tr><tr><td>

Short description

</td><td>

Brief information on what tables the candidates accesses.

</td></tr><tr><td>

Potential

</td><td>

Evaluation of how well a candidate is suited for replatforming.The value represents how well the remote tables and extraction tables for the candidate match an application.

-   A high potential indicates that ERP-CM can immediately use remote tables and extraction tables that match the ERP model for the application candidate without making additional changes.
-   A low potential indicates that the application candidate matches few of the remote tables and extraction tables in the ERP models in Zero Copy Connector for ERP.

**Note:** This column is available only on the candidates list on the Candidates page, not on the home page.

</td></tr><tr><td>

ERP application

</td><td>

Record for the ERP application of the candidate.

</td></tr><tr><td>

ERP module

</td><td>

Name of the ERP functional area in the system of record. For example, logistics, procurement, or sales.

</td></tr><tr><td>

ERP models

</td><td>

Number of ERP models the candidates belongs to.ERP models are configured in Zero Copy Connector for ERP. An ERP model functions as a staging area that contains all potential fields you can add to remote and extraction tables, and read and update operations. You can then use the tables and queried data as a data source on the ServiceNow AI Platform. For more information, see [Building and managing ERP models to work with ERP data](../../erp-integration/concept/work-with-erp-data-models.md).

**Note:** This column is available only on the candidates list on the Candidates page, not on the home page.

</td></tr><tr><td>

Similar candidates

</td><td>

Number of similar candidates. Similarity is based on the remote tables.

</td></tr></tbody>
</table>**Parent Topic:**[ERP-CM field descriptions](../concept/erpcm-field-description-reference-landing.md)

