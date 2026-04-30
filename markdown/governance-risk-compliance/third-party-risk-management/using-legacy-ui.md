---
title: Working in the VRM Classic user interface
description: While you can continue to use the legacy user interface to perform Vendor Risk Management tasks, the Vendor Management Workspace offers enhanced TPRM features and more useful reports.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Working in the VRM Classic user interface

While you can continue to use the legacy user interface to perform Vendor Risk Management tasks, the Vendor Management Workspace offers enhanced TPRM features and more useful reports.

-   **[Configure a risk assessment to recur on a schedule](../../grc-vendor-risk/task/define-repeating-vend-assess.md)**

    Configure a third-party risk assessment to recur on a schedule to regularly update risk results for a third party or an engagement.

    Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

-   **[Create a VRM third party record](../../grc-vendor-risk/task/tprm-ws-third-party-create-new.md)**

    Configure a third-party risk assessment to recur on a schedule to regularly update risk results for a third party or an engagement.

    Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_manager.

-   **[Setting up VRM third-party hierarchies and engagements](../../grc-vendor-risk/concept/vendor-hierarchy-engagements.md)**

    Create third-party hierarchies by defining the parent-child relationships between the parent third party and all of their subsidiaries. You do this task because some organizations work with third parties that have subsidiaries \(or subsidiaries of subsidiaries\) that can pose a potential risk to your business. You can perform assessments at each subsidiary organization and roll up the results to calculate an overall risk score for the parent third party.

    Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager or sn\_vdr\_risk\_asmt.vendor\_assessor.

-   **[Define a VRM engagement](../../grc-vendor-risk/task/tprm-ws-engagement-request.md)**

    Define an engagement so that you can assess the risks that are associated with the services or products offered by a third party. Engagements can also represent the products or services that are provided to the parent third party, either directly or from departments, partners, or subsidiaries that you can also assess for risk.

    **Tip:** Any person with access to your instance at your organization can request an engagement. That process is typically more streamlined and more effective than the process described here, where a Third-party risk \(TPR\) manager or TPR assessor defines an engagement. For more information, see [Request due diligence for a third-party engagement](../task/tprm-ws-request-dd-for-engagement.md).

    Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager or sn\_vdr\_risk\_asmt.vendor\_assessor.

-   **[VRM third-party risk tiering assessments](../reference/manage-risk-tiering-assessments.md)**

    Organizations use risk tiering to classify their third parties into categories of potential risk posed at the time of onboarding. The standard predefined risk tiers are None, Low, Minor, Moderate, High, and Critical. Each risk tier has associated assessment questions and document requests.

-   **[Managing external risk assessments — Legacy process](../../grc-vendor-risk/concept/c_Issues.md)**

    Before the TPR manager closes an assessment, stakeholders create issues and tasks, usually during the **Generating observations** state. The TPR assessor assigns third parties as needed and communicates using comment streams to achieve closure on non-compliance. The third-party primary contact uses the Third-party portal to view all assessments.

-   **[Create an external assessment — Legacy process](../../grc-vendor-risk/task/create-vendor-risk-assess.md)**

    Create an assessment and initiate the third-party risk assessment life cycle.


**Important:** Starting with version 18.1.3 of Third-party Risk Management the Vendor Risk Overview dashboard is deprecated. If Third-party Risk Management was installed prior to 18.1.3 the Vendor Risk overview dashboard is still available for your use.

