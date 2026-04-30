---
title: Obtaining ERP Semantic Mining statistics and mining analysis
description: Use the ERP Semantic Mining home page dashboard to obtain statistics about candidates and info to help you troubleshoot.
locale: en-US
release: zurich
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Obtaining ERP Semantic Mining statistics and mining analysis

Use the ERP Semantic Mining home page dashboard to obtain statistics about candidates and info to help you troubleshoot.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

View statistics, metrics, and debug information for ERP Semantic Mining on the dashboard. Open links to related ERP Semantic Mining properties, logs, events, and editors.

You must have the sn\_erp\_mining.erp\_user role to view the dashboard.

To view the dashboard, navigate to **All** &gt; **ERP Foundation** &gt; **ERP Semantic Mining**.

Select the charts, graphs, and lists on the dashboard to view the underlying records. For example, select a section of a donut chart to see a list of the records for that section.

The dashboard contains three tabs.

## Custom applications results tab

This tab contains information about candidates.

|Title|Type|Description|
|-----|----|-----------|
|Application candidates per module|Donut|Number of application candidates for each module by number and percentage.|
|Application candidates by potential|Donut|Number of application candidates for each module by number and percentage.|
|Users of application candidates per module|Bar|Type of user of application candidates by module. User type is based on the number of different application candidates accessed. Users are defined as Light \(uses few apps\), Moderate \(uses multiple apps\), and Power \(uses the most apps\). Frequency of use isn't part of the calculation.|
|Application candidates per model|Bar|Number of application candidates that have a matching model in Zero Copy Connector for ERP.|
|Application candidates per CRUD operation type|Column|Number of application candidates by CRUD \(create, update, read, delete\) type for different models.|
|Application types|Column|Candidates by model type, such as a standard ERP model \(which you work with in Zero Copy Connector for ERP\), a workflow, or a custom business area.|

## Selected potential candidates tab

This tab contains information about candidates that have been identified as potential candidates for replatforming.

<table id="table_uln_spf_b2c"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the potential candidate, which is the record number on the ServiceNow AI Platform.

</td></tr><tr><td>

Short description

</td><td>

Brief information on what tables the potential candidate accesses

</td></tr><tr><td>

ERP application

</td><td>

Record for the ERP application of the potential candidate.

</td></tr><tr><td>

ERP module

</td><td>

Name of the ERP functional area in the system of record. For example, logistics, procurement, or sales.

</td></tr><tr><td>

Potential number

</td><td>

Evaluation of how well a potential candidate is suited for replatforming. The value represents how well the remote tables and extraction tables for the potential candidate match an application.

</td></tr><tr><td>

Similar candidates

</td><td>

Number of similar potential candidates. Similarity is based on the remote tables.

</td></tr><tr><td>

ERP models

</td><td>

Number of ERP models the potential candidate belongs to.ERP models are configured in Zero Copy Connector for ERP. An ERP model functions as a staging area that contains all potential fields you can add to remote and extraction tables, and read and update operations. You can then use the tables and queried data as a data source. For more information, see [Building and managing ERP models to work with ERP data](https://www.servicenow.com/docs/bundle/xanadu-application-development/page/build/erp-integration/concept/work-with-erp-data-models.html).

</td></tr><tr><td>

Updated

</td><td>

Date and time the candidate record was last edited.

</td></tr></tbody>
</table>## All applications results tab

This tab contains system-wide information that is useful to view after importing data.

| | | |
|---|---|---|
|Applications per module|Donut|Number of applications for each module by number and percentage.|
|Users per module|Donut|Number of users for each module by number and percentage.|
|Users of applications per module|Bar|Type of application users by module. User type is based on the number of different applications accessed. Users are defined as Light \(uses few apps\), Moderate \(uses multiple apps\), and Power \(uses the most apps\). Frequency of use isn't part of the calculation.|

**Parent Topic:**[Finding and working with candidates to replatform](work-with-candidates.md)

