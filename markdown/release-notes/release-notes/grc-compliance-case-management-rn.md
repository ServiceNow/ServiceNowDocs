---
title: Compliance Case Management release notes
description: The ServiceNow Compliance Case Management application helps you to report, investigate, analyze, and resolve a compliance case or raise a compliance request in a centralized location. Compliance Case Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Compliance Case Management release notes

The ServiceNow® Compliance Case Management application helps you to report, investigate, analyze, and resolve a compliance case or raise a compliance request in a centralized location. Compliance Case Management was enhanced and updated in the Yokohama release.

## Compliance Case Management highlights for the Yokohama release

-   Empower compliance professionals to perform assessments on compliance cases using the Smart Assessment Engine.
-   Utilize the unified **Tasks** page on Employee Center to complete your assessments.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Compliance Case Management](https://www.servicenow.com/docs/access?context=compliance-case-management&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Compliance Case Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Smart assessments in Compliance Case Management](https://www.servicenow.com/docs/access?context=smart-assessment-in-ccm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Utilize the Smart Assessment Engine to assess if your employees are compliant with the necessary regulations. The compliance case administrator configures the questionnaire, and when an action task moves from the **Draft** to the **Assigned** state, the assessment is sent. After the assessment, the compliance case manager examines the nature of the non-compliance and its impact on the organization. Based on the findings, appropriate remediation measures are identified and implemented to resolution. To use the smart assessment, a new property called enable\_smart\_assessments \(sn\_grc\_case\_mgmt.enable\_smart\_assessments\) is introduced with the default value as **true**.

-   **[Unified Task-driven UI experience](https://www.servicenow.com/docs/access?context=perform-smart-assessment-on-action-task&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    As a business user, use the **Tasks** page on the Employee Center for a consolidated view of all your tasks, enabling you to access and complete them efficiently. This page provides an easy way to manage all your assessments in one place, enabling you to view and perform tasks seamlessly.


## Changed in this release

-   **[Roles updated for smart assessment](https://www.servicenow.com/docs/access?context=roles-compliance-case-management&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The following roles in Compliance Case Management have been updated with respect to smart assessments.

    -   sn\_comp\_case.compliance\_case\_admin
    -   sn\_comp\_case.compliance\_case\_analyst
    -   sn\_comp\_case.compliance\_case\_business\_user
    -   sn\_comp\_case.compliance\_case\_manager
-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    The Compliance Management configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


## Activation information

Install Compliance Case Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

    The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for details.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

