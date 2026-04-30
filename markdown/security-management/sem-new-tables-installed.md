---
title: Security Exposure Management Workspace Tables
description: The following are the tables installed with Security Exposure Management. These tables store Security Exposure Management-related configuration, rules, findings, and other data required for exposure assessment, remediation, scoring, and exception management.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-08-11"
reading_time_minutes: 2
breadcrumb: [Security Exposure Management Workspace Components, Reference, Unified Security Exposure Management, Security Operations]
---

# Security Exposure Management Workspace Tables

The following are the tables installed with Security Exposure Management. These tables store Security Exposure Management-related configuration, rules, findings, and other data required for exposure assessment, remediation, scoring, and exception management.

|Application|Table|Description|
|-----------|-----|-----------|
|Administration for Security Exposure Management|Assignment Rule \[sn\_sec\_wf\_assign\_rule\]|Contains the set of rules evaluated to set the assignment group on findings.|
|Administration for Security Exposure Management|Classification Group \[sn\_sec\_wf\_classification\_group\]|Stores classification group configurations for grouping related classification rules.|
|Administration for Security Exposure Management|Classification Rule \[sn\_sec\_wf\_classification\_rule\]|Stores classification rules that categorize findings based on defined conditions.|
|Administration for Security Exposure Management|Remediation Status \[sn\_sec\_wf\_m2m\_ttr\_status\]|Stores status, rule and findings mapping for approaching and past due findings.|
|Administration for Security Exposure Management|Remediation Target Rules \[sn\_sec\_wf\_ttr\_rule\]|Stores remediation target rules that define remediation timeframes, notifications, and applicable conditions for findings.|
|Administration for Security Exposure Management|Rollup Config \[sn\_sec\_wf\_rollup\_config\]|List of vulnerability rollup calculators.|
|Exception Management for Unified Security Exposure Management|Change Approval \[sn\_sec\_exception\_change\_approval\]|Stores approval records with details on the reason and findings for each request, approval status, approver information, and related questionnaire.|
|Exception Management for Unified Security Exposure Management|Exception Management Configuration \[sn\_sec\_exception\_config\]|Stores the configuration settings for the exception management feature.|
|Exception Management for Unified Security Exposure Management|Exception Rule \[sn\_sec\_exception\_rule\]|Stores rules for automatically deferring findings based on matching criteria and execution order in exception management.|
|Exception Management for Unified Security Exposure Management|Policy Exception Reason Mapping \[sn\_sec\_exception\_policy\_reason\_mapping\]|Maps policy exception reasons to their corresponding reasons in Vulnerability Response and Configuration Compliance.|
|Exception Management for Unified Security Exposure Management|Questionnaire Configuration \[sn\_sec\_exception\_questionnaire\_config\]|Stores questionnaire templates used for exception assessments.|
|Remediation for Attack Surface Management|Remediation Task Rule \[sn\_sec\_rem\_task\_rule\]|Contains the rules that define the criteria with which groups are automatically created for a set of findings.|
|Risk Scoring for Security Exposure Management|Calculator Configuration \[sn\_sec\_calculator\_config\]|Stores configuration settings for risk calculators, including scoring logic.|
|Risk Scoring for Security Exposure Management|Risk Calculator \[sn\_sec\_calculator\_group\]|Groups related risk rules, which are evaluated in order to calculate risk score.|
|Risk Scoring for Security Exposure Management|Risk Calculator Rule \[sn\_sec\_calculator\_rule\]|Stores risk rules that calculates risk score on findings based on defined conditions.|
|Risk Scoring for Security Exposure Management|Risk rule field \[sn\_sec\_calculator\_risk\_field\]|Stores scoring criteria defined under a risk rule, containing weightage and weight breakdowns on field values.|
|Risk Scoring for Security Exposure Management|Risk Score Weight \[sn\_sec\_calculator\_risk\_score\_weight\]|Stores risk score range to risk rating mapping.|
|Security Exposure Management|Dashboard \[sn\_sec\_sem\_dashboard\]|Stores configuration for dashboards used in findings view.|
|Security Exposure Management|Widget Aggregation \[sn\_sec\_sem\_m2m\_widget\_dashboard\]|Stores mapping between widgets, findings table, aggregation, and dashboards data.|
|Security Exposure Management|Widget Grouping \[sn\_sec\_sem\_widget\_grouping\]|Stores widget group definitions for aggregations associated with selected dashboard widgets.|

**Parent Topic:**[Security Exposure Management Workspace Components](../concept/sem-components-installed.md)

