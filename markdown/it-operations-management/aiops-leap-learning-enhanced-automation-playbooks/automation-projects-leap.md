---
title: Automation projects
description: Use Automation projects to analyze multiple sets of incident data independently, so different teams or business units can derive separate insights and automation opportunities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/automation-projects-leap.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 5
breadcrumb: [Explore, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Automation projects

Use Automation projects to analyze multiple sets of incident data independently, so different teams or business units can derive separate insights and automation opportunities.

An Automation project defines the scope and configuration for LEAP analysis. Each project runs independently and can target specific assignment groups, time periods, or filtered sets of incidents. By creating multiple Automation projects, you can analyze different categories of incidents separately and generate automation opportunities tailored to each context.

## Benefits of Automation projects

Automation projects provide the following benefits:

-   Team-specific insights: Different teams or business units can work on separate projects concurrently without affecting each other's analysis, metrics, or automation opportunities.
-   Analyze multiple data sets independently: Create separate projects to analyze different groups of incidents based on assignment groups, time periods, or other criteria. For example, analyze the last 6 months of Human Resources incidents in one project while creating a focused project for last month's spike in cases.
-   Flexible taxonomy configuration: Select one or more taxonomies per project to group incidents according to your team's classification needs. Multiple projects can use the same taxonomy when analyzing different subsets of data.
-   Real-time dashboard views: Switch between projects to view project-specific metrics, reports, and automation opportunities in the dashboard.
-   Configurable analysis schedule: Schedule analysis jobs to run at specified frequencies for each project independently.

Each Automation project has its own independent configuration: incident, filter, grouping column, taxonomy selection, job frequency, and settings. Projects run without affecting each other.

## When to use Automation projects

The following examples illustrate common scenarios where creating multiple Automation projects provides more relevant and actionable results than a single shared project.

-   **Per-team automation**

    A large IT organization wants Network team incidents grouped and automated separately from Database team incidents. Because issue patterns, root causes, and resolution steps differ significantly between teams, each team gets its own project instead of a single mixed pool of recommendations.

-   **Per-region automation**

    A global company wants automation tuned separately for APAC and EMEA support teams. Ticket volume, categories, and SLAs vary by region, so separate projects confirm that grouping and recommendations reflect each region's specific incident patterns.

-   **Per-service-tier automation**

    A customer wants to separate automation for critical Tier-1 services, such as banking systems and core infrastructure, from general Tier-2 and Tier-3 services. Keeping high-priority incidents in a dedicated project prevents lower-priority noise from diluting the grouping and resolution logic for business-critical systems.

-   **Controlled pilot before a wider rollout**

    A customer wants to try LEAP automation on one team's data first before expanding to the rest of the organization. Creating a separate project for the pilot team keeps the trial isolated from the default project that is already running in production.

-   **Business unit isolation**

    A company with multiple business units, each using ServiceNow with different assignment groups, wants each unit to see automation results relevant only to their own incidents. Separate projects scoped by assignment group ensure that each business unit's recommendations are not mixed with those of other units.

-   **Testing and sandbox configuration**

    An administrator wants to test grouping or filter changes safely before applying them to the production setup. A separate project scoped to a small filtered set of records acts as a sandbox, leaving the default project and its running jobs unaffected.


## Default Automation project

The Default Automation project is shipped with the LEAP. The Default project represents the existing pre-multi-project setup and has no taxonomy configuration and is read-only. You can view its configuration but can't edit it from the Automation project details page. To change the default configuration, use the AI Admin Workspace.

**Note:**

-   The initial setup experience for LEAP remains unchanged. When you first activate LEAP, you must still configure the default project through the AI Admin Workspace. Automation projects is an additional capability that is available after the default project is set up.
-   Skill activation occurs in the AI Admin workspace.

Automation projects are an opt-in capability. Existing deployments continue to work without modification. You don't have to migrate your current configuration to use Automation projects. Adding a new project does not change the Default Automation project or any currently running analysis jobs.

## Automation project lifecycle

Managing Automation projects involves creating new projects, running analysis jobs, and switching between projects to view different automation opportunities. The following workflow describes the complete lifecycle:

1.  Create the project: Define the project name, description, table, filter, grouping column, topic column, taxonomy/assignment group, and job frequency. The project is created in a **ready \(editable\)** state and can be viewed directly on the projects details screen or the homepage. No analysis runs at this point.
2.  Start the grouping job: After the project configuration is complete, start the analysis job. Starting the job clones the required skills in the back end and activates the scheduled job. Once analysis begins, the project configuration can't be edited until the job completes or the job status is *ready* or *failed*.
3.  Review automation opportunities: After the analysis completes, review automation opportunities, create resolution steps, and measure impact. The day-to-day experience is the same as the standard LEAP workflow.
4.  Switch between projects: Switch between projects to view different sets of automation opportunities. Switching between projects updates data on every page and the LEAP value dashboard to reflect the selected project's data set.
5.  Edit project configurations: Edit project configurations as needed. You can only edit a project when its job status is *ready* or *failed*.

## Configuration constraints

When configuring an Automation project, be aware of the following constraints:

-   The taxonomy field is multi-select. You can select one or more taxonomies to define which incident groups the project analyzes.
-   Multiple projects can use the same taxonomy. When an incident matches multiple projects, playbooks from all matching projects are displayed.
-   Filter queries are limited to 300 characters. Filters that return zero records are marked as an error before the project is saved.
-   This release supports only the incident table.

## Taxonomy filtering

Selected taxonomies dictate the filter query for an Automation project. For example, if you select assignment groups AG1 and AG2, the system creates a filter where the assignment group is one of AG1 or AG2.

## Prediction logic

When an incident is created or updated, LEAP determines which Automation projects run predictions based on the incident's assignment group:

-   The Default Automation project always runs predictions regardless of the assignment group.
-   If an incident has a specific assignment group, predictions run on the Default project plus any Automation projects that match that assignment group.

