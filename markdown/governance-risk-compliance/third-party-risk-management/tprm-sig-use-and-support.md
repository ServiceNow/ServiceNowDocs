---
title: Using the SIG questionnaire for a risk assessment
description: Third parties can use the Shared Assessments Standardized Information Gathering questionnaire \(SIG\) to provide assessment documentation in the Third-party Risk Management application. The third-party contact can upload the pre-filled SIG spreadsheet or respond to a form-based questionnaire that is imported to the instance.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage the third-party portal, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Using the SIG questionnaire for a risk assessment

Third parties can use the Shared Assessments Standardized Information Gathering questionnaire \(SIG\) to provide assessment documentation in the Third-party Risk Management application. The third-party contact can upload the pre-filled SIG spreadsheet or respond to a form-based questionnaire that is imported to the instance.

## Supported SIG versions

TPRM supports the current SIG version and prior versions up to 2021. The following SIG versions are supported:

-   SIG Full 2025, 2024, 2023, 2022, and 2021
-   SIG Core 2025, 2024, 2023, 2022, and 2021
-   SIG Lite 2025, 2024, 2023, 2022, and 2021

**Note:** SIG 2020 versions are available for reactivation. SIG 2020 versions are deactivated by default.

**Important:**

The base system includes sample SIG questionnaires. These questionnaires don’t provide the correct answers. The templates provided by the Shared Assessments service don’t include the correct answers. You have to determine the correct and wrong answers.

Yes-or-no questions in the sample SIG questionnaires don’t include scoring logic. By default, all Yes answers in the samples are graded as correct. You must configure the logic for your own needs.

## SIG Limitations

Your third party might run into the following issues when using a SIG:

-   If a third party uploads a version prior to the earliest supported SIG, all responses for matching questions are imported and any non-matching questions are imported with empty responses for the third party to answer later.
-   If a third party attempts to load the data from a version of SIG that is older than the current version, some questions might not be mapped or parsed correctly \(for example, if you load data for SIG 2021 full on SIG 2022 full\).
-   Loading a version of SIG prior to 2021 isn’t supported.

**Note:** For more information about using the GRC: SIG Questionnaire Integration plugin, see [Standardized Information Gathering \(SIG\) Questionnaire Integration](../../grc-sig-questionnaire/concept/grc-sig-integration.md), [Install the GRC: SIG Questionnaire Integration](../../grc-sig-questionnaire/task/install-grc-sig-plugin.md), and [Verify the SIG Questionnaire Integration in Third-party Risk Management](../../grc-sig-questionnaire/task/verify-grc-sig-vendor-risk.md).

For instructions that you can send to third-party contacts, see [Respond using the SIG](../task/tprm-tpcontact-use-sig.md).

