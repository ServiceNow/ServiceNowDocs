---
title: Schedule a job to generate TPM technology risk
description: Execute the  Populate Technology Lifecycle Risks scheduled job to generate the TPM technology lifecycle risks and populate the result in the TPM Technology Lifecycle Risks \[sn\_apm\_tpm\_technology\_risk\] table.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with Technology Portfolio Management \(TPM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Schedule a job to generate TPM technology risk

Execute the  **Populate Technology Lifecycle Risks** scheduled job to generate the TPM technology lifecycle risks and populate the result in the TPM Technology Lifecycle Risks \[sn\_apm\_tpm\_technology\_risk\] table.

## Before you begin

Role required: admin

## About this task

The scheduled job populates the risk scores for business applications \(BA\), application services \(AS\), software products, and hardware models for a fiscal period of type month in the Technology lifecycle risks \(sn\_apm\_tpm\_technology\_risk\) table.

The scores of software products and hardware models are calculated based on their lifecycle dates \(EOS, EOES, EOL\), where 100 is the maximum score. The sum of the related software and hardware risk score is the risk score of an application service. And, the sum of the related application service risk score is considered as the risk score of a business application.

These risk scores are displayed in the risk column of a TPM Gantt chart. The same scores for a business application is served as an application weight for calculating Technology Lifecycle Risk indicator score for a fiscal period.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler ** &gt; ** Scheduled Jobs** &gt; ** Scheduled Jobs**.

2.  Find and select the  **Populate Technology Lifecycle Risks** scheduled job.

3.  Select  **Execute Now**.


**Parent Topic:**[Working with Technology Portfolio Management \(TPM\) in EA Workspace](../../concept/eaw-concept/eaw-work-with-tpm.md)

