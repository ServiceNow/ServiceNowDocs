---
title: Integration of advanced risk assessment with other applications
description: As an administrator, you can embed risk assessments within other workflows and define rules for when risk assessments must be initiated. The key benefit of embedding risk assessments is the digitization of the workflow so that assessments are initiated automatically without manual effort.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Integration of advanced risk assessment with other applications

As an administrator, you can embed risk assessments within other workflows and define rules for when risk assessments must be initiated. The key benefit of embedding risk assessments is the digitization of the workflow so that assessments are initiated automatically without manual effort.

Prior to the San Diego release, you could perform risk assessments in a cyclic manner. This means that earlier risk assessments were performed only few times in a year and thus your risk posture reporting might not be accurate. To address this issue, you can now perform event-driven risk assessments. Event-driven risk assessments mean that when an event occurs, you can perform a risk assessment. Performing event-driven risk assessments help you to get a quick view of the actual risk posture and take the necessary corrective actions. You can integrate advanced risk assessment with any application and perform risk-based assessments in your workspaces. By default, ServiceNow® provides the integration of advanced risk assessment with risk events in the Risk Workspace.

To integrate risk assessment in an application in your workspace, you must perform the configuration steps given in the [Risk assessment integration in workspace \[KB0999135\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3Db413590cdbb73c1039445ac2ca9619bc%26sysparm_stack%3Dkb_knowledge_list.do%3Fsysparm_query%3Dactive%3Dtrue%26sysparm_view%3DKB0999135) article in the Now Support Knowledge Base. After you perform the configuration steps, you can see the **Initiate risk assessment** button.

Although you can integrate the Initiate risk assessment feature on any application in your workspace, this article uses risk events as an example. When you analyze a risk event and identify the relevant risks, you can easily initiate risk assessments for those risks by integrating the advanced risk assessment workflow in your risk events. This integration enables you to perform risk assessments without going through the entire process of creating risk assessment scopes. Prior to the San Diego release, for a risk assessor to perform a risk assessment, the risk user was required to create a risk assessment scope defining the entity, the assessor, and the approver.

When you initiate an assessment for a risk that is created for a risk event, although the risk assessment methodology \(RAM\) is set to the primary RAM of the entity class, you can select a different relevant risk assessment methodology. Only those risk assessment methodologies that are associated with the entity class of the selected risk are available for selection. You can then specify the assessor and approver for the risk assessment. Only users with the sn\_risk\_advanced.ara\_assessor role can be the assessors and users with the sn\_risk\_advanced.ara\_approver role can be the approvers. For more information on these roles, see [Roles for performing advanced risk assessment](../../grc-risk/reference/roles-for-ara.md). Earlier, the approvers were defined when the risk administrators created the risk assessment scopes. However, when you initiate a risk assessment from an application, you can specify the approvers at the time creating the assessment. You cannot change the approvers once you have specified them. If the approver is set as **Same as assessor's manager**, then the approver is automatically set depending on the assessor. You can also define the number of days after which the assessment will be considered overdue.

Even when you initiate a risk assessment from an application using the API, you can add those risks to the risk assessment scope at any time. After the risk is added to the risk assessment scope, the frequency of the assessment is based on the frequency defined in the risk assessment scope.

There could be some scenarios when you maybe unable to initiate a risk assessment from an application. Those scenarios are listed as follows.

-   If you select multiple risks and try to initiate the assessments at once. The reason for this is that different risks can have different entities and can have different risk assessment methodologies.
-   If an in-progress risk assessment exists.
-   If a risk assessment methodology is not defined for the entity for which the risk exists.

