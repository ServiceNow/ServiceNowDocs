---
title: Create an Automation project
description: Create an Automation project to run LEAP analysis on a specific set of incident data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/create-automation-project.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [automation project, multi-taxonomy, LEAP configuration]
breadcrumb: [Manage automation projects, Use, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Create an Automation project

Create an Automation project to run LEAP analysis on a specific set of incident data.

## Before you begin

Role required: LEAP admin \(`sn_itom_leap.leap_admin`\)

## About this task

Each Automation project runs LEAP analysis independently on a specific set of incident data. You can create multiple projects to analyze different incident categories, assignment groups, or time periods. Multiple projects can use the same taxonomy when analyzing different data sets.

## Procedure

1.  Navigate to the **Manage Automation projects** page.

    \[Omitted image "manage-automation-projects-page.png"\] Alt text: Manage automation projects pageThe page displays all existing Automation projects as cards, including the Default Automation project.

2.  Select **New configuration**.

    The **Automation Project Details** page opens in create mode.\[Omitted image "new-automation-project.png"\] Alt text: New automation project configuration

3.  Complete the following fields:

    -   Name: Enter a unique name for the project.
    -   Description: \(Optional\) Describe the purpose of this project.
    -   Table: Select the incident table to analyze. Only the incident table is supported in this release.
    -   Filter: Define a filter to scope the incidents for this project. The filter must return at least one thousand records and can't exceed 300 characters.
    -   Grouping column: Select the column used to group incidents.
    -   Topic column: Select the column used to generate topics.
    -   Taxonomy: Select one or more taxonomies for this project. The taxonomy field is multi-select. Multiple projects can use the same taxonomy.
    -   Job frequency: Select how often the analysis job runs.
    Mandatory fields must be filled and the filter must return at least one record before you can start the job. Validation errors are displayed inline.

4.  Select **Submit**.

    The project is created in *ready* status. The analysis job has not started yet. You can edit the project configuration before starting the job.


## What to do next

After creating the project, start the analysis job to begin generating automation opportunities.

