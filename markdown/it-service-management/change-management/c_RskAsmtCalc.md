---
title: Risk assessment
description: Change Management provides two methods to calculate the risk of a change. The Change Management - Risk Calculator plugin is active by default in the base system, and Change Management - Risk Assessment is optional.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/c\_RskAsmtCalc.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Analyze change request risk and impact, Reference, Change Management, IT Service Management]
---

# Risk assessment

Change Management provides two methods to calculate the risk of a change. The Change Management - Risk Calculator plugin is active by default in the base system, and Change Management - Risk Assessment is optional.

-   Change Risk Calculator uses predefined properties and conditions to calculate a risk value.
-   Change Management - Risk Assessment uses information provided by the end user to assess a risk value.

You can use the two methods individually or together, depending on your requirements. If you use the methods together, the system selects the higher of the two risk values.

\[Omitted image "image.risk\_assessment\_calculation"\] Alt text: Risk assessment calculation

**Note:** To use only one method when both Risk Assessment and Risk Calculator are active, remove the conditions for the other method.

If you activate Change Management - Risk Assessment, the administrator can add the **Task Assessment** &gt; **Task** related list to the change request form, if necessary. The related list displays risk assessments associated with the change request. For more information, see [Perform risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_AssessRisk.md)

-   **[Define risk assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_DefineARiskAssessment.md)**  
Define the risk assessment questions, thresholds, and conditions that calculate the risk of a change request from information that the end user provides.
-   **[Perform risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_AssessRisk.md)**  
Perform a risk assessment on an existing change request after the risk assessment criteria are defined, and view the responses on the change request.

**Parent Topic:**[Analyze change request risk and impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-risk-conflict-analysis.md)

**Related topics**  


[Perform risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_AssessRisk.md)

