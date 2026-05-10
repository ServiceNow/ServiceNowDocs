---
title: Workflow of project risk assessment
description: To understand the integration of Project Portfolio Management and Governance, Risk, and Compliance risk management capabilities, it is important to understand the workflow of project risk assessment.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Project Risk Assessment using Advanced Risk Assessment, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Workflow of project risk assessment

To understand the integration of Project Portfolio Management and Governance, Risk, and Compliance risk management capabilities, it is important to understand the workflow of project risk assessment.

Project risk assessment follows a sequence of steps. Sometimes, a risk is elevated to an enterprise risk after the risk is assessed. An enterprise risk is a risk that can cause monetary or reputational losses. It can jeopardize your ability to stay in business.

The workflow of project risk assessment is as follows:

1.  A project manager identifies risks and adds those risks to a project. The manager can either create risks or add them from a library. The project manager has the it\_project\_manager and sn\_grc.business\_user roles. For more information, see [Add risks for a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/add-risks-for-project.md).
2.  The project manager then initiates risk assessment for the newly added risks. In the Project Integration Configuration form, the assessors and approvers are defined for the assessment. They get an email notification to assess the risks.

    **Note:** You can only assess the risks that are in the Pending, Open, or Work in Progress state.

3.  If the Project Integration Configuration form has stakeholders selected as assessors, then the project manager must manually assign the risks to the relevant stakeholder.
4.  As a risk specialist, the risk assessor is notified about the new risks for assessment.

    The risk assessor can use the link in the email notification to start the assessment. Alternatively, the risk assessor can navigate to **Advanced Risk Assessment** &gt; **Risk Assessment Tasks** &gt; **My Tasks** to perform advanced risk assessment. See [Advanced Risk Assessment](advanced-risk-assessment.md).

5.  In the project risk form, the project manager reviews the Risk Assessment Summary section to view the risk assessment scores.
6.  If the project manager determines that the project risk has an impact on the enterprise, then the project manager can elevate the risk to an enterprise risk.

    **Note:** When a project risk is elevated to an enterprise risk, the project risk is copied from the project risk register to the enterprise risk register.

7.  If a risk is elevated to an enterprise risk, the enterprise risk manager is requested to assess the risk.
8.  The project manager views the enterprise inherent risk score and the enterprise residual risk score in the **Risk Assessment Summary**.
9.  As part of the Project Portfolio Management workflow, if a risk materializes and an action must be taken for this risk, then the project manager can convert the risk into an issue. For more information, see [RIDAC \(Risk, Issue, Decision, Action, and Request Changes\) record entries for a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/ridac-entries-for-project.md).
10. The project manager can also view the project risk posture through the heatmap in the Risk Overview section on the project form. The heatmap displays high impact risks and high likelihood risks. With the heatmap, you can prioritize the risks that need immediate attention. The risks that are assessed contribute to the aggregated risk score. The aggregated risk score is a single score that can be reported to all the stakeholders. For more information, see [Create a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_CreateAProject.md).
11. View the Project Risk Overview dashboard to understand the overall risk posture of project risks and of enterprise risks. For more information, see [Project Risk Overview dashboard](../../../use/dashboards/application-content-packs/project-risk-dashboard.md).

**Note:** The assessor and the approver must have risk business user role \(sn\_grc.business\_user\) to perform the required tasks. If the project risks are reassessed for any reason and the scores change, then the enterprise risk assessor gets an email notification with the option to reassess the enterprise risk.

The key users and the user journey are shown in the following figures.

![Key personas who use the PPM and Risk integration feature](../image/personas_ppm_risk.png "Key users of Project Portfolio Management and Risk Integration")

![PPM and Advanced Risk Assessment integration user journey](../image/project-risk-assessment-user-journey.png "User journey of Project Portfolio Management and risk integration")

**Parent Topic:**[Project Risk Assessment using Advanced Risk Assessment](risk-and-ppm-better-together.md)

