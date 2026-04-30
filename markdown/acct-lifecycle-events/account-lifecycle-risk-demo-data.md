---
title: Sample risk definitions
description: These are sample risk definitions available with the base system and can configured based on your requirements.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setup the engagement risk definition, Configure customer success, Customer success, Customer Success Management]
---

# Sample risk definitions

These are sample risk definitions available with the base system and can configured based on your requirements.

## Drop in NPS health

This is a metric based risk definition and generates a risk signal if the NPS score falls below a specified threshold. In this case, if the Daily collection of NPS metric score falls below 30, a risk signal is generated. Additionally, override conditions with different threshold values and ranking that can impact specific engagements are defined.

![NPS health risk definition](../image/account-lifecycle-risk-defn-nps-health.png)

## SLA achievement in less than 90%

This is a metric based risk definition and generates a risk signal if the SLA achievement score falls below a specified threshold. In this case, if the Daily collection of % achieved incident SLA metric falls below 90, a risk signal is generated. An override condition with a different threshold value that can impact specific engagements has been defined. Additionally, a filter condition has been defined in the Applicable engagements field. This filter condition is applied along with the override condition when the risk signal is generated.

![SLA achievement score](../image/account-lifecycle-risk-defn-sla-score.png)

**Note:** For metric based definitions, the data source and the context engine mapping must be defined. See [Setup the data context engine](account-lifecycle-setup-metric-data.md) for details.

## Missing renewal date in contract

This is a table based risk definition and generates a risk signal if the contract renewal date are missing. In this case, the Source table is the Contract table. This table must be mapped to the Engagement table. See [Set up the context engine mapper](account-lifecycle-define-context-engine-mapper.md) for details. If the renewal start and end dates are missing in the Contract table, a risk signal is generated.

![Missing renewal date](../image/account-lifecycle-risk-defn-renew-date.png)

