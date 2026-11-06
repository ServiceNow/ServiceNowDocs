---
title: Business Continuity Management release notes
description: The ServiceNow Business Continuity Management application enables your organization to deliver products and services at an acceptable level during disruptive incidents. See the following sections for release notes by version.Business Continuity Management, version 12.0.x enhances collaboration between recovery teams and integrates GRC issues in plans and events. You can assign user groups as owners of business impact analysis \(BIA\), plans, and events, while importing and exporting recovery tasks to Microsoft Excel for streamlined workflows. To further strengthen your business continuity management capabilities, ServiceNow Otto for Integrated Risk Management \(IRM\) helps summarize issues in plans and events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/grc-business-continuity-management-rn.dita.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Governance, Risk, and Compliance release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Business Continuity Management release notes

The ServiceNow® Business Continuity Management application enables your organization to deliver products and services at an acceptable level during disruptive incidents. See the following sections for release notes by version.

## About Business Continuity Management

-   Plan, test, and maintain business continuity and disaster recovery strategies to verify organizational resilience across critical business functions and dependencies.
-   Coordinate cross-functional response activities, manage incidents, and track recovery objectives with centralized visibility into business impact and recovery time metrics.

See [Business Continuity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/business-continuity-mangmt-overview.md) for more information.

## Activation and other requirements

**Note:** Business Continuity Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Business Continuity Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.


## Accessibility and localization

-   **Accessibility information**
    -   Accessibility improvements were made to Business Continuity Management \(BCM\) pages and components. Updates include accessible names for buttons and interactive elements across Crisis map, Gantt view, Event tasks, Asset dependencies, and Business continuity planning pages. Keyboard navigation was corrected for forms and recovery task pages. These updates benefit users who rely on screen readers, keyboard-only users, and users of other Assistive Technology \(AT\).
    -   Reflow support for BCM: Content can be zoomed up to 400% through your browser settings, with page layouts automatically transforming into a vertical, stacked view without loss of content or functionality. This enhancement helps users with low vision or who have trouble seeing web content due to monitor size, device type, poor lighting, or other situations.

**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## Version 12.0.x

Business Continuity Management, version 12.0.x enhances collaboration between recovery teams and integrates GRC issues in plans and events. You can assign user groups as owners of business impact analysis \(BIA\), plans, and events, while importing and exporting recovery tasks to Microsoft Excel for streamlined workflows. To further strengthen your business continuity management capabilities, ServiceNow Otto for Integrated Risk Management \(IRM\) helps summarize issues in plans and events.

### What's new

-   **[Assign group ownership to business impact analysis, plan, and event records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/group-ownership-bias.md)**

    Enable group ownership for business impact analysis \(BIA\), plan, and event records along with individual ownership.

    Use the **My group's pending tasks** and **My group's items** tabs, added to the My Tasks page, to view group-owned records.

-   **[BIA owner and contributor synchronization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/group-ownership-bias.md)**

    Automatically sync the BIA owner, members of BIA owner group, and BCM lead with the Smart Assessment when a BIA is created. After the BIA is created, added BIA contributors are automatically synced to all associated Smart Assessment' contributors.

-   **[Enable integration of the GRC Issue module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/managing-issues-in-bcm.md)**

    Use the **Issues** tab in plan and event records to create GRC issues or link existing issues in Business Continuity Workspace. It helps you track issue sources automatically and maintain proper access control.

-   **[Report and summarize issues with ServiceNow Otto for IRM generative AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/bcm-exploring-ai-skills.md)**

    Report and summarize GRC issues faster with ServiceNow Otto for IRM. Issue Summarization and Issue Validation are available across BCM Foundation and BCM Advanced tiers. Automated Resolution Planning is available in BCM Advanced tier. These capabilities enable you to track issue status from discovery through closure from the Employee Center in an instance or from plan and event records in Business Continuity Workspace.

-   **[Import and export recovery tasks from Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/using-export-import-feature-recovery-tasks.md)**

    Upload recovery tasks in bulk using Microsoft Excel files, with row-level validation and error handling. Microsoft Excel columns are mapped to recovery task fields, to validate data integrity, support updates to existing tasks, and insert new tasks in the same import.

    Use the **Export to Excel** action to download current recovery tasks as a Microsoft Excel workbook for offline editing or sharing. Transform history and Import log related lists provide traceability of the most recent import run, including row-level errors and skipped records.

    Reorder recovery tasks in the Gantt view by linking task dependencies with drag-and-drop actions. If the linked order is invalid, an error message is displayed. Planners can reorder tasks for their own plans, while program managers can reorder tasks for all plans.

-   **[Enhance collaboration between recovery teams during a crisis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/creating-collaboration-threads-in-crisis.md)**

    Enable BCM users to create and manage recovery teams with users, groups, and hierarchies for coordinated crisis response. Tag events by escalation level \(Site, Regional, Corporate, Global\) and link recovery teams to track who's involved at each level.

    Create collaboration threads within events to assign action items, track impacted assets, and communicate directly with team members. Auto-populate email recipients from recovery team membership for frictionless notifications. Propagate all team actions to the event activity stream for a complete visibility into the response timeline.


### What's changed

-   **[Group ownership](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/group-ownership-bias.md)**
    -   **BIA owner group** field appears on the BIA form, the **Plan owner group** field appears on the plan form, and the **Assignment group** field appears on the exercise and crisis event forms.
    -   The **My group's pending tasks** and **My group's items** tabs have been added to the My Tasks page to view group-owned records.
    -   Group ownership details for BIA, plan, and event records also appear in separate sections in the PDF and Microsoft Word reports.
-   **[Integrate Issues in plan and event records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/add-or-create-issue-from-plan-uib-ws.md)**
    -   The **Issues** tab is added to the plans and event records.
    -   The Issues details section is added to the PDF and Microsoft Word reports showing the Issue name, description, and number.
-   **[Import and export recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/using-export-import-feature-recovery-tasks.md)**
    -   **Import from Excel** and **Export to Excel** UI actions are added to the Recovery tasks related list.
    -   The Microsoft Excel workbook contains the Recovery task, Instructions, Plan details sheets.
-   **[Enhance collaboration between recovery teams during a crisis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/creating-collaboration-threads-in-crisis.md)**
    -   The Recovery teams list \(name, description, location\) and form with parent and child hierarchy, Users and Groups lists, and Department column are added.
    -   The **Compose email** action and Email client template with recovery team members and members of linked groups are added.
    -   The Attachments and Emails related lists are added in the collaboration thread with email preview screen and activity stream integration.
    -   The Activities section is added in the Events form that lists all the events and related information.
    -   A Collaboration threads section is added to PDF and Microsoft Word reports showing thread name, description, impacted assets, recovery teams, and escalation level.

### What's deprecated or removed

-   **Now LLM service deprecation**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **New plugins**

    Install the GRC: Issue Managementplugin to enable a redesigned issue management experience with configurable workflows, custom state models, issue approvals, and centralized administration.


