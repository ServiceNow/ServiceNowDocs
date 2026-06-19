---
title: Now Assist for CSM Major Issue Management Properties
description: The Now Assist for CSM Major Issue Management application is configured through the NowAssistMajorIssueExtPoint extension point and the trigger conditions on the Major case agentic workflow flow. This reference describes every configurable property, the valid values, the default, and the impact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/na-for-csm-mim-properties.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: reference
last_updated: "2026-06-02"
reading_time_minutes: 2
breadcrumb: [Configure Now Assist for CSM Major Issue Management, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Now Assist for CSM Major Issue Management Properties

The Now Assist for CSM Major Issue Management application is configured through the `NowAssistMajorIssueExtPoint` extension point and the trigger conditions on the **Major case agentic workflow** flow. This reference describes every configurable property, the valid values, the default, and the impact.

## Flow trigger properties

Configure these properties in Flow Designer on the **Major case agentic workflow** flow trigger.

|Property|Description|Default|Impact|
|--------|-----------|-------|------|
|Trigger conditions|The case-record conditions that cause the flow to run. Add filters such as category, account, product, or any other case field to control which cases the AI detection evaluates.|Priority is 1 or 2; Parent is empty|More restrictive conditions reduce AI skill executions, which lowers cost and processing load.|

## Major case search configuration

These properties come from `NowAssistMajorIssueExtPoint.getConfigForMajorCase()`. They control the search for similar existing major cases.

|Property|Description|Values|Default|Impact|
|--------|-----------|------|-------|------|
|`maxSearchResults`|Maximum number of similar major cases returned by the AI search.|Integer 1–50|10|Higher values increase AI search cost and latency. Lower values may miss relevant matches.|
|`similarityThreshold`|Minimum similarity score a major case must meet to be included in results.|0.0–1.0|0.75|Higher values return fewer, more precise matches. Lower values cast a wider net with more noise.|
|`searchProfile`|AI search profile used when searching for similar open major cases. Determines which indexed fields and ranking logic apply.|String \(profile name\)|`sn_csm_mim_gen_ai_mim_major_cases_profile`|You can edit this profile or replace it with a custom profile. The profile must return major cases.|
|`matchFieldList`|Case fields whose values are appended as additional exact-match filter conditions on the AI search.|Array of field names \(for example, `["account", "product"]`\). Empty field values are skipped.|`[]`|Restricts the search to cases that exact-match on the listed fields. For example, with `["account"]`, only cases from the same account are considered.|

## Non-major case search configuration

These properties come from `NowAssistMajorIssueExtPoint.getConfigForNonMajorCase()`. These properties control the search for similar non-major cases.

|Property|Description|Values|Default|Impact|
|--------|-----------|------|-------|------|
|`maxSearchResults`|Maximum number of similar non-major cases returned by the AI search.|Integer 1–50|10|Higher values increase AI search cost and latency. Lower values may undercount similar cases and suppress major case escalation.|
|`similarityThreshold`|Minimum similarity score a non-major case must meet to be included in results.|0.0–1.0|0.70|Higher values enforce stricter matching before escalation is considered. Lower values may trigger escalation proposals more liberally.|
|`searchProfile`|AI search profile used when searching for similar open non-major cases.|String \(profile name\)|`sn_csm_mim_gen_ai_mim_non_major_cases_profile`|Determines which indexed fields and ranking logic apply during the non-major search.|
|`matchFieldList`|Case fields whose values are appended as additional exact-match filter conditions on the AI search.|Array of field names. Empty field values are skipped.|`[]`|Restricts the search to cases that exact-match on the listed fields.|
|`minSimilarCasesForMajor`|Minimum number of similar non-major cases the AI must return before the new case is auto-proposed as a major case. Below this threshold the flow exits with no updates.|Integer 1–N|5|Lower values make major case escalation easier to trigger. Higher values require stronger evidence before a new major case is proposed.|

## Extension point method reference

The `NowAssistMajorIssueExtPoint` extension point exposes three methods that you can override.

|Method|OOB default|Purpose|
|------|-----------|-------|
|`isValid(glideRecord)`|Returns `true` for all cases|Pre-flight eligibility check called before skill invocation. Override to exclude specific case types, domains, or any other condition.|
|`getConfigForMajorCase(glideRecord)`|limit: 10, threshold: 0.75|Returns the search configuration used when scanning for existing major cases.|
|`getConfigForNonMajorCase(glideRecord)`|limit: 10, threshold: 0.70|Returns the search configuration used when scanning for similar non-major cases.|

