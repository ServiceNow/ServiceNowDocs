---
title: Configure TPRM properties
description: Configure property settings for a variety of TPRM operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-properties-configure.html
release: brazil
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Configure TPRM properties

Configure property settings for a variety of TPRM operations.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

## About this task

You can specify the following property settings:

-   **Organization name \[`sn_vdr_risk_asmt.company.name`\]**

    Third-party contacts see this name in all references on the Third-party portal.

-   **Excel cell text delimiter \[`sn_vdr_risk_asmt.excel_choice_delimiter`\]**

    Character string that separates response text in questions of type ‘Choice’ and ‘Multiple Selection’.

    Common delimiters: \\r, \\n, \\t, \\r\\n, and the comma character.

-   **Maximum Excel file size \[`sn_vdr_risk_asmt.excel_file_max_size`\]**

    Maximum file size in MB that can be imported.

-   **Maximum age for reusing responses \[`sn_tprm_dd.max_age_for_questionnaire_reuse`\]**

    Maximum age in days for a questionnaire to be used to pre-populate responses in a new questionnaire. The questionnaire from the most recent closed assessment is used. This setting applies when a user selects the **Include previous responses** option when configuring a questionnaire or questionnaire template.

-   **Allow assessors to answer/edit questionnaires for third-party contacts \[`sn_svdp.allow_assessor_edit`\]**

    You can set the following options:

    -   Enter `answer` to enable TPR assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] to answer questions or modify responses \(default\).
    -   Enter `edit` to enable TPR assessors to modify responses.
    -   Enter `false` to not enable TPR assessors to answer questions or modify responses.
    **Important:** This property applies only to Classic assessments. If Smart Assessment Engine \(SAE\) is enabled \[`sn_vdr_risk_asmt.sae_enabled`\], this property has no effect, and external assessment responses remain read-only for TPR assessors and TPR managers regardless of this setting. To edit responses for an external SAE assessment, TPR assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] and TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can use the assessment reassign \[sn\_smart\_asmt.reassign\] role, which is available to both roles by default, to reassign the in-progress assessment to themselves during the review process. Once reassigned, they are granted edit access to the responses. For more information, see [Smart assessments with Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/third-party-risk-management/tprm-sae-using.md).

-   **Smart Assessment Engine enabled \[`sn_vdr_risk_asmt.sae_enabled`\]**

    The option to use Smart Assessment Engine or Assessment Engine.

    -   Select the check box to enable Smart Assessment Engine for TPRM.
    -   When the check box isn’t selected Smart Assessment Engine isn’t enabled for TPRM.
    **Warning:** You won’t be able to change this setting back once it's set to be "true." After this property is enabled, this selection can’t be reversed.


## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Administration** &gt; **Properties**

2.  For each property, enter the value that meets your need.

    -   Each property entry describes the value to enter.
    -   To view the name of a property, select the help icon \[Omitted image "help-icon.png"\] Alt text:.

