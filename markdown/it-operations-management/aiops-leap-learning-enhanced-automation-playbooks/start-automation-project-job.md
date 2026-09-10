---
title: Start the analysis job
description: Start the analysis job for an Automation project to begin generating automation opportunities and insights.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/start-automation-project-job.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [automation project, analysis job, LEAP configuration]
breadcrumb: [Manage automation projects, Use, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Start the analysis job

Start the analysis job for an Automation project to begin generating automation opportunities and insights.

## Before you begin

Role required: LEAP admin \(`sn_itom_leap.leap_admin`\)

## About this task

After creating an Automation project, you must start the analysis job to activate the scheduled analysis and begin generating automation opportunities. The project configuration is locked once the job starts.

## Procedure

1.  Open the Automation Project in the **Automation Project Details** page.

2.  Select **Start analysis**.

    LEAP generates the required grouping skills and activates the scheduled analysis job in the back end. The job status transitions from *ready* to *running*. \[Omitted image "start-group-analysis.png"\] Alt text: Start group analysis for new automation project


## Result

When the job completes, automation opportunities and insights for this project are available in the LEAP workspace.

\[Omitted image "automation-opportunities-success-automation-project.png"\] Alt text: Automation opportunities created successfully

