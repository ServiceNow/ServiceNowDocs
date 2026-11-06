---
title: L1 IT Service Desk AI Specialist release notes
description: The ServiceNow L1 IT Service Desk AI Specialist application is an autonomous worker that investigates and resolves incidents end-to-end without human intervention. It's designed to support high-volume, repeatable L1 incidents enabling a live human agent to handle more complex issues. For incidents that come in as requests, the appropriate request item, such as software access, is proposed. The L1 IT Service Desk AI Specialist is a new application in the Zurich release. See the following sections for release notes by version.Adds performance dashboard enhancements, cross-group reassignment outcome tracking, and requester portal configuration, and removes the routing journey count cards, Research depth, and Pre resolution condition settings.The L1 IT Service Desk AI Specialist has been updated.The L1 IT Service Desk AI Specialist is a new application in ServiceNow Otto for IT Service Management \(ITSM\) in the Zurich release.The L1 IT Service Desk AI Specialist is a new application in ServiceNow Otto for ITSM in the Zurich release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/l1-it-service-desk-ai-specialist-rn.html
release: zurich
topic_type: topic
last_updated: "2026-08-24"
reading_time_minutes: 5
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# L1 IT Service Desk AI Specialist release notes

The ServiceNow® L1 IT Service Desk AI Specialist application is an autonomous worker that investigates and resolves incidents end-to-end without human intervention. It's designed to support high-volume, repeatable L1 incidents enabling a live human agent to handle more complex issues. For incidents that come in as requests, the appropriate request item, such as software access, is proposed. The L1 IT Service Desk AI Specialist is a new application in the Zurich release. See the following sections for release notes by version.

## About L1 IT Service Desk AI Specialist

-   Helps increase efficiency by automating high-volume, repeatable L1 incidents.
-   Enables a human to intervene in the automated process, if needed.
-   Helps frees up live human agents to handle more complex issues.

See [L1 IT Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/l1-service-desk-ai-specialist.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install L1 IT Service Desk AI Specialist by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    Contact your ServiceNow account manager to get started with L1 IT Service Desk AI Specialist.

    **Note:** Domain separation is not supported on this version of L1 IT Service Desk AI Specialist.

-   **Additional requirements**

    Your instance must be on Zurich Patch 12.


## Accessibility and localization

-   **Localization information**

    Multi-language support for the L1 IT Service Desk AI Specialist may vary.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-service-management-rn-landing.md)

## Version 1.3 \| Zurich Patch 12

Adds performance dashboard enhancements, cross-group reassignment outcome tracking, and requester portal configuration, and removes the routing journey count cards, Research depth, and Pre resolution condition settings.

### What's new

-   **[Rate trend chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/perf-overview-l1-sd-ai-spec.md)**

    Track the durable auto-resolve and coverage rates over time with a Rate trend chart on the AI Specialist Performance dashboard, and select a day to see its incidents.

-   **[Overview funnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/perf-overview-l1-sd-ai-spec.md)**

    Follow incidents from assignment to eligible groups through durable resolution in a four-step funnel on the Overview tab. Drill down into each step, and use the calculation cards to see how each rate is worked out.

-   **[Cross-group reassignment outcomes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/cross-group-reassignment-l1-sd-ai-spec.md)**

    See what your service desk team did with cross-group reassignment recommendations in a chart that shows which were adopted, overridden, or are awaiting a decision.

-   **[Requester reference portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)**

    AI Admins can set the portal that knowledge article and catalog item links open in for requesters. Links in work notes for Service Desk Agents continue to open in the platform view.


### What's changed

-   **[Catalog variable collection and messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/catalog-variable-collection-slot-fill-l1-sd-ai-spec.md)**

    The L1 IT Service Desk AI Specialist now fills catalog item variables from the incident and the caller's details and shows requesters what it already captured, so requesters answer fewer questions. It also now uses dynamic response authoring for L1 IT Service Desk AI Specialist Catalog submission responses. Default instructions are provided so the agent composes each message fresh instead of relying on a fixed template.


### What's deprecated or removed

-   **[Routing journey count cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/perf-overview-l1-sd-ai-spec.md)**

    Removed. The Routing journey count cards are replaced by the funnel on the Overview tab.

-   **[Research depth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)**

    Removed. The unused Research depth setting is no longer available. There is no replacement.

-   **[Pre resolution condition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)**

    Removed. The Pre resolution condition setting is no longer available, and incidents are no longer checked against it. There is no replacement.


## Version 1.2 \| Zurich Patch 12

The L1 IT Service Desk AI Specialist has been updated.

### What's new

-   **[Configure L1 IT Service Desk AI Specialist tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/config-tasks-l1-sd-ai-spec-sow.md) Response Templates**

    AI Admins can switch response templates between a fixed template and dynamic mode, where the AI Specialist writes activity notes, customer comments, work notes, and close notes from free-form instructions the administrator provides.

-   **[Catalog request submission and tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/catalog-variable-collection-slot-fill-l1-sd-ai-spec.md)**

    The L1 IT Service Desk AI Specialist can resolve incidents by submitting service catalog requests on behalf of users. The L1 IT Service Desk AI Specialist collects the required details through guided questions, submits or drafts the request, and resolves the linked incident so users can track fulfillment through the request.

    L1 IT Service Desk AI Specialist now uses dynamic response authoring for ZTS Action Agent and Catalog submission responses. Default instructions are provided so the agent composes each message fresh instead of relying on a fixed template.

-   **[Catalog performance analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/catalog-tab-l1-sd-ai-spec.md)**

    A new Catalog tab on the AI Specialist performance dashboard shows drafted, submitted, abandoned, and canceled request volumes by catalog item. This gives administrators visibility into how well the AI Specialist is handling catalog-based resolutions.

-   **[AI Quality assessment for L1 IT Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/qa-l1-sd-ai-spec.md)**

    Evaluate L1 IT Service Desk AI Specialist's work, captured in a coaching assessment against the rubric defined on the coaching opportunity by using the AI Quality Assessment skill to get consistent, objective scoring.


## Version 1.1

The L1 IT Service Desk AI Specialist is a new application in ServiceNow Otto for IT Service Management \(ITSM\) in the Zurich release.

### What's new

-   **[Routing criteria configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)**

    Enable hand-offs between the AI specialist and human agents if work is better handled by a different group or requires additional human oversight.

-   **[Routing decision criteria over time analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/perf-overview-l1-sd-ai-spec.md)**

    Shows how many incidents over time were reassigned because routing decision criteria matched.

-   **[Performance quality assessment analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/perf-quality-l1-sd-ai-spec.md)**

    Review how the AI Specialist measures up in each quality area using automatically generated quality assessments. You can monitor scores, compare different coaching opportunities, and pinpoint areas where quality can be enhanced.


## Version 1.0

The L1 IT Service Desk AI Specialist is a new application in ServiceNow Otto for ITSM in the Zurich release.

### What's new

The L1 IT Service Desk AI Specialist is an autonomous worker that helps handle incidents end-to-end without human intervention. It uses knowledge articles and historical data to investigate and resolve high-volume, repeatable level 1 \(L1\) incidents. It communicates directly with requesters and escalates incidents to human agents when confidence is low.

-   ****

    Choose from two types of execution modes for the L1 IT Service Desk AI Specialist during configuration or activation, Autonomous or Supervised. The execution mode of the L1 IT Service Desk AI Specialist determines its autonomy when performing tasks on incidents. You can change the execution mode at any time.

-   **[Configure the L1 IT Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/configuring-l1-sd-ai-specialist.md)**

    Configure how the L1 IT Service Desk AI Specialist works an incident across each stage of its task pipeline from classifying and assigning fields to which team or whom it reassigns incidents. Each stage is configurable, so you control how incidents are handled from intake to resolution.

-   **[View the performance of the L1 IT Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/perf-l1-sd-ai-spec.md)**

    Review performance analytics for the L1 IT Service Desk AI Specialist to track task execution success. You can use analytics to help make choices to tune the L1 IT Service Desk AI Specialist to suit your exact business needs.

-   **[View the activity of the L1 IT Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/activity-l1-sd-ai-spec.md)**

    View the task execution history of the L1 IT Service Desk AI Specialist to track where and when it is planning and attempting executions. You can also give feedback on its performance.


