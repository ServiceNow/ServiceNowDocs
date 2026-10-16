---
title: Enable smart assessments
description: Enable the sn\_align\_ws.enable\_smart\_assessments property so demands use smart assessments instead of the classic assessment workflow, when they are moved to screening.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/strategic-planning/enable-smart-assessments-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-09-26"
reading_time_minutes: 1
keywords: [enable smart assessments, smart assessments property, configure smart assessments]
breadcrumb: [Configure, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Enable smart assessments

Enable the **sn\_align\_ws.enable\_smart\_assessments** property so demands use smart assessments instead of the classic assessment workflow, when they are moved to screening.

## Before you begin

Role required: admin

## About this task

Requires the Smart Assessment \(**sn\_smart\_asmt**\), Smart Assessment - Connected \(**sn\_smart\_asmt\_conn**\), Smart Assessment Designer \(**sn\_smart\_asmt\_desg**\), and Smart Scoring \(**sn\_smart\_scoring**\) plugins to be active. Portfolio Planning automatically installs these as dependencies.

**Tip:** Check **System Applications** &gt; **All Available Applications** if smart assessments aren't triggered after enabling the property and verify that all required plugins are active.

## Procedure

1.  Navigate to **All** and enter `sys_properties.list` in the filter box.

2.  Filter the Name column to locate and open the **sn\_align\_ws.enable\_smart\_assessments** property.

3.  Enter `true` in the Value field.

4.  Select **Update**.


## Result

Demands route through smart assessments. No separate role assignment is needed for demand managers to read assessments. The **sn\_smart\_asmt.assessment\_reader** and **sn\_smart\_asmt.template\_reader** roles are inherited in the demand\_manager role. Stakeholders still need the **sn\_smart\_asmt.actor** role to fill the assessments. For more information about user roles, see [Smart assessment users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/smart-assessments-overview.md).

**Related topics**  


[Use a custom smart assessment template for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/override-smart-assessment-template-dw.md)

[Assess demands with smart assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/smart-assessments-overview.md)

[Configuring Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine-cf-config.md)

