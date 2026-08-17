---
title: Schedule a job to generate TLM technology risk
description: Execute the Populate Technology Lifecycle Risks scheduled job to generate the TLM technology lifecycle risks and populate the result in the TLM Technology Lifecycle Risks \[sn\_apm\_tpm\_technology\_risk\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-schedule-job-generate-tpm-risk.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with Technology Lifecycle Management \(TLM\) in EA Workspace, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Schedule a job to generate TLM technology risk

Execute the **Populate Technology Lifecycle Risks** scheduled job to generate the TLM technology lifecycle risks and populate the result in the TLM Technology Lifecycle Risks \[sn\_apm\_tpm\_technology\_risk\] table.

## Before you begin

Role required: admin

## About this task

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

The scheduled job populates the risk scores for business applications \(BA\), application services \(AS\), software products, and hardware models. The scores are calculated for a fiscal period of type month in the Technology lifecycle risks \(sn\_apm\_tpm\_technology\_risk\) table.

The scores of software products and hardware models are calculated based on their lifecycle dates \(EOS, EOES, EOL\), where 100 is the maximum score. The sum of the related software and hardware risk score is the risk score of an application service. And, the sum of the related application service risk score is considered as the risk score of a business application.

These risk scores are displayed in the risk column of a TLM Gantt chart. The same scores for a business application is served as an application weight for calculating Technology Lifecycle Risk indicator score for a fiscal period.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

2.  Find and select the **Populate Technology Lifecycle Risks** scheduled job.

3.  Select **Execute Now**.


**Parent Topic:**[Working with Technology Lifecycle Management \(TLM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-work-with-tpm.md)

