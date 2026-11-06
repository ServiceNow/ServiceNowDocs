---
title: Product compliance summarization skill - Triggers and Inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a product compliance summary. A trigger initiates an action, such as when the system generates a product compliance summary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/product-compliance-sum-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Product compliance summarization skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a product compliance summary. A trigger initiates an action, such as when the system generates a product compliance summary.

## Triggers for product compliance summarization skill

The following table lists the triggers that determine when a product compliance summary is generated and how a product compliance summary is displayed.

|Trigger|Description|
|-------|-----------|
|User-triggered|Product compliance summary is generated when the agent manually triggers the skill by selecting **Summarize** in the Publisher details page.|

## Inputs for the product compliance summarization skill

The following table lists the inputs for the product compliance summarization skill.

<table id="table_inputs_pcs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reconciliation results

</td><td>

Compliance status of the software products with regards to the discovery and entitlements.

</td></tr><tr><td>

Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]

</td><td>

Contains product life-cycle details for all the software products that are installed in your environment.

</td></tr><tr><td>

Dashboards

</td><td>

Dashboards include Discovered inventory, Normalization and content, Health check, and Optimization and Savings dashboard.

</td></tr><tr><td>

SAP related tables

</td><td>

The SAP related tables include:-   SAP Document Type \[samp\_sap\_document\_type\]
-   SAP Digital Access Usage \[samp\_sap\_digital\_access\_usage\]
-   SAP Engine Usage \[samp\_sap\_sw\_client\_access\]
-   SAP System User \[samp\_sap\_system\_user\]

</td></tr><tr><td>

Software Subscription \[samp\_sw\_subscription\] table

</td><td>

Contains information pertaining to user software subscriptions.

</td></tr><tr><td>

Purchased Subscription Details \[samp\_purchased\_subscription\_details\]

</td><td>

Contains the information pulled from the Microsoft Azure portal related to subscriptions purchased and assigned for Microsoft 365.

</td></tr><tr><td>

Software Installation table \[cmdb\_sam\_sw\_install\]

</td><td>

Contains information on all software installed in your environment.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)

