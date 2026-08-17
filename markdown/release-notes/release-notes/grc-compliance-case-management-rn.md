---
title: Compliance Case Management release notes
description: The ServiceNow Compliance Case Management application helps you to report, investigate, and resolve compliance cases, such as complaints and breaches. Compliance Case Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Compliance Case Management release notes

The ServiceNow® Compliance Case Management application helps you to report, investigate, and resolve compliance cases, such as complaints and breaches. Compliance Case Management was enhanced and updated in the Australia release.

## Compliance Case Management highlights for the Australia release

-   ServiceNow Otto is the new name for the Now Assist experience, delivering agentic AI, multimodal interactions, and autonomous cross-system workflow orchestration.
-   Update an assessment template to send new assessments with the latest version, without disrupting the ones that are already in progress.
-   Automatically generate an AI-recommended compliance case summary from varied compliance case data, reducing investigation time and enabling faster, more consistent decision-making.
-   Anonymously report compliance violations through a secure portal that maintains complete identity protection while enabling organizational trust and regulatory compliance.

See  for more information.

**Important:** Compliance Case Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Smart assessment versioning of assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/update-ccm-asmt-template.md)**

    You can create a version of an existing compliance case assessment template to revise the questionnaire and response options, without disrupting assessments that are already in progress. New assessments use the latest published version of the template.

-   **[Report a compliance case anonymously from the Anonymous Reporting Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/report-compliance-case-anonymously.md)**

    Employees can now use the Anonymous Reporting Center to report compliance violations such as fraud and embezzlement, workplace misconduct \(harassment, discrimination\), bribery and corruption, and other concerns without revealing their identity or location.

    Accessed through the Employee Center, the Anonymous Reporting Center portal automatically logs users out to enforce anonymity, creates case records without mapping to employee identity, and provides a unique report key and report number for secure follow-up communication.

    CAPTCHA‑based verification is used to authenticate submissions, and the system generates a report statement summarizing the case after submission. Employees can save a copy of their report for future reference. For security and confidentiality, the submitted information is not displayed again. Reports are routed to the appropriate compliance team based on the nature of the concern.

    Throughout the investigation process:

    -   Investigators can request additional information through a comments system visible to the reporter
    -   Reporters can follow up on their case using their report key to check progress and respond to questions
    -   All interactions maintain reporter anonymity at every step; no identity or location data is ever captured or linked
    This enhancement enables organizations to build trust, mitigate risks before escalation, and ensures regulatory compliance with whistleblower protection requirements.

-   **[GRC case summarization skill for compliance cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/compliance-case-summarization-skill.md)**

    After upgrading ServiceNow Otto for Integrated Risk Management \(IRM\) application to version 22.x, Compliance analysts can use the case summarization feature to quickly understand a compliance case without manually reviewing every field, attachment, or related list.Now Assist analyzes key case attributes—such as timelines, impacted areas, evidence, and actions—and generates a structured summary directly inside the compliance case.

    This solves a common problem: case data is often lengthy, scattered across multiple related lists, and difficult for analysts to digest efficiently. Analysts can also save and edit summaries as case data evolves, ensuring the record stays current.

    By consolidating all relevant information into a single, coherent narrative, Now Assist reduces investigation time, improves consistency across reviewers, and supports faster decision-making.


## Changed in this release

-   **[ServiceNow Otto® name announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-ai-implementation-landing.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

    The Now Assist for IRM \(sn\_irm\_gen\_ai\) plugin, which provides generative AI capabilities for Compliance Case Management, has been renamed to ServiceNow Otto for IRM.


-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Activation information

Install Compliance Case Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

