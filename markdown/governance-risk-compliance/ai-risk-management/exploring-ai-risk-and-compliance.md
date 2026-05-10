---
title: Exploring AI Risk and Compliance
description: Learn how you can use the AI Risk and Compliance application to manage your artificial intelligence \(AI\) capabilities ethically, mitigate AI risks, and ensure compliance.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Exploring AI Risk and Compliance

Learn how you can use the AI Risk and Compliance application to manage your artificial intelligence \(AI\) capabilities ethically, mitigate AI risks, and ensure compliance.

## AI Risk and Compliance overview

The AI risk and compliance team is responsible for identifying and assessing risks associated with AI. This includes evaluating legal, regulatory, and ethical considerations to ensure that the AI capabilities are implemented responsibly. Their role is to establish guidelines and frameworks that enable the organization to adopt AI solutions while maintaining compliance with industry standards and ethical principles. The AI Risk and Compliance application enables the risk and compliance team of an organization to manage their AI capabilities and assets.

## AI Risk and Compliance users

The users listed in the following table represent generic roles. Each of these roles may be identified by different titles and names in various organizations. For specific roles within the AI Risk and Compliance application, refer to [Roles installed with AI Risk and Compliance](../reference/roles-installed-with-ai-risk-and-compliance.md).

<table id="table_pyh_bxl_p2c"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI product owner, Business user, IT asset owner, AI practitioner

</td><td>

-   Initiates requests to create AI use cases, models, and datasets through the workspace or the Employee Center.
-   Monitors AI system performance drives continuous improvements, and assesses business impact.
-   Maintains compliance with governance, ethical, and legal standards throughout the AI product life cycle.
-   Actively engages in responsible AI practices at key development and administration points, and accesses approved AI Assets for discovery and reuse.

</td></tr><tr><td>

AI steward

</td><td>

-   Ensures that the AI systems adhere to ethical principles like fairness, transparency, accountability, and non-discrimination, and regularly reviews models and outputs to help prevent harm and bias.
-   Promotes fairness in AI decision-making by identifying and addressing biases in training data, algorithms, and outcomes, and conducts periodic impact and risk assessments.
-   Oversees the entire life cycle of AI models, from ideation to retirement, and acts as a liaison between teams to integrate governance across departments, ensuring compliance with data privacy, security, and intellectual property protection.
-   Identifies and mitigates potential risks, such as privacy concerns and technological malfunctions, through regular testing, monitoring, and updates, and quickly adapts to changes in policies and regulations through workflow updates and issue management.

</td></tr><tr><td>

Chief risk officer

</td><td>

-   Establishes frameworks for responsible AI use, ensuring adherence to ethical guidelines, industry regulations, and risk management policies.
-   Manages the AI strategy implementation.

</td></tr><tr><td>

AI risk and compliance analyst

</td><td>

Views and manages compliance and risk inventories, for example, authority documents, risk statements, policies, and controls, as well as accesses the Advanced Risk dashboards.

</td></tr><tr><td>

AI risk and compliance admin

</td><td>

-   Sets up risk and impact assessment frameworks by configuring risk assessment methodologies, contribution factors, and impact templates, for example, conformity assessments.
-   Sets up automation rules for impact assessments to identify applicable AI risks and controls.
-   Defines AI case types, applies business rules for form fields and assignments, and designs reporting templates to meet business needs.

</td></tr></tbody>
</table>## AI Risk and Compliance workflow

The following section describes the steps involved when an AI asset is created in the AI Control Tower application and the risks for the assets are assessed in the AI Risk and Compliance application until the asset is deployed and moves to being monitored.

When a new AI system is introduced or enhanced, it undergoes a risk assessment and an AI impact assessment. These assessments yield scores that denote the risk levels for the AI systems. After the approval is obtained from the relevant stakeholders, the development or build phase begins. During development, controls are attested, issues are tracked and managed, and policy exceptions are raised as needed from a risk and compliance perspective. Following development, the AI system is reviewed to ensure:

-   Completion of conformity assessment
-   Review and resolution of open issues and policy exceptions
-   Reassessment of risks

Based on these evaluations, the AI system is either approved or rejected for deployment.

The workflow for an AI asset creation and deployment is the following:

1.  Business users use the Employee Center or the AI Control Tower workspace and submit a new AI use case.
2.  A new inventory record is automatically created in the workspace.
3.  The AI Center of Excellence \(COE\) team reviews the submitted use case.
4.  Relevant assets are added to the inventory to help determine if the use case should proceed to the next stage.
5.  In the AI Risk and Compliance workspace, either an AI impact assessment or an AI conformity assessment is initiated.
6.  The assigned business user completes the assessment in the workspace.
7.  Based on the assessment results, potential risks and necessary controls are identified and mapped.
8.  After the assessment is approved, the AI use case is built by the appropriate teams.
9.  The completed solution undergoes a formal review process.
10. Ongoing monitoring is performed to ensure compliance and performance.
11. After successful review, the solution is deployed to production.

## AI Risk and Compliance benefits

The AI Risk and Compliance application addresses the following challenges faced by any organization that uses AI:

-   Lack of AI strategy: No commonly agreed-upon AI strategy or alignment with corporate goals.
-   No centralized management: No single platform for all stakeholders and for the Chief AI officer to collaborate and manage AI use.
-   No responsible AI guidelines: Absence of guidelines for ethical and responsible AI use.
-   No risk assessment process: No process to evaluate risks for in-house and third-party AI.
-   Scalability and monitoring issues: Challenges in scaling AI deployment, tracking performance, and continuously monitoring for emerging risks like privacy.

The following table lists the benefits of using the AI Risk and Compliance application.

<table id="table_ejf_j3j_fcc"><thead><tr><th>

Benefits

</th><th>

Feature

</th><th>

Role

</th></tr></thead><tbody><tr><td>

Manage AI systems, models, and datasets across their entire life-cycle with consistent governance for better visibility, control, and compliance.

</td><td>

[AI asset lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-asset-lifecycle.md)

</td><td>

AI steward

</td></tr><tr><td>

Perform impact assessments for AI systems, models, and datasets to identify high-risk AI assets.

</td><td>

[Perform impact assessment on an AI use case](../task/perform-impact-assessment-of-ai-use-case.md)

</td><td>

The roles required are as follows:-   AI Control Tower: AI Asset Owner
-   AI Risk and Compliance: AI Risk and Compliance User

</td></tr><tr><td>

Perform risk assessments on AI system and individual risks associated with an AI asset based on additional information and testing.

</td><td>

[Perform risk assessments on AI systems](../task/perform-risk-assessments-on-ai-systems.md)[Initiate risk assessment on AI asset's risks](../task/request-risk-assessments-for-ai-systems.md)

</td><td>

AI Risk and Compliance Analyst

</td></tr><tr><td>

Manage and oversee AI-related cases and issues through a structured case management process.

</td><td>

[Create an AI case in the AI Risk and Compliance workspace](../task/create-ai-case-in-the-ai-risk-and-compliance-workspace.md)

 [Create an AI issue in the AI Risk and Compliance workspace](../task/create-ai-issue-in-the-ai-risk-and-compliance-workspace.md)

</td><td>

The roles required are as follows:-   AI case: AI Case Analyst and AI Case Manager
-   AI issue: AI Risk and Compliance Manager and AI Risk and Compliance Analyst

</td></tr><tr><td>

Build a compliance-ready AI asset inventory aligned with regulatory requirements using the AI framework content pack.

</td><td>

-   [AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-assets.md)
-   [Create control attestations for AI asset](../task/attest-controls-for-ai-systems.md)

</td><td>

AI Risk and Compliance Analyst

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using AI Risk and Compliance, see:

-   [Configuring AI Risk and Compliance](configuring-ai-risk-and-compliance.md)
-   [Using AI Risk and Compliance](using-ai-risk-and-compliance.md)
-   [AI Risk and Compliance reference](../reference/ai-risk-and-compliance-reference.md)

