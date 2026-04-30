---
title: AI cases and inquiries
description: AI cases and inquiries provide a structured way to report, track, and manage AI-related concerns and questions as part of AI governance in AI Control Tower and AI Risk and Compliance.
locale: en-US
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [AI case management, AI cases, AI inquiries, AI Risk and Compliance, AI Control Tower, AI governance, Employee Center]
breadcrumb: [AI governance life cycle, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI cases and inquiries

AI cases and inquiries provide a structured way to report, track, and manage AI-related concerns and questions as part of AI governance in AI Control Tower and AI Risk and Compliance.

## AI cases and inquiries overview

The AI Case Management application is used as part of AI Risk and Compliance \(AIRC\). It provides the workflows used to review, investigate, and respond to AI‑related risks, incidents, and governance questions associated with AI systems, models, and datasets governed in AI Control Tower \(AICT\). AI cases and inquiries help identify potential issues, capture governance signals, and ensure that AI systems align with organizational policies, regulatory expectations, and ethical principles across the AI life cycle. You can view AI cases and inquiries from the AI Risk and Compliance dashboard.

![AI cases tab on the AI risk and compliance dashboard.](../image/ai-case-landing-page.png "AI cases tab on the AI risk and compliance dashboard")

![Inquiries tab on the AI risk and compliance dashboard.](../image/ai-cases-inquiries-tab.png "Inquiries tab on the AI risk and compliance dashboard")

## AI cases and AI inquiries

AI cases and AI inquiries represent two related intake types used to capture AI-related input from users and stakeholders.

AI cases are typically used to report observed AI-related concerns, risks, incidents, or potential noncompliance. AI inquiries are used to ask questions or request guidance related to AI systems, acceptable usage, governance requirements, or next steps.

**Note:** The distinction between cases and inquiries may vary by organization and configuration. Both follow a structured review and management process once submitted.

## Submission and intake

AI Case Business Users \[sn\_ai\_case\_mgmt.ai\_case\_business\_user\] submit AI cases and inquiries through the Employee Center to report concerns or request guidance. Submissions include descriptive information that helps reviewers understand context, such as the AI system, model, or dataset involved, observed behavior or concern, impacted users or business areas, and any supporting details or attachments. For more information, see [Report an AI case from the Employee Center](../task/report-ai-case.md).

After upgrading to version 22.0.3 and installing the AI Case Management application, organizations can enable anonymous submission of AI cases through the Employee Center. Anonymous reporting supports broader participation in AI governance while protecting the identity of the reporter.

**Note:** When the AI Case Management application is installed, the Anonymous Report Center record producers and plugin are installed and enabled by default.

Before an anonymous report is saved, all free‑text fields in the forms \(such as case type, summary, business unit, and jurisdiction\) are sanitized to accomplish the following.

-   Remove HTML and embedded script or style content
-   Restrict input to standard alphanumeric characters and basic punctuation
-   Trim extra whitespaces

Sanitization helps reduce the risk of unsafe or malformed input.

For more information, see [Report an AI case anonymously](../task/report-ai-case-anon.md), [Follow up on a report from the Anonymous Reporting Center](../../grc-common/task/grc-follow-up-anonymously.md), and [Anonymous Reporting Center](../../grc-common/concept/grc-anonymous-reporting-center.md).

## Case management and follow-up

After submission, AI cases and inquiries are managed in the AI Risk and Compliance Workspace. AI Risk and Compliance analysts \[sn\_ai\_case\_mgmt.ai\_case\_analyst\] review case details, investigate reported issues, assess potential impact, and work assigned governance tasks.

AI Risk and Compliance managers \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] who inherit the AI case manager \[sn\_ai\_case\_mgmt.ai\_case\_manager\] role oversee case status, prioritize work, and coordinate follow-up across governance teams. Cases can result in tasks, identification of impacted areas such as policies or regulations, and the creation of related issues to support remediation, escalation, or ongoing governance activities across the AI life cycle.

## Roles and access

Access to create and manage AI cases and inquiries is controlled through roles that support separation of duties and least-privilege access.

Business users focus on reporting concerns and requesting guidance. Analysts and managers focus on investigation, assessment, coordination, and oversight. AI stewards \[sn\_ai\_governance\_ai\_steward\] and other governance stakeholders, such as security, legal, privacy, or data governance teams, contribute expertise and perform review or remediation tasks as needed.

Governance stakeholders participate in case review and investigation activities without owning business outcomes or life cycle approval decisions.

For more information, see [Roles installed with AI Risk and Compliance](../reference/roles-installed-with-ai-risk-and-compliance.md).

**Related topics**  


[Create an AI case in the AI Risk and Compliance workspace](../task/create-ai-case-in-the-ai-risk-and-compliance-workspace.md)

[Raise an AI inquiry](../task/raise-ai-inquiry.md)

[AI cases tab](ai-cases-tab-airc.md)

[AI Risk and Compliance workspace](ai-risk-and-compliance-workspace.md)

