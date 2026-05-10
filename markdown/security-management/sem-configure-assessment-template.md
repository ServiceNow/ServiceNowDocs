---
title: Configure an assessment template
description: Assessment templates contain the questions prompted during the request process \(such as, when requesting an exception\). The above-mentioned preconfigured templates are provided with smart assessment. You can also create your own templates as required.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Questionnaire support in Exception Management via Smart Assessment, Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Configure an assessment template

Assessment templates contain the questions prompted during the request process \(such as, when requesting an exception\). The above-mentioned preconfigured templates are provided with smart assessment. You can also create your own templates as required.

## Before you begin

Role required:

**Template Reader Role**: **sn\_vul\_cmn.smart\_assessment\_reader** enables you \(Approver\) to read the submitted questionnaire responses.

**Template Actor Role**: **sn\_vul\_cmn.smart\_assessment\_actor** enables you \(Remediation Owner and Admin\) to fill out the questionnaires/assessments.

## About this task

In the Security Exposure Management workspace, you can select the template with the assessment target as Change Approval \(CA\), to be used for the exception request \(such as, Exception for Vulnerability Response, False Positive for Vulnerability Response\). If you select the default template, it automatically populates the questions. If you choose to create your own template, it can be modified.

## Procedure

1.  Navigate to the **Assessment Workspace**.

2.  Select an existing **Assessment Template** or select a **New Template**

3.  Fill in the following details:

    -   **Template Name**: Unique name for the template
    -   **Assessment Name**: Name displayed in the system when viewing the assessment.
    -   **Template Categories**: Templates are categorized for easier management. Some template categories are provided by default, for example, Vulnerability Response Questionnaire Templates. Alternatively, you can also create templates of your choice.
    -   **Assessment Targets**: Specifies the table that the template is related to. For VR, it’s the CA table \(Change Approval table\).

**Parent Topic:**[Questionnaire support in Exception Management via Smart Assessment](../concept/sem-smart-assessment-exp-management.md)

