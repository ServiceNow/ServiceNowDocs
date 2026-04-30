---
title: Any object assessment using Advanced Risk Assessment
description: If you don't have the complete GRC setup for entities, risk statements, controls, and so on, even then, you can still assess the risks on any ServiceNow record or object. An example of object assessment is assessing change management or assessing a citation.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Any object assessment using Advanced Risk Assessment

If you don't have the complete GRC setup for entities, risk statements, controls, and so on, even then, you can still assess the risks on any ServiceNow record or object. An example of object assessment is assessing change management or assessing a citation.

Any object assessment is used to perform risk assessment on any ServiceNow record. To perform a risk assessment, a prior knowledge of risk is not necessary. Using the assessment results, risk managers can quickly analyze the risks associated with their project or application.

Any object assessment can be performed in the following ways:

-   Ad hoc: In an ad hoc based risk assessment, users can perform the assessment through a UI action.
-   Event driven: In an event driven risk assessment, a user can perform the risk assessment based on some event.

To perform any object assessment, you must create a risk assessment methodology with **Object** as the context and then select the relevant table.

**Note:** You cannot assess your controls if you perform the risk assessment for an object. The reason for this limitation is that controls are associated to either an entity or a risk. Also, the risk response workflow is not available for the assessment of an object.

After you generate an assessment, you can add a related list in the object in which you can see the list of assessments. For more information on how to configure any object assessment for an object and create the **Assess risk** button, see the [Perform any object assessment \[KB0826429\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0826429) article in the Now Support Knowledge Base.

For information on how to configure any object assessment in the Risk Workspace, refer to the [Any object integration in workspace \[KB0961251\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0961251) article in the Now Support Knowledge Base.

**Note:** You must log in to Now Support to view the articles.

**Parent Topic:**[Advanced Risk Assessment](advanced-risk-assessment.md)

