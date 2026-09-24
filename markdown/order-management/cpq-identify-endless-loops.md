---
title: Identify endless loops in blueprint rules
description: Use the Rule Cycle Report to identify endless loops that may be hard to find during ordinary operation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-identify-endless-loops.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [blueprint rules, endless loops, rule cycle report, circular references]
breadcrumb: [CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Identify endless loops in blueprint rules

Use the Rule Cycle Report to identify endless loops that may be hard to find during ordinary operation.

## Before you begin

Role required: Admin

## Procedure

1.  In CPQ Admin, select **Configuration Blueprints**, and then open a blueprint.

2.  Select the **three vertical dots** icon next to **Deploy**, and then select **Rule Cycle Report**.

3.  Select **Run Report**.

4.  From a top-level Transaction Manager element page such as Stages, Associated Fields, or Related Rules, select the **Settings** icon in the sub-header, and then select **Rule Cycle Report**.


## Result

The report provides a list of all potential circular references in the blueprint. For each record, the involved rules and fields are noted. Links help the administrator quickly review rule definitions. Often, an admin needs to examine related fields. When investigating in this way, a breadcrumb trail is provided to help the administrator navigate amongst the related components and back to the Rule Cycle Report.

The most recent Rule Cycle Report remains visible to all administrators until the report is run again by selecting **Rerun Report**.

\[Omitted image "cpq-encrichments-rule-cycle-report.png"\] Alt text: Identify endless loops in Blueprint rules

\[Omitted image "cpq-enrichments-rule-cycle-report-breadcrumbs.png"\] Alt text: Identify endless loops in Blueprint rules

