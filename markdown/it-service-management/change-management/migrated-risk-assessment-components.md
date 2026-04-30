---
title: Migrated risk assessment components
description: When you migrate a change risk assessment, the system maps records from legacy risk assessment to the new risk assessment tables.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Migrate to legacy change risk assessments, Analyze change request risk and impact rating, Reference section for Change Management, Change Management, IT Service Management]
---

# Migrated risk assessment components

When you migrate a change risk assessment, the system maps records from legacy risk assessment to the new risk assessment tables.

To create a functional risk assessment on the assessment framework, the system converts risk assessment records to the most logical equivalent assessment risk records. This may mean multiple assessment risk records are created from one legacy risk record.

|Risk assessment components|Change risk assessment components|
|--------------------------|---------------------------------|
|Assessment Main \[assessment\_main\]|Change Risk Assessment \[change\_risk\_asmt\]|
|Assessment Question \[assessment\_question\]|Assessment category \[asmt\_metric\_category\]|
|Assessment Metric \[asmt\_metric\]|
|Assessment Question Choice \[assessment\_question\_choice\]|Assessment metric definition \[asmt\_metric\_definition\]|
|Risk Assessment Thresholds \[risk\_assessment\_threshold\]|Assessment Thresholds \[change\_risk\_asmt\_threshold\]|
|Assessment Conditions \[assessment\_conditions\]|This is included in Change Management - Risk Assessment \[com.snc.change.risk\_assessment\].|

**Parent Topic:**[Migrate to legacy change risk assessments](../task/legacy-change-risk-assessment-migration.md)

