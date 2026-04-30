---
title: Identify endless loops in blueprint rules
description: Use the Rule Cycle Report to identify endless loops that may be hard to find during ordinary operation.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Identify endless loops in blueprint rules

Use the Rule Cycle Report to identify endless loops that may be hard to find during ordinary operation.

## Before you begin

Role required: Admin

## Procedure

1.  In ServiceNow CPQ Admin, click to open Configuration Blueprints, and open a blueprint.

2.  Click the three vertical dots next to **Deploy**, and then click **Rule Cycle Report**.

3.  Click **Run Report**.

4.  Alternatively, from a top-level Transaction Manager element page such as Stages, Associated Fields, or Related Rules, click the three vertical dots in the sub-header, and then click **Rule Cycle Report**.


## Result

The report provides a list of all potential circular references in the blueprint. For each record, the involved rules and fields are noted. Links help the administrator quickly review rule definitions. Often, an admin needs to examine related fields. When investigating in this way, a breadcrumb trail is provided to help the administrator navigate amongst the related components and back to the Rule Cycle Report.

The most recent Rule Cycle Report remains visible to all administrators until the report is run again by clicking **Rerun Report**.

![Identify endless loops in Blueprint rules](../images/cpq-encrichments-rule-cycle-report.png)

![Identify endless loops in Blueprint rules](../images/cpq-enrichments-rule-cycle-report-breadcrumbs.png)

