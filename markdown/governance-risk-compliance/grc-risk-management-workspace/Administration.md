---
title: Risk Management Administration
description: Using the Risk Management application, administrators can customize risk categories, risk criteria, risk management properties, and risk assessment types.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Risk Management detailed setup, Configure, Risk Management, Governance, Risk, and Compliance]
---

# Risk Management Administration

Using the Risk Management application, administrators can customize risk categories, risk criteria, risk management properties, and risk assessment types.

## Risk criteria

Risk criteria are the scoring values attributed to the likelihood that a risk occurs, and the impact to your organization if the risk does occur.

Risk criteria thresholds define a high/likely or low/unlikely score as shown:

|Likelihood|Impact|Scores|
|----------|------|------|
|1 = Extremely Unlikely|1 = Very Low|0-5 = Very Low|
|2 = Unlikely|2 = Low|6-10 = Low|
|3 = Neutral|3 = Moderate|11-15 = Moderate|
|4 = Likely|4 = High|16-20 = High|
|5 = Extremely Likely|5 = Very High|21-25 = Very High|

|Name|Description|
|----|-----------|
|A list of tables that are available in the **Applies to** field on forms|If this field is blank, all tables are available on the various forms for Entity Types, Entities, and Risks. Defines a comma-separated list of tables that are available in the **Applies to** field on the Entity Type, Entity, and Risk form. Add **.extended** after the table name to include all extended tables.|

## Assessment types

Risk managers can create a new set of questions for each risk assessment. See [Create an assessment type](../task/create-assessment-type.md).

**Parent Topic:**[Risk Management detailed setup](setup-risk-management.md)

