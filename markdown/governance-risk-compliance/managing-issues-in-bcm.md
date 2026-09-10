---
title: Managing issues from Business Continuity Workspace
description: Associate issues with business continuity plans to track problems identified during continuity planning. Create an issue or add an existing issue from the Issues related list on a plan record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/managing-issues-in-bcm.html
release: zurich
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 4
keywords: [BCM, issues, remediation, plan]
breadcrumb: [Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Managing issues from Business Continuity Workspace

Associate issues with business continuity plans to track problems identified during continuity planning. Create an issue or add an existing issue from the **Issues** related list on a plan record.

## Business continuity with issue management

-   **Prerequisites**

    The GRC: Profiles application must be installed as a prerequisite for issue management. For more information, see [Dependencies for integrating the Issues module with BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/issues-bcm-dependencies.md).

-   **Benefits**

    The GRC: Issue Management integration enables organizations to track, prioritize, and resolve issues throughout their life cycle, reducing resolution time and minimizing business impact. AI-powered insights accelerate root-cause identification, strengthen resilience planning, and support data-driven decisions to prevent future disruptions—maintaining critical operations and reducing downtime.

-   **Usage**

    Associate issues with business continuity plans and events to track problems identified during planning, exercises, and crisis events. Use the Issues related list in plan and event records to create a new issue or add an existing GRC issue and track it through resolution.


## Dependencies

Certain GRC applications are required for Issues integration with BCM:

-   GRC: Profiles, which provides issues and remediation
-   GRC: Issue Management
-   GRC: Advanced Core, which provides issue triage

The **Issues** related list appears when BCM and these GRC applications are installed.

For more information, see [Dependencies for integrating the Issues module with BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/issues-bcm-dependencies.md).

## Classification and source

When you create an issue from a plan, the issue is given the **Business continuity management** classification. The issue source and issue source reference are set to the plan that you created it from, which is set to the primary source of the issue.

\[Omitted image "create-issue-from-plan-record.png"\] Alt text: Create an issue from plan record.

When you add an existing issue to another plan, that plan is recorded as a secondary source of the issue.

## Relationship between an issue and a plan

The relationship between an issue and a plan is stored in a many-to-many table \[sn\_bcp\_m2m\_plan\_issue\] \(Plan related issues\) that brings the issue fields into the related list. Removing an issue from the related list removes only the association. It doesn't delete the issue record.

## Access

Adding or creating an issue requires write access to the plan, the same as for recovery tasks and loss scenarios. The list of issues that you can add shows the active issues that you have access to. You can't add or create an issue when the plan, recovery event, or exercise is in a state that doesn't allow edits, such as Archived.

Issue access by role is described in the following table and the following illustrations.

|Role|Access to issues|
|----|----------------|
|sn\_bcp.plan\_contributor|Read, write, and create|
|sn\_bcp.plan\_manager|Read, write, and create|
|sn\_bcp.plan\_viewer|Read only|
|sn\_recovery.event\_manager, sn\_recovery.event\_user|Read, write, and create|
|sn\_bcm.program\_manager|Read, write, and create|

**Note:**

When GRC: Profiles is installed, all roles in this table contain the sn\_grc.compliance\_assurance\_user role, except sn\_bcp.plan\_viewer, which contains the sn\_grc.compliance\_assurance\_reader role.

The role records show the contained roles for each role. The sn\_grc.compliance\_assurance\_user role or sn\_grc.compliance\_assurance\_reader role appear only when GRC: Profiles is installed.

\[Omitted image "issue-plan-contributor-role.png"\] Alt text: Plan contributor.\[Omitted image "issue-plan-manager-role.png"\] Alt text: Plan manager.\[Omitted image "issue-plan-viewer-role.png"\] Alt text: Plan viewer.\[Omitted image "issue-event-user-role.png"\] Alt text: Event user.\[Omitted image "issue-reco-event-mgr.png"\] Alt text: Event manager.

## Issues on crisis events and exercises

Recovery events and exercises support the same issue association as continuity plans. From an event or exercise record, use the **Issues** related list to create a new issue or add an existing issue. The issue is given the same classification and source reference behavior as an issue created from a plan.

## Viewing plans and events from the issue record

The issue record shows every plan, recovery event, or exercise linked to it as a related item. Where these appear depends on which applications are installed. When the Issue Management app is installed, plans, events, and exercises each appear as their own related-list category under Impacted items, with Add and Remove actions only. When only GRC: Profiles is installed, the plan, event, and exercise related lists appear directly on the classic issue form, also with **Add** and **Remove** only.

\[Omitted image "plans-tab-in-issue-record.png"\] Alt text: Plans tab in Issue record.\[Omitted image "exercise-added-from-issue-record.png"\] Alt text: Exercise added from Issue record.

The first plan or event that an issue is created from is set to its primary source. Every other plan or event you link afterward is recorded as a secondary source. Removing a plan or event from the issue record's related list removes only the association. The plan, event, and issue records aren't affected.

## Vertical page layout

BCM Administrators can group and arrange related lists in a vertical layout. It enables you to access connected data without scrolling through a traditional horizontal page layout.

The "Record page vertical template" \(sn-rec-pg-vertical\) and "GRC: Issue Management" applications are used as the core components for the enhanced layout. The Impacted Items section now groups related items for improved visibility and easier identification of affected items.

The "Record page vertical template" application is installed with GRC Base Workspace \(app-grc-base-workspace\). It manages related lists and UI pages on a record page within groups. Its template uses preset values that enable the page to work without complex configuration. It also controls how related information is organized and displayed when you view records in Business Continuity Workspace as shown in the example.

\[Omitted image "issue-events-impacted-items.png"\] Alt text: Impacted items.

**Related topics**  


[Issue modules in Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/bcm-issue-list-modules.md)

[Add or create an issue from a plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/add-or-create-issue-from-plan-uib-ws.md)

[Add or create an issue from an exercise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/add-or-create-issue-from-event-uib-ws.md)

[Dependencies for integrating the Issues module with BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/issues-bcm-dependencies.md)

