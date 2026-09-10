---
title: Recommended actions roles and tables
description: The Recommended actions feature includes the following roles and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-360-reco-actions-reference.html
release: australia
topic_type: reference
last_updated: "2026-08-25"
reading_time_minutes: 1
keywords: [recommended actions, success recommendation table, ALE definition table, recommendation skill, Account 360 reference]
breadcrumb: [View and execute recommended actions for an engagement, Engagement home page, Manage engagements, Customer success, Use, Customer Success Management]
---

# Recommended actions roles and tables

The Recommended actions feature includes the following roles and tables.

## Roles

The following roles are required to use or administer recommended actions.

|Role|Description|
|----|-----------|
|`sn_customerservice_agent`|Required to access Technology Account 360 and the Recommended actions panel. Grants Account 360 data broker access.|
|`sn_tech_exp.executive_portfolio_manager`|Grants Executive Portfolio data broker access. Required to view the Executive Portfolio page and navigate to it from Account 360.|

## Tables

Recommended actions uses the following tables.

|Table|Purpose|Notes|
|-----|-------|-----|
|`success_recommendation`|Caching and staging table for AI-generated play recommendations|Stores fetched recommendations for an account so that reopening the panel does not trigger a new AI call. Records are cascade-deleted when new account insights are fetched or when the context expiry period elapses.|
|ALE definition table|Candidate pool for play matching|Contains the play definitions evaluated against the account context. Recommendations are only surfaced when records in this table semantically match the account's current context. The table is the source of all `sys_id` values returned by the skill.|
|Script include: `ExecPortfolioRecommendedActions`|Server-side orchestration|Assembles the skill payload and calls the recommendation skill. Works with `SuccessRecommendationUtil` and the platform's `ScriptingGeneratorFactory` pattern.|

**Parent Topic:**[View and execute recommended actions for an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-360-view-reco-actions.md)

