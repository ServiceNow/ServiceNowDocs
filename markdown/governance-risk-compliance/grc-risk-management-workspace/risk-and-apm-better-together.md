---
title: Application risk assessment using Advanced Risk Assessment
description: Manage digital risks of business applications easily by integrating GRC with business applications. By integrating, you get real-time insights into the digital risk posture of business applications, have improved communication between application owners and IT risk managers, and can reduce workloads.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Application risk assessment using Advanced Risk Assessment

Manage digital risks of business applications easily by integrating GRC with business applications. By integrating, you get real-time insights into the digital risk posture of business applications, have improved communication between application owners and IT risk managers, and can reduce workloads.

Enterprises use Application Portfolio Management \(APM\) to manage their inventory of business applications. Examples of business applications are Zoom, Workday, Jobvite, and so on. Each business application has two owners:

-   IT Application owner: Owns the application from the IT team and is the primary point of contact. The IT application owner is also known as the application product owner or application owner.
-   Business owner: Owns the application for its business uses. The business owner is the executive sponsor of the business application. The owner is generally from the business who sponsors the application. For example, finance applications are usually sponsored by the head of finance.

When you integrate GRC with APM, you can simplify the work of IT risk managers by identifying the risks and the necessary controls. You can mitigate the digital risks of business applications. You can also ensure that the controls are effective. The benefits of this integration are the following:

-   Reduces the time spent by risk managers and by the application owners of digital risks.
-   Provides faster and more efficient communication between the application owners and risk managers.
-   Provides an overview of the digital risk posture of business applications.
-   Enables continuous monitoring of the applications.

The users who benefit from this integration are shown in the following figure:

![Users that benefit by integrating APM and risk](../image/GRC_All_Key_Personas-01.png "Beneficiaries of APM and Risk integration")

The Application Risk Assessment feature is available when you activate the Advanced Risk plugin. But the default configurations for the APM risk identification record are available only when you have the APM integration with Risk Management plugin \(com.snc.apm\_risk\_assessment\) enabled.

The following image shows the high-level workflow of the integration:

![Figure depicting a high-level integration of the solution](../image/grc-apm-high-level-solution.png "High-level integration of APM and Advanced Risk Assessment")

-   **[Workflow of risk identification for business applications](workflow-risk-identification.md)**  
When assessing an application for risks, the application goes through various stages of risk identification and assessment. You can define the identification and assessment workflow based on your requirements.
-   **[Set up risk identification integration](../task/configure-risk-identification-form.md)**  
Before assessing an application, specify the target application where the risk identification must be initiated.
-   **[Respond to an application questionnaire](../task/respond-to-app-questionnaire.md)**  
Respond to a questionnaire about an application for risk assessment.
-   **[Create a smart assessment template for risk identification](../task/create-smart-assessment-template-for-risk-identification.md)**  
Create a smart assessment template for risk identification using the Smart Assessment Engine application.
-   **[Review responses and perform inherent risk assessment](../task/review-responses-to-apm-risk-assmt.md)**  
Compute the overall risk score for an application by performing an advanced risk assessment. After the IT application owner responds to the questionnaire, a risk manager reviews the responses and performs the inherent assessment.
-   **[Associate risks, citations, policies, and controls with a risk identification record](../task/associate-risks-pols-citations-risk-idenfn.md)**  
After the inherent assessment is completed, you can associate risks, citations, policies, and controls with the risk identification record. You can identify what methods to use to mitigate the risks.

**Parent Topic:**[Governance, Risk, and Compliance](../../grc-common/reference/r_WhatIsGRC.md)

**Related topics**  


[Workflow of risk identification for business applications](workflow-risk-identification.md)

