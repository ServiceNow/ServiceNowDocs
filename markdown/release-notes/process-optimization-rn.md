---
title: Process Mining release notes
description: The ServiceNow Process Mining application helps analysts and process owners quickly analyze and optimize their business processes.The Brazil release delivers meter-based usage guardrails and a redesigned evaluation project experience so you can control costs and explore Process Mining risk-free. This release also adds automatic content packs and template management capabilities, deeper playbook analytics, and quick starters for transition and finding filters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/process-optimization-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Platform Analytics release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Process Mining release notes

The ServiceNow® Process Mining application helps analysts and process owners quickly analyze and optimize their business processes.

## About Process Mining

-   See your real processes, not assumptions — automated discovery maps actual workflow paths from audit logs.
-   Find where work breaks down — bottleneck and root-cause analysis pinpoint stalled approvals and rework.
-   Accelerate value with proven templates — best-practice content packs give you ready-made starting points.
-   Prove every change works — side-by-side comparisons confirm improvements and catch regressions.
-   Govern humans and AI, together — trace performance across people, automations, and AI agents in one view.

See [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining.md) for more information.

## Activation and other requirements

-   **Activation information**

    Process Mining is available by default. For details, see [Access Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/activate-po-plugin.md).


**Parent Topic:**[Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/analytics-intel-report-rn-landing.md)

## Brazil Early Availability

The Brazil release delivers meter-based usage guardrails and a redesigned evaluation project experience so you can control costs and explore Process Mining risk-free. This release also adds automatic content packs and template management capabilities, deeper playbook analytics, and quick starters for transition and finding filters.

### What's new

-   **[Meter-based usage guardrails and controls introduced](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/meter-based-guardrails.md)**

    Configure table-level guardrails and mandatory filters to control entitlement usage and prevent unexpected overage charges. Projects with configured guardrails are automatically validated, capped, or flagged before mining starts.

-   **[Process Mining for Playbooks enhanced](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/playbook-project.md)**

    Playbook projects are enhanced:

    -   to configure and analyze breakdowns based on the trigger record of a playbook
    -   to filter playbook executions by recency to focus on current performance trends
    -   to view execution-time histograms for each activity and phase to identify performance patterns and outliers
    -   to compare playbook variants on overall and per-activity efficiency
-   **[Evaluation project experience improved](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/evaluate-pm.md)**

    Explore evaluation projects directly from the Process Mining workspace landing page, with guided onboarding that highlights key areas of the interface and suggests where to start exploring. Human Resources and Security Operations users get personal evaluation projects scoped to their own data access, so no administrator impersonation is required.

-   **[AI-assisted process configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/gen_process_config_ai.md)**

    Generate process configuration field values with AI directly from the process configuration header, then review, select, and confirm the suggested fields before applying them. Map states to stakeholder responsibilities with AI in the Process details step.

-   **[Launch Process Mining from any ServiceNow workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/list-proj-crt.md)**

    Create a Process Mining project directly from a list of records from any ServiceNow workspace.

-   **[Project sharing with edit rights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/share-project.md)**

    Share a project with other users as **Can view** or **Can edit**. Users with edit rights can modify the project definition and perform mining, but can't share or delete the project.

-   **[Contextual Task Mining project names](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/task-mining-naming.md)**

    Task Mining projects launched from Process Mining include the triggering node or improvement opportunity name in the project name, making it easier to distinguish between multiple task mining projects.

-   **[Template creation and management introduced](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/pm_templates.md)**

    Create multiple templates per table to support several distinct use cases instead of one generic configuration.

-   **[Preset filters for transitions introduced](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/filter-auto.md)**

    Create filters from the available filters after selecting the Select quick starter from Process steps in Analyst workbench. This makes the process of creating filters easier and faster.

-   **[Three new system properties added](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/components-installed.md)**

    The following three system properties are added:

    -   promin.metered\_usage.allow\_unrestricted
    -   promin.metered\_usage.warning\_limit
    -   promin.workspace.hide\_from\_navigation

### What's changed

-   **[Content packs availability changed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining-content-pack-delivery.md)**

    Access content packs for the following automatically when the corresponding application plugin is active and the associated table is present:

    -   IT Service Management
    -   Customer Service Management
    -   HR Service Delivery
    -   Strategic Portfolio Management
    -   Security Incident Response
    -   Field Service Management

### What's deprecated or removed

-   **Two APIs deprecated**

    The following two APIs are deprecated:

    -   promin.api.allow\_no\_role\_mining
    -   promin.api.auto\_share\_project\_with\_creator

### Plugin information

-   **Renamed or changed plugins**

    Now Assist for Process Mining: Renamed to ServiceNow Otto for Process Mining.


