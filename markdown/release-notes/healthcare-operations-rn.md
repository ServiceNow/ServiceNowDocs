---
title: Healthcare Operations release notes
description: The ServiceNow Healthcare Operations family helps care teams manage operational requests across the hospital: Care Team Work Management, Care Team Portal, Care Team Mobile, the Care Team Operations for Biomed, Care Team Operations for Environmental Services, Care Team Operations for Facilities, and Care Team Operations for Healthcare IT apps, and the Healthcare Operations Core data model they share.The ServiceNow Care Team Work Management application enables clinicians to create and track ad-hoc and recurring tasks for their care team. Tasks are managed through orchestration and care team cases.The ServiceNow Healthcare Operations family helps care teams manage operational requests across the hospital, including Care Team Work Management, Care Team Mobile, and a dedicated AI chat and voice assistant for case intake and creation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/healthcare-operations-rn.html
release: brazil
topic_type: topic
last_updated: "2026-10-01"
reading_time_minutes: 3
breadcrumb: [Healthcare and Life Sciences release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Healthcare Operations release notes

The ServiceNow® Healthcare Operations family helps care teams manage operational requests across the hospital: Care Team Work Management, Care Team Portal, Care Team Mobile, the Care Team Operations for Biomed, Care Team Operations for Environmental Services, Care Team Operations for Facilities, and Care Team Operations for Healthcare IT apps, and the Healthcare Operations Core data model they share.

## About Healthcare Operations

-   Create ad-hoc or recurring scheduled task plans for care teams across one or more units with Care Team Work Management. See  for more information.
-   Submit and track operational requests from a self-service Care Team Portal.
-   Create, assign, and edit care team cases and tasks from Care Team Mobile. See  for more information.
-   Route and fulfill department-specific requests through the Care Team Operations for Biomed, Care Team Operations for Environmental Services, Care Team Operations for Facilities, and Care Team Operations for Healthcare IT apps.
-   Use a dedicated ServiceNow Otto assistant, the Care Team Operations AI Chat Assistant, for conversational case intake and creation by chat or voice. See  for more information.

All of these apps build on the Healthcare Operations Core data model for locations, organizations, and departments.

## Activation and other requirements

**Important:** Healthcare Operations apps are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install each Healthcare Operations app by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    The Care Team Operations AI Chat Assistant and its agents require an HCLS Prime or HCLS Advanced scoped application.


**Parent Topic:**[Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/healthcare-life-sciences-rn-landing.md)

## September 2026

The ServiceNow® Care Team Work Management application enables clinicians to create and track ad-hoc and recurring tasks for their care team. Tasks are managed through orchestration and care team cases.

### What's new

-   **Care team activities playbook**

    Define a recurring or one-time activities plan once, such as a daily unit safety check or a routine equipment inspection. The system automatically generates care team cases and tasks for every selected team or unit according to a configured schedule.

    Unlike the Operational Rounding playbook, the Care team activities playbook works directly at the care team case and task level. It does not create a healthcare orchestration case, making it suited to single-unit, recurring operational work.

-   **Smart assessments**

    Associate a structured, repeatable questionnaire with a care team task to capture standardized evidence, such as room inspections, equipment checks, or readiness surveys. Assessments can also be associated with task plan templates so that every concrete task generated from the template automatically inherits the assessment. Results can be reviewed, compared, and reported on across a unit, an organization, or an entire hospital.

    This feature depends on the Smart Assessment for CSM plugin, which is automatically installed with Care Team Work Management.


### What's changed

-   **Healthcare Orchestration roles**

    Two new roles, `sn_hco_orc.loc_contributor` \(Healthcare Orchestration Location Contributor\) and `sn_hco_orc.loc_manager` \(Healthcare Orchestration Location Manager\), can now be assigned directly as a service organization member's type.

    Location-level and hospital-level visibility and management permissions for orchestration functions resolve automatically, without requiring the Care Team Agent Manager role as a workaround.


## October 2026

The ServiceNow® Healthcare Operations family helps care teams manage operational requests across the hospital, including Care Team Work Management, Care Team Mobile, and a dedicated AI chat and voice assistant for case intake and creation.

### What's new

-   **Care Team Operations AI Chat Assistant**

    A dedicated ServiceNow Otto assistant, pre-configured for Care Team Operations, lets care team members report and create operational requests by chat or voice without navigating the general Virtual Agent. The assistant surfaces the Care team operations case intake and case creation AI agents, and the Request care team assistance agentic workflow, as a single conversational entry point.

    If Care Team Mobile is installed, the assistant is automatically extended to mobile with its own nav-tab channel.

-   **Case and task management from Care Team Mobile**

    Create, assign, and edit care team cases and tasks directly from Care Team Mobile. Care team agents can also complete tasks, including attached smart assessments, through FSM Mobile.


### What's changed

-   **User criteria for Care Team Mobile quick actions**

    Six out-of-the-box user criteria records ship with Care Team Operations so admins can control which Care Team Mobile quick-action icons each care team role sees, instead of building their own user criteria from scratch.


