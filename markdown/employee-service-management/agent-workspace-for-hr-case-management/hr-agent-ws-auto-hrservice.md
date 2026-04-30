---
title: Auto determination of HR service in Agent Workspace for HR Case Management
description: Auto determine the correct HR service for a case in Agent Workspace for HR Case Management. Enable an HR agent to transfer the case to the appropriate HR service rather than having to spend significant time manually triaging cases to appropriate HR services.
locale: en-US
release: xanadu
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Machine learning solutions in Agent Workspace for HR Case Management, Using Agent Workspace for HR Case Management, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Auto determination of HR service in Agent Workspace for HR Case Management

Auto determine the correct HR service for a case in Agent Workspace for HR Case Management. Enable an HR agent to transfer the case to the appropriate HR service rather than having to spend significant time manually triaging cases to appropriate HR services.

**Important:** This feature is available with the HR Professional and HR Enterprise packages when you activate the Agent Workspace for HR Case Management and Predictive Intelligence applications. If you do not want to use this feature, disable the **sn\_hr\_core.case\_auto\_categorization** system property.

After you create the case, the HR Case Classification solution definition auto determines the HR service based on the short description of the case. The appropriate HR service for the case is displayed in a banner.

**Important:** The banner is not displayed if:

-   you have logged the case under the correct HR service
-   you have manually transferred or auto-transferred the case
-   case is not in the ready or draft state

## Auto training the predictive model

The HR Case Classification solution definition is configured and the predictive model is auto trained only when all the following conditions are met.

-   The Human Resources Scoped App: Workspace \(com.sn\_hr\_agent\_workspace\) plugin is installed.
-   The Predictive Intelligence \(com.glide.platform\_ml\) plugin is installed.
-   There are 10000 records of HR case study matching the filters defined in the solution definition.
-   The **glide.platform\_ml.auto\_training.enabled** system property is set to true.

**Note:** Auto training does not happen if any one of the preceding conditions is not met. In such a case, [Manually train the HR predictive model](../task/hr-predictive-intelligence-train.md). Navigate to the **HR AI configuration** module, open the HR Case Classification record, and map the manually configured solution definition.

**Parent Topic:**[Machine learning solutions in Agent Workspace for HR Case Management](hr-agent-ws-ml-solutions.md)

**Related topics**  


[Auto determination of assignment group in Agent Workspace for HR Case Management](hr-agent-ws-auto-assign-grp.md)

[Display similar closed cases in Agent Workspace for HR Case Management](hr-agent-ws-similar-closed-case.md)

