---
title: L1 IT Service Desk AI Specialist release notes
description: The ServiceNow L1 IT Service Desk AI Specialist application is an autonomous worker that investigates and resolves incidents end-to-end without human intervention. It's designed to support high-volume, repeatable L1 incidents enabling a live human agent to handle more complex issues. For incidents that come in as requests, it proposes the appropriate request item, such as a software access. See the following sections for release notes by version.Adds performance dashboard enhancements, cross-group reassignment outcome tracking, and requester portal configuration, and removes the routing journey count cards, Research depth, and Pre resolution condition settings.The L1 IT Service Desk AI Specialist has been updated.The L1 IT Service Desk AI Specialist is a new application in ServiceNow Otto for IT Service Management \(ITSM\) in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/l1-it-service-desk-ai-specialist-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# L1 IT Service Desk AI Specialist release notes

The ServiceNow® L1 IT Service Desk AI Specialist application is an autonomous worker that investigates and resolves incidents end-to-end without human intervention. It's designed to support high-volume, repeatable L1 incidents enabling a live human agent to handle more complex issues. For incidents that come in as requests, it proposes the appropriate request item, such as a software access. See the following sections for release notes by version.

## About L1 IT Service Desk AI Specialist

-   Helps increase efficiency by automating high-volume, repeatable L1 incidents.
-   Enables a human to intervene in the automated process, if needed.
-   Helps free up live human agents to handle more complex issues.

See  for more information.

## Activation and other requirements

-   **Activation information**

    Install L1 IT Service Desk AI Specialist by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    Contact your ServiceNow account manager to get started with L1 IT Service Desk AI Specialist.

    **Note:** Domain separation is not supported on this version of L1 IT Service Desk AI Specialist.


## Accessibility and localization

-   **Localization information**

    Multi-language support for the L1 IT Service Desk AI Specialist may vary.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/it-service-management-rn-landing.md)

## Version 1.3 \| Brazil Patch 0

Adds performance dashboard enhancements, cross-group reassignment outcome tracking, and requester portal configuration, and removes the routing journey count cards, Research depth, and Pre resolution condition settings.

### What's new

-   **Rate trend chart**

    Track the durable auto-resolve and coverage rates over time with a Rate trend chart on the AI Specialist Performance dashboard, and select a day to see its incidents.

-   **Overview funnel**

    Follow incidents from assignment to eligible groups through durable resolution in a four-step funnel on the Overview tab. Drill down into each step, and use the calculation cards to see how each rate is worked out.

-   **Cross-group reassignment outcomes**

    See what your service desk team did with cross-group reassignment recommendations in a chart that shows which were adopted, overridden, or are awaiting a decision.

-   **Requester reference portal**

    AI Admins can set the portal that knowledge article and catalog item links open in for requesters. Links in work notes for Service Desk Agents continue to open in the platform view.


### What's changed

-   **Catalog variable collection and messages**

    The L1 IT Service Desk AI Specialist now fills catalog item variables from the incident and the caller's details and shows requesters what it already captured, so requesters answer fewer questions. It also now uses dynamic response authoring for L1 IT Service Desk AI Specialist Catalog submission responses. Default instructions are provided so the agent composes each message fresh instead of relying on a fixed template.


### What's deprecated or removed

-   **Routing journey count cards**

    Removed. The Routing journey count cards are replaced by the funnel on the Overview tab.

-   **Research depth**

    Removed. The unused Research depth setting is no longer available. There is no replacement.

-   **Pre resolution condition**

    Removed. The Pre resolution condition setting is no longer available, and incidents are no longer checked against it. There is no replacement.


## Version 1.2 \| Brazil Patch 0

The L1 IT Service Desk AI Specialist has been updated.

### What's new

-   ** Response Templates**

    AI Admins can switch response templates between a fixed template and dynamic mode, where the AI Specialist writes activity notes, customer comments, work notes, and close notes from free-form instructions the administrator provides.

-   **Catalog request submission and tracking**

    The L1 IT Service Desk AI Specialist can resolve incidents by submitting service catalog requests on behalf of users. The L1 IT Service Desk AI Specialist collects the required details through guided questions, submits or drafts the request, and resolves the linked incident so users can track fulfillment through the request.

-   **Catalog performance analytics**

    A new Catalog tab on the AI Specialist performance dashboard shows drafted, submitted, abandoned, and canceled request volumes by catalog item. This gives administrators visibility into how well the AI Specialist is handling catalog-based resolutions.

-   ****

    Evaluate L1 IT Service Desk AI Specialist's work, captured in a coaching assessment against the rubric defined on the coaching opportunity by using the AI Quality Assessment skill to get consistent, objective scoring.


## Version 1.1

The L1 IT Service Desk AI Specialist is a new application in ServiceNow Otto for IT Service Management \(ITSM\) in the Brazil release.

### What's new

-   **Routing criteria configuration**

    Enable hand-offs between the AI specialist and human agents if work is better handled by a different group or requires additional human oversight.

-   **Routing decision criteria over time analytics**

    Shows how many incidents over time were reassigned because routing decision criteria matched.

-   **Performance quality assessment analytics**

    Review how the AI Specialist measures up in each quality area using automatically generated quality assessments. You can monitor scores, compare different coaching opportunities, and pinpoint areas where quality can be enhanced.


