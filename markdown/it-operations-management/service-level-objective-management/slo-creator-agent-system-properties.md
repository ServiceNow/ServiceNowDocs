---
title: SLO creator agent system properties
description: Configure how the SLO creator agent generates and activates SLOs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-level-objective-management/slo-creator-agent-system-properties.html
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: reference
last_updated: "2026-08-19"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [SLO Management reference, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# SLO creator agent system properties

Configure how the SLO creator agent generates and activates SLOs.

To turn automatic SLO generation on or off and manage email notifications for generated SLOs, see [Manage SLO creator agent settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-level-objective-management/now-assist-itom-manage-generated-slos.md).

**Note:** Property changes apply only to newly generated SLOs. Existing SLOs aren't recalculated.

## `sn_ai_agents_slo.commitment_buffer`

-   **Description**

    Adds a buffer to an availability commitment when the agent calculates the SLO target. Applies only when the agent finds an availability commitment.

-   **Values**

    Default: `0.09`

-   **When to adjust**

    Increase the buffer to set stricter SLO targets and provide earlier warning before the service falls below its availability commitment. Decrease it if the generated targets are too strict.


## `sn_ai_agents_slo.create_slo_mode`

-   **Description**

    Controls if the agent activates generated SLOs automatically or saves them as drafts.

-   **Values**

    Default: `auto_activate`

    Other value: `draft`

-   **When to adjust**

    Use `draft` to review and edit generated SLOs before activation. Use `auto_activate` when generated SLOs can take effect without review. Error budget notifications begin after activation.


## `sn_ai_agents_slo.linked_alerts_cap`

-   **Description**

    Limits the number of critical alerts associated with an incident that the agent considers when generating SLOs.

-   **Values**

    Default: `5`

    Maximum: `10`

-   **When to adjust**

    Increase the value when incidents commonly produce more relevant critical alerts than the default includes. Decrease it when numerous alerts represent the same underlying issue.


## `sn_ai_agents_slo.linked_outages_cap`

-   **Description**

    Limits the number of outages associated with an incident that the agent considers when generating SLOs.

-   **Values**

    Default: `5`

    Maximum: `10`

-   **When to adjust**

    Increase the value when a single incident commonly spans more outage records than the default includes. Decrease it when multiple outage records represent the same underlying issue.


## `sn_ai_agents_slo.orphan_alert_window_days`

-   **Description**

    Specifies how far back the agent looks for critical alerts that aren't associated with an incident when generating SLOs.

-   **Values**

    Default: `30`

    Range: `7-90`

-   **When to adjust**

    Use a shorter window when older alerts no longer reflect current service reliability. Use a longer window to account for less frequent or recurring alert patterns.


## `sn_ai_agents_slo.other_incident_window_days`

-   **Description**

    Specifies how far back the agent looks for other P1 and P2 incidents associated with the service or CI when generating SLOs.

-   **Values**

    Default: `90`

    Range: `30-180`

-   **When to adjust**

    Use a shorter window to focus on recent conditions. Use a longer window to account for severe incidents that occur less frequently.


**Parent Topic:**[SLO Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-level-objective-management/service-level-objective-management-reference.md)

