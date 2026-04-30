---
title: Questionnaire support in Exception Management via Smart Assessment
description: Configure advanced questionnaires as part of the exception management process using Smart Assessment. This enables Remediation Owners to provide more detailed context for Exception Requests and enables Approvers to configure conditional questions to gather information for informed decision making.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-08-01"
reading_time_minutes: 1
breadcrumb: [Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Questionnaire support in Exception Management via Smart Assessment

Configure advanced questionnaires as part of the exception management process using Smart Assessment. This enables Remediation Owners to provide more detailed context for Exception Requests and enables Approvers to configure conditional questions to gather information for informed decision making.

## Roles Required

**Smart Assessment Template Reader**: **sn\_vul\_cmn.smart\_assessment\_template\_manager** \(Vulnerability admin and Template reader\) enables admins to create and edit templates.

**Smart Assessment actor**: **sn\_vul\_cmn.smart\_assessment\_actor** enables you \(Remediation Owners and Admins\) to fill out the questionnaires/assessments.

**Smart Assessment reader**: **sn\_vul\_cmn.smart\_assessment\_reader** enables you \(Approver\) to read the submitted questionnaire responses.

Pre-requisite: The smart assessment plug-ins must be installed as the Smart Assessment is a dependency.

You can configure questionnaires as part of the Exception Management process using Smart Assessment. It enables Vulnerability Admins/Manager to configure conditional questions to gather the right information needed for informed decision-making, while enabling Remediation Owners to provide more detailed context for exception requests. This enhances collaboration between the Vulnerability Management and Remediation teams by streamlining the approval process and ensuring clarity and completeness of exception justifications.

In the **Exception Management Configuration** screen from any of the four options- **Vulnerability Response**, **Application Vulnerability Response**, **Container Vulnerability Response**, and **Configuration Compliance** you can select the Assessment for Compensating Control, request exception and false positive records.

You can use the **Smart Assessment** to manage the Questionnaires in Security Exposure Management Workspace.

Templates can be accessed/edited by the Smart Assessment Template Reader: **sn\_vul\_cmn.smart\_assessment\_template\_manager**.

-   **[Questionnaire Configuration form fields](../reference/sem-compensating-controls-approval-rule.md)**  
You can define distinct questionnaire for a distinct collection of vulnerabilities or remediation tasks by filtering the vulnerabilities or remediation tasks respectively.
-   **[Configure an assessment template](../task/sem-configure-assessment-template.md)**  
Assessment templates contain the questions prompted during the request process \(such as, when requesting an exception\). The above-mentioned preconfigured templates are provided with smart assessment. You can also create your own templates as required.
-   **[Use case for False positive or Request Exception Questionnaire](../reference/sem-ques-for-false-positive-or-request-exp.md)**  
Scenario when the questionnaire for False Positive or Request Exception is raised but not filled completely.

**Parent Topic:**[Exception Management Overview](sem-exception-management-overview.md)

