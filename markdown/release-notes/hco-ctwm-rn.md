---
title: Care Team Work Management release notes
description: The ServiceNow Care Team Work Management application enables clinicians to create and track ad-hoc and recurring tasks for their care team. It supports orchestration and care team cases and tasks.The ServiceNow Care Team Work Management application enables clinicians to create and track ad-hoc and recurring tasks for their care team. Tasks are managed through orchestration and care team cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/hco-ctwm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Healthcare and Life Sciences release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Care Team Work Management release notes

The ServiceNow® Care Team Work Management application enables clinicians to create and track ad-hoc and recurring tasks for their care team. It supports orchestration and care team cases and tasks.

## About Care Team Work Management

-   Create ad-hoc or recurring scheduled task plans for care teams across one or more units.
-   Use the unified workspace landing page for managing cases and tasks.
-   Streamline rounding workflows and reduce administrative burden by leveraging the Operational Rounding playbook.
-   Standardize recurring unit-level work, such as daily safety checks or shift readiness reviews, with the Care team activities playbook.

See  for more information.

## Activation and other requirements

**Important:** Care Team Work Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Care Team Work Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/healthcare-life-sciences-rn-landing.md)

## Brazil

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


