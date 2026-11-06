---
title: Components installed with AI Cost Management
description: Several types of components are installed with activation of the sn\_itam\_aicm plugin, including user roles, scheduled jobs, and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/installed-with-ai-cost-management.html
release: australia
product: Asset Management
classification: asset-management
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [Reference, AI Cost Management, IT Asset Management, Asset Management]
---

# Components installed with AI Cost Management

Several types of components are installed with activation of the sn\_itam\_aicm plugin, including user roles, scheduled jobs, and tables.

## Roles installed

<table id="table_zk1_hkd_xjc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

AI cost administrator

 \[ai\_cost\_admin\]

</td><td>

This role has full access to the AI Cost Management application. This role is required for all administrative functions, such as setting up integrations with AI SaaS providers.

</td><td>

none

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_uhg_l2y_skc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AICM - Alert Evaluation

</td><td>

Runs at 10:00 UTC daily to evaluate spend against set thresholds on spend limits. Creates alerts when thresholds are exceeded.

</td></tr><tr><td>

AICM - Anthropic Spend Limits Pull

</td><td>

Runs at 00:00 UTC daily to pull user spend limits from Anthropic.

</td></tr><tr><td>

AICM - Anthropic Usage Pull

</td><td>

Runs at 2:00 UTC daily to pull usage data from Anthropic.

</td></tr><tr><td>

AICM - Daily Licensing Counts

</td><td>

Runs at 12:00 UTC daily to publish the AI Cost Management license counts to the Licensing Resource Counts \[itam\_licensing\_resource\_counts\] table

</td></tr><tr><td>

AICM - Dimensional Roll Up

</td><td>

Runs at 6:00 UTC daily to roll up entity-level spend to higher level entities.

</td></tr><tr><td>

AICM - Microsoft Copilot Usage Pull

</td><td>

Runs at 2:30 daily to pull usage data from Copilot.

</td></tr><tr><td>

AICM - Normalize Discovered AI Models

</td><td>

Runs at 13:00 UTC daily. Normalizes Anthropic model names to model names in ServiceNow.

</td></tr><tr><td>

AICM - Normalize Discovered Products

</td><td>

Runs at 14:00 UTC daily. Normalizes consumption product names to product names in ServiceNow.

</td></tr><tr><td>

AICM - Normalize Discovered Users

</td><td>

Runs at 12:00 UTC daily. Normalizes user names from AI accounts to users in ServiceNow, by user ID, email, and then name.

</td></tr><tr><td>

AICM - Spend Limit Snapshot

</td><td>

Runs at 5:00 UTC monthly. Reads the Alert Configuration \[alert\_config\] table and saves that as a monthly snapshot to the Spend Limit Snapshot table.

</td></tr></tbody>
</table>## Tables installed

<table id="table_whg_l2y_skc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI model

 \[aicm\_ai\_model\]

</td><td>

AI models whose usage is tracked.

</td></tr><tr><td>

Consumer AI usage aggregate

 \[aicm\_ai\_usage\_aggregatel\]

</td><td>

Aggregation of all AI spend

</td></tr><tr><td>

Consumer AI usage

 \[aicm\_ai\_usage\_daily\]

</td><td>

Daily user consumption

</td></tr><tr><td>

Alert

 \[aicm\_alert\]

</td><td>

Generated alert information

</td></tr><tr><td>

Alert configuration

 \[aicm\_alert\_config\]

</td><td>

Alert configuration information for the current month. A snapshot is taken each month and stored in the Spend Limit Snapshot table \[aicm\_spend\_limit\_snapshot\] to preserve history.

</td></tr><tr><td>

Alert dismissal

 \[aicm\_alert\_dismissal\]

</td><td>

Populated when a user dismisses an alert from the UI.

</td></tr><tr><td>

Custom AI model

 \[aicm\_custom\_ai\_model\]

</td><td>

Custom AI models whose usage is tracked.

</td></tr><tr><td>

Discovered AI model

 \[aicm\_discovered\_ai\_model\]

</td><td>

AI model discovered during data ingestion.

</td></tr><tr><td>

Discovered AI product

 \[aicm\_discovered\_product\]

</td><td>

AI product discovered during data ingestion.

</td></tr><tr><td>

Discovered AI service

 \[aicm\_discovered\_product\]

</td><td>

AI service discovered during data ingestion.

</td></tr><tr><td>

AICM discovered user

 \[aicm\_discovered\_user\]

</td><td>

User discovered during data ingestion.

</td></tr><tr><td>

AICM integration

 \[aicm\_integration\_account\]

</td><td>

AI account information based on an integration.

</td></tr><tr><td>

Consumer AI usage by dimension grouping\[aicm\_nd\_ai\_usage\]

</td><td>

Populated by the Dimensional Roll Up job. Holds data displayed in top-level Usage pages.

</td></tr><tr><td>

AI usage by user\[aicm\_user\_ai\_usage\]

</td><td>

AI usage information for a given user.

</td></tr><tr><td>

Spend limit snapshot\[aicm\_spend\_limit\_snapshot\]

</td><td>

Stores monthly spend limit snapshots.

</td></tr><tr><td>

Subscription\[aicm\_subscription\]

</td><td>

Subscription information per user.

</td></tr><tr><td>

Subscription aggregate\[aicm\_subscription\_aggregate\]

</td><td>

Monthly history of subscription.

</td></tr><tr><td>

Subscription cost\[aicm\_subscription\_cost\]

</td><td>

Tenant-wide seat count for purchased, assigned, and available seats and monthly seat cost.

</td></tr><tr><td>

User spend limit\[aicm\_user\_spend\_limit\]

</td><td>

User spend limit information.

</td></tr><tr><td>

AICM licensing cost breakdownaicm\_licensing\_cost\_breakdown

</td><td>

Daily USD spend per account that makes up the published consumption license count.

</td></tr><tr><td>

AICM licensing user breakdownaicm\_lcensing\_user\_breakdown

</td><td>

Distinct subscription users that make up the published subscription-users license count.

</td></tr></tbody>
</table>