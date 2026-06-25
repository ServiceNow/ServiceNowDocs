---
title: Exploring Third-party Risk Management
description: The Third-party Risk Management application centralizes and standardizes the processes, source materials, responsible persons, and methods of your third-party risk management program. You can improve your operations by managing your portfolio of third parties and by identifying, tracking, and mitigating the issues that arise with third parties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-exploring.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 19
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Exploring Third-party Risk Management

The Third-party Risk Management application centralizes and standardizes the processes, source materials, responsible persons, and methods of your third-party risk management program. You can improve your operations by managing your portfolio of third parties and by identifying, tracking, and mitigating the issues that arise with third parties.

## Third-party Risk Management overview

To protect your organization's assets, reputation, and operations, your third-party risk management program must identify, assess, and mitigate the risks that are associated with external parties. The TPRM application helps you to prevent your outsourced providers, partners, and suppliers from creating a business disruption or a negative impact on your business performance. By using the TPRM application, you can reduce the manual burden and costs of your risk assessment process through automation.

TPRM brings all third-party risk information into one environment.

The following key capabilities can help you to assess risk more effectively:

-   Onboarding, Offboarding, Renewals, and additional due diligence workflows
-   Assessment management
-   Continuous risk monitoring
-   Risk performance management

## Third-party Risk Management Users

<table id="table_azr_yvk_rcc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Due diligence requesters

</td><td>

Requesters can be any employee at your organization interested in onboarding, reassessing, or offboarding an engagement. For more information on the different types of due diligence requests, see [Requesting third-party risk due diligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-requesting-tpr-due-diligence.md).

</td></tr><tr><td>

TPRM Assessors

</td><td>

TPRM Assessors are members of the Risk manager's team that help with mitigating the risk of a potential engagement by reviewing information collected through the due diligence process. They could be potentially assigned as owners of due diligence requests based on their expertise or knowledge of the engagement.Here are some examples of different types of assessors and how they would impact the due diligence process for TPRM:

-   **Compliance Risk Assessor**: Confirms that engagements comply with industry standards, legal requirements, and contractual obligations. They regularly review engagement processes and activities to help ensure compliance.

-   **Cybersecurity Risk Assessor**: Evaluates the cybersecurity practices and infrastructures of engagements to protect against data breaches and cyber threats. They regularly review the engagement's security measures and suggest necessary enhancements.

-   **Operational Risk Assessor**: Analyzes the existing operational practices of engagements, focusing on aspects such as business continuity, supply chain logistics, and quality of service. They regularly review the engagement's operational practices to help ensure they are in alignment with the organization's standards and that appropriate contingencies are in place for potential disruptions.


</td></tr><tr><td>

TPRM Approvers

</td><td>

TPRM approvers are typically a senior member within the organization. They’re responsible for the final review and approval of the due diligence findings. They help confirm that all risk management requirements have been satisfactorily addressed before proceeding with any third-party engagement, whether it involves onboarding, continuing, or offboarding an engagement.

 Here are some examples of different types of approvers:

 -   **Senior Risk Manager**: Oversees risk management strategies and alignment with organizational goals.
-   **Chief Compliance Officer**: Responsible for the company adhering to legal standards and internal policies.
-   **Legal Executive**: A senior member of the legal team who ensures that all contractual and regulatory requirements are met.

</td></tr><tr><td>

Contract negotiator

</td><td>

Contract negotiators orchestrate and finalize agreements between your organization and potential engagements. They use all the information collected through the due diligence process to help ensure that all contracts reflect your strategic interests and adhere to your risk management protocols.

</td></tr><tr><td>

Risk Manager

</td><td>

Risk managers lead thorough risk assessments of third parties and engagements. Based on the information collected and reviewed by the Risk manager and their team, they prioritize risks, develop mitigation strategies, and use TPRM to monitor and manage ongoing third-party relationships effectively.

</td></tr><tr><td>

TPRM Admin

</td><td>

Administrators manage user roles, permissions, and system settings to set up TPRM to meet your organization's specific risk management needs and compliance requirements.

</td></tr></tbody>
</table>For more information on TPRM roles, see [Roles in Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-roles.md).

## Third-party Risk Management workflow

The following infographic shows the workflow of the most important processes that you can use to manage risk.

\[Omitted image "mmasset0020705-due-diligence-workflow-horizontal.png"\] Alt text: Infographic that shows where the processes in the due diligence workflow are performed. For the text description, refer to the workflow steps that follow.

-   **Request due diligence for an engagement**

    An employee at your organization requests due diligence for a third-party engagement. The due diligence request is reviewed and approved by the Third-party risk \(TPR\) manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\].

    For more information, see [Requesting third-party risk due diligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-requesting-tpr-due-diligence.md).

-   **Assess risk using an internal assessment containing an Inherent Risk Questionnaire \(IRQ\)**

    An IRQ is a set of questions that scores and scopes the required due diligence on the third parties or engagements. After the due diligence request is approved by the TPR manager or TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] that has been assigned as the owner of the due diligence request, they select an IRQ and attach it to an internal assessment.

    **Note:** After the IRQ process enters the IRQ in progress state, you can request risk intelligence reports associated with your due diligence request. For more information, see [Using risk intelligence reports and scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-riskintel-using.md) and [Request a risk intelligence report associated with a due diligence request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-riskintel-request-dd.md).

    For more information, see [Assessing your third-party risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-assessing-tpr.md).

-   **Create third-party elements**

    After your due diligence request has completed the IRQ process, if TP elements are needed, the TPR manager or due diligence request owner selects **Start collection** and a collection task is created. A third-party element questionnaire is sent to the third-party engagement contact. The TPR manager or owner manually creates third-party element records based on the responses.

    For more information, see [Assessing your third-party risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-assessing-tpr.md) and [Monitoring third-party elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-monitor-tp-elements.md).

-   **Assess risk using an external assessment**

    After the IRQ process or TP element collection process is completed, the TPR manager or owner selects questionnaires and requests for documentation to attach to external assessments for sending to the third party or engagement. For more information on creating assessments, see [Create an external assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-assessment.md) and [Third-party risk assessment form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-assessment-form.md).

    For more information on this process, see [Assessing your third-party risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-assessing-tpr.md) and [Monitoring third-party elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-monitor-tp-elements.md).

    **Note:** If you have any integrated risk intelligence, relevant information is pulled at this time.

-   **Integrate scores using risk intelligence providers**

    Your organization can purchase services from providers that return data that is analogous to personal credit scores. The scores provide insight on how trustworthy and safe a particular third party can be.

    For more information, see [Integrating scores from risk intelligence providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-riskintelprvdr-overview.md).

-   **Request risk intelligence reports and scores**

    If you are the TPR assessor and are the due diligence request owner or have the TPR manager role, you can use the TPRM application to request scores or reports for third parties by using the risk intelligence request form. After the reports and scores are generated by the risk intelligence provider, the links to these reports are delivered and associated with that risk intelligence report record. If you have any integrated risk intelligence, relevant information is pulled at this time. For more information, see [Using risk intelligence reports and scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-riskintel-using.md).

-   **View scores and related information**

    The information gathered is scored and combined into a single view of the due diligence process to display all scores, completed questionnaires, issues, approvals, and comments.

    For more information on scoring, see [Scoring calculations using the classic assessment engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/vendor-ratings-scoring.md) and [Verifying scoring calculations using the classic assessment engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-verif-q.md). See [Classic assessment configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ongoing-config.md) for information on how scoring can be configured at the assessment and questionnaire level.

-   **Approve due diligence requests**

    All approvers can review due diligence and see the detailed information before making an approval. After all approvers approve the due diligence request, all the due diligence information can be made available for the person that is negotiating the contract. The contract risk process only applies if a contract is required.

    For more information, see [Approving or rejecting requests for due diligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-approving.md).

-   **Negotiate a contract**

    The contract negotiator can see the detailed information of all the scores and questionnaires. If additional due diligence is required, they can request it. If the contract negotiator successfully executes a contract with the third party, they can upload it and specify that the contract is executed. This action automatically notifies all key stakeholders of the contract's status. The contract negotiator can also skip the contract risk process, reject the due diligence request, or specify that the contract isn’t executed and that the third party isn't engaged for business.

    **Note:** If the third-party risk manager or owner selects the **Skip contract risk process** option during the due diligence process, the assigned contract negotiator isn’t notified and the Contract risk process state is skipped. An approver and owner can update the **Skip contract risk process** selection up until the approval process is completed. For more information about this process, see [Due diligence request process management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-dd-mgt-pg-details-tab.md).

    For more information on this process, see [Managing the contract risk process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-contract-risk-process.md).

-   **Monitor third-party risk**

    TPR managers, TPR assessors, and Third-party assessment reviewers \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] can monitor and review the performance of third parties with Vendor Management Workspace.

    For more information, see [Monitoring your third-party risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-monitoring-tpr.md).

-   **Manage the Third-party portal**

    TPR managers can manage third-party contacts, including creating logins, assigning roles, and tracking progress on questionnaires and tasks through the Third-party portal. Third-party contacts can use the portal to respond to assessments, delegate tasks, and manage their information, with options to use Microsoft Excel templates or the SIG questionnaire for responses.

    For more information, see [Managing the contract risk process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-contract-risk-process.md).


For an in-depth description of the TPRM Due diligence workflow, see [Due diligence workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-workflow-in-workspace.md).

**Note:** Starting with version 19.1.x of the Third-party Risk Management application, the tiering questionnaire and external assessment reminders workflows are deprecated and migrated to Workflow Studio. If you have customized these workflows, they won’t be deprecated or migrated as part of this change.

## Third-party Risk Management benefits

The following table shows the benefits of the Third-party Risk Management application.

|Benefit|Feature|Users|
|-------|-------|-----|
|View important risk information and quickly access actions.|[TPRM Home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-home-page.md)|All TPRM users|
|Use due diligence management reports to track, prioritize, and manage responsibilities.|[TPRM Due diligence management reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-dd-management-reports.md)|All TPRM users|
|Identify and assess the potential risk that is associated with your third-party relationship.|[TPRM Risk activity page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-risk-activity-page.md)|All TPRM users|
|Pinpoint the geographical locations of active third parties and engagements. You can configure filters to view particular risk ratings and engagement types.|[TPRM Risk concentration map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-risk-concentration-map.md)|All TPRM users|
|Prioritize assessments, issues, and tasks that need attention.|[TPRM Risk activity page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-risk-activity-page.md)|All TPRM users|
|Access tasks that are assigned to you and to members of your group.|[TPRM Task page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-task-page.md)|All TPRM users|
|Access all items that you can view or act on in TPRM.|[TPRM List page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-list-page.md)|All TPRM users|
|Use the engagement page to access all current information and status for a third party or engagement.|[Get an overview of a third party](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-tp-working-on.md)|All internal users|
|Import existing data \(third parties, engagements, assessments, questionnaires, issues, and so on\) from other systems \(like the Aravo platform, the ProcessUnity platform, and so on\). You aren’t charged for importing the data.|[Import existing data from other systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-historical-data-import.md)|TPR Managers and TPR Admins|
|Work on all processes in the workflow for a due diligence request: IRQs, external due diligence, approval, contract risk, and closed requests.|[Monitoring the due diligence request process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-dd-mgt-pg-overview.md)|TPR Managers and TPR Admins|
|Use the third-party portal as a primary point of interaction for third parties and risk assessors.|[Managing the Third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/vendor-portal.md)|TPR Managers, TPR Assessors, and Third parties|

For more information on the terminology used in TPRM, see [Terminology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-terminology.md).

## What to explore next

To learn more about configuring and using Third-party Risk Management, see:

-   [Configuring Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-configuring.md)
-   [Classic assessment configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ongoing-config.md)
-   [Smart assessment configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sae-assessment-config.md)
-   [Requesting third-party risk due diligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-requesting-tpr-due-diligence.md)
-   [Assessing your third-party risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-assessing-tpr.md)
-   [Monitoring your third-party risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-monitoring-tpr.md)
-   [Approving or rejecting requests for due diligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-approving.md)
-   [Managing the contract risk process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-contract-risk-process.md)
-   [Using digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dora.md)
-   [Managing the Third-party portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/vendor-portal.md)
-   [Using risk intelligence reports and scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-riskintel-using.md)
-   [Integrating scores from risk intelligence providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-riskintelprvdr-overview.md)
-   [Third-party Risk Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-reference.md)

**Related topics**  


[Due diligence workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-workflow-in-workspace.md)

[Smart assessments with Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sae-using.md)

[Exploring software bill of materials collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-exploring.md)

[AI-assisted questionnaire pre-fill using the Document Management System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-dms-sae.md)

