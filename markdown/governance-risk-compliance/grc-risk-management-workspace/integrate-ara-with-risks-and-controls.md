---
title: Integration of advanced risk assessments with risks and controls
description: When customers migrate to advanced risk assessments, the system replaces the legacy risk life cycle and shows a new section called Assessment Summary on the Risk form. This section is useful for the risk managers as it provides the overall visibility of the assessment results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-risk-management-workspace/integrate-ara-with-risks-and-controls.html
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Integration of advanced risk assessments with risks and controls

When customers migrate to advanced risk assessments, the system replaces the legacy risk life cycle and shows a new section called Assessment Summary on the Risk form. This section is useful for the risk managers as it provides the overall visibility of the assessment results.

Migrating to advanced risk assessments is useful for the risk managers as they can view the risks that need immediate attention. To migrate to advanced risk assessment, a new property called **Migrate to Advanced Risk Assessments** is introduced in the Quebec release. Users can enable this property under **Advanced Risk Assessment** &gt; **Administration** &gt; **Properties**.\[Omitted image "migrate-to-ara.png"\] Alt text: Property to migrate to advanced risk assessment

When users enable this property, they completely migrate to the advanced risk assessment and do not use the old risk management. This migration affects the following forms:

-   Risk
-   Entity
-   Risk Statement

When users migrate, the system then removes the legacy risk life cycle, scoring, assessment, and response sections on the risk form. Instead, a new section called Assessment Summary is available where the risk assessment scores are displayed along with the risk response. If there are multiple methodologies used for risk assessment, the system detects the default methodology for the selected entity class and displays those scores in this field. The primary risk assessment methodology can be defined in the risk assessment methodology form.

\[Omitted image "new-risk-form-with-new-property.png"\] Alt text: Changed view of the risk form

\[Omitted image "updates-to-risk-form.png"\] Alt text: Old links are hidden and newer links are available.

Similarly, for controls, the control effectiveness values are updated if individual assessment of controls is performed.

On the Entity form, the aggregated risk scores are displayed from the primary risk assessment methodology. The old tabs displaying the legacy risk scores are hidden from the user's view.

On the risk statement form, fields like assessment, framework, and scoring are hidden. The corresponding old links for pushing risk scores and so on are also hidden from the user's view.

**Parent Topic:**[Advanced Risk Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-risk-management-workspace/advanced-risk-assessment.md)

