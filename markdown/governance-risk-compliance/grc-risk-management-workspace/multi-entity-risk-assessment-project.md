---
title: Multi-entity risk assessment project
description: A risk assessment project can scope risks across multiple entity classes and multiple entities at the same time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-risk-management-workspace/multi-entity-risk-assessment-project.html
release: brazil
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Risk assessment project, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Multi-entity risk assessment project

A risk assessment project can scope risks across multiple entity classes and multiple entities at the same time.

## Multi-entity scoping

With multi-entity scoping, you can select one or more entity classes and one or more entities within a single risk assessment project. Risks that are mapped to the selected entities are scoped in automatically. You can also add ad hoc risks or risks from the risk library to any of the selected entities.

## Benefits

Scoping multiple entities in a single risk assessment project provides the following benefits:

-   Reduces the setup effort of creating and configuring a separate project for each entity.
-   Consolidates the assessment experience for an assessor who is responsible for the same risks across several entities.
-   Enables a consolidated view for approvers across all the scoped entities.
-   Reduces the need to manually aggregate results across projects for reporting.

## Considerations

The following considerations apply to a multi-entity risk assessment project:

-   A risk assessment project can use only one risk assessment methodology \(RAM\), regardless of how many entities are scoped in.
-   When more than one entity is selected, you can select only a single assessor \(a user or a group\) for the project. The **Entity owner** and **Entity stakeholder** assessor type options are available only when the project has a single entity.
-   Each entity that's scoped into the project must have at least one risk. You can't remove the last risk that's scoped to an entity.
-   The **Submit** action stays disabled until all the risks across all the scoped entities pass validation.

**Parent Topic:**[Risk assessment project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/risk-assessment-project.md)

**Related topics**  


[Risk assessment project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/risk-assessment-project.md)

[Create a risk assessment project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/create-risk-assessment-project.md)

[Assess Risk Projects in Stacked View](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/perform-assessment-on-risk-assessment-project.md)

[Assess Risk Projects in Grid view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/perform-assessment-risk-assessment-project-grid-view.md)

