---
title: Configure the Project Data Quality Analysis skill
description: Configure the Project Data Quality Analysis AI skill to enable it for your projects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/configure-data-quality-index-skill.html
release: brazil
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 1
breadcrumb: [Configure AI Admin features, Configuring Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure the Project Data Quality Analysis skill

Configure the Project Data Quality Analysis AI skill to enable it for your projects.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub** &gt; **AI Skills**

2.  On the navigation panel, select **Technology** and select **SPM**.

3.  On the Project Data Quality Analysis card, select **Edit Configuration**.

    The skill is active by default.

    Select **Data Quality Criteria** in the navigation panel. Review the rules for each project dimension in the skill.

    Project Data Quality Analysis evaluates projects across six dimensions: Charter, Schedule, Resources, Financials, Reporting, and RIDAC. Each dimension has its own criteria field, and a read-only list shows the full set of rules evaluated for that dimension.

4.  Switch the scope to ServiceNow Otto for Strategic Portfolio Management to customize the rating for each rule.

5.  Review how each dimension contributes to the composite score and update the weighting to match your organization's priorities.

6.  Select **Save and continue**.

7.  Select **Define access** in the navigation panel to view and edit ACL roles to access this skill.

    You can add required role in the Roles field. You must have at least one role specified who can access the skill.

8.  Select **Save and continue**.

9.  Select **Select display** in the navigation panel and select In-product desktop if you'd like to display the skill on forms and workspaces.

    Select in-product display to show the Data Quality Index widget on the AI Insights tab of Project Workspace.

10. Review your choices and select **Done** to complete the configuration.


## Result

The Project Data Quality Analysis skill is configured and ready to evaluate project data quality.

**Parent Topic:**[Configure AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-workspace/configuring-na-spm.md)

