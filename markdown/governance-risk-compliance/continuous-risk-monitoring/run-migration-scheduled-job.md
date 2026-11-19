---
title: Run migration scheduled job
description: Run the migration scheduled job to associate existing authorization packages and boundaries with the workflow after enabling the CAM workflow configuration property. The migration confirms that existing data is compatible with the workflow configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/continuous-risk-monitoring/run-migration-scheduled-job.html
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 1
breadcrumb: [CAM workflow configuration, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Run migration scheduled job

Run the migration scheduled job to associate existing authorization packages and boundaries with the workflow after enabling the CAM workflow configuration property. The migration confirms that existing data is compatible with the workflow configuration.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**.

2.  Enter **Migrate to CAM Workflow Configurator** in the **Name** filter search bar to search for the CAM workflow migration-scheduled jobs.

3.  Select **Migrate to CAM Workflow Configurator** from the scheduled job search list.

4.  Verify the scheduled job details.

5.  Select **Execute Now** to confirm execution.


**Related topics**  


[GRC state model configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/continuous-risk-monitoring/cam-create-state-model.md)

[Workflow configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/continuous-risk-monitoring/work-configuration.md)

