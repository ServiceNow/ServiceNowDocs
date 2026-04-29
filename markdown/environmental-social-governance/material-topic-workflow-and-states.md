---
title: Material topic workflow and states
description: Material topics are the point of origin for sustainability initiatives. A material topic must be identified before it can be tracked and measured for success. The workflow states for a material topic depend on how the material topic was created.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Material topic workflow and states

Material topics are the point of origin for sustainability initiatives. A material topic must be identified before it can be tracked and measured for success. The workflow states for a material topic depend on how the material topic was created.

## Default workflow

The states of a material topic are:

1.  **Draft**: All material topics begin in this state. The following fields can be updated in this state:
    -   Name
    -   Classification
    -   Importance to business success
    -   Importance to stakeholders
    -   Priority
    -   Approver
2.  **Approval**:The Operational Sustainability program manager reviews the material topic and ensures that all fields are accurate and complete. After the review completes, the material topic moves to Monitor. For example, if the material topic is Carbon emissions, the reviewer might verify:
    -   The material topic is accurately defined.
    -   The description of the material topic is accurate.
3.  **Monitor**: The material topic remains in this state until a modification is needed. If an update is necessary, you can return the material topic to the Draft state. This may occur after a subsequent materiality assessment, where there could be a shift in the following attributes:

    -   Priority
    -   Significance to business success
    -   Significance to stakeholders
    Moving a material topic back to the Draft state does not affect downstream goals and targets.

    Only material topics that are in the Monitor state are shown in the Materiality matrix on the Operational Sustainability Workspace home page.

4.  **Retired**: The material topic is no longer tracked by the organization as a relevant sustainability issue.

## Socialsuite workflow

Material topics imported from Socialsuite do not require approval in your ServiceNow instance. These topics use different workflow states than the default workflow. The following table shows how Socialsuite states map to states in your ServiceNow instance:

|Socialsuite state|ServiceNow instance state|
|-----------------|-------------------------|
|Not started|Draft|
|Open for input|Materiality Assessment|
|Input closed|Materiality Assessment|
|Complete|Monitor|
|Historical|Monitor|

Material topics imported from Socialsuite progress through the following states in your ServiceNow instance:

1.  Draft: Material topics in the Not started state in Socialsuite appear in Draft. The material topic details are read-only and cannot be updated.
2.  Materiality Assessment: The ESG program manager validates and reviews the materiality assessment data in this state.
3.  Monitor: Only material topics in Monitor appear in the materiality matrix on the Operational Sustainability Workspace home page. Material topics imported from Socialsuite cannot be moved back to Draft.

## Fields for Socialsuite material topics

Material topics imported from Socialsuite include additional fields that store materiality assessment data. These fields are visible and read-only for topics imported from Socialsuite. All data for these fields is managed through Socialsuite. For a complete list of fields, see [Socialsuite material topic fields](../reference/socialsuite-material-topic-fields.md).

**Parent Topic:**[Exploring Operational Sustainability Management \(formerly ESG Management\)](esg-new-explore.md)

**Related topics**  


[Integrating Operational Sustainability Management \(formerly ESG\) with other applications](integrate-esg.md)

[Set Material topic selection system property](../task/set-material-topic-selection-system-property.md)

