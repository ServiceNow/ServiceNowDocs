---
title: AI Risk and Compliance release notes
description: The ServiceNow AI Risk and Compliance application helps you to manage your AI capabilities ethically, mitigate AI risks, and ensure compliance. AI Risk and Compliance was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# AI Risk and Compliance release notes

The ServiceNow® AI Risk and Compliance application helps you to manage your AI capabilities ethically, mitigate AI risks, and ensure compliance. AI Risk and Compliance was enhanced and updated in the Australia release.

## AI Risk and Compliance highlights for the Australia release

-   Classify AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), enabling early risk identification and consistent AI governance decisions across the system life cycle.
-   Submit AI cases anonymously to report potential AI risks or concerns without disclosing your identity, helping improve early risk visibility and participation in AI governance.
-   Offboard AI assets with structured life-cycle tasks to help ensure governance and risk activities are completed when systems are retired or replaced.

See AI Risk and Compliance for more information.

**Important:** AI Risk and Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the AI Risk and Compliance release

-   **Risk‑based classification during intake**

    After upgrading to version 22.0.3, if you have the AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, you can now classify AI systems using a risk‑based approach at intake, enabling organizations to capture AI risk context early and align governance workflows with regulatory and internal risk requirements. This improvement to the AI use case request form supports more accurate AI oversight throughout the system life cycle.

-   **Report an AI case anonymously**

    After upgrading to version 22.0.3, if you have the AI case business user \[sn\_ai\_case\_mgmt.ai\_case\_business\_user\] role, you can navigate to the Employee Center to access the Anonymous Reporting Center and submit AI cases anonymously, enabling broader participation in AI governance while protecting the identity of reporters. No additional role is required to submit an anonymous report directly through the Anonymous Reporting Center. Broader participation helps organizations identify potential AI risks earlier by removing barriers to case submission.

-   **Offboard AI models and datasets**

    After upgrading to version 22.0.3, if you have the AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role you can manage AI asset offboarding life cycle tasks. Managing these tasks helps ensure that governance‑related activities, such as risk and impact assessments, conformity reviews, issue closure, and audit documentation, are addressed when an AI asset is retired or removed from active use.


## UI changes

-   **Operations tab**

    On the Operations tab in the AI Risk and Compliance Workspace, the AI systems by state section includes an Offboard state to track AI systems in retirement/offboarding and the AI systems by department section now supports grouping by Risk classification from the Show by drop-down list to view the distribution of AI systems in each department.

-   **AI use case request form**

    A Use and Purpose section containing screening questions has been added to the AI use case request form to capture contextual information about how an AI system will be used and supports automated risk‑based classification during submission.

-   **AI system record page**

    A Use and Purpose section has been added to the AI system record page, which you can access from the AI asset inventory list in the AI Risk and Compliance Workspace.

-   **Anonymous AI case reporting**

    A Visit Anonymous Report Center card is available in the Support resources section of the AI assets page in the Employee Center, enabling you to navigate to the Anonymous Report Center to submit an anonymous AI case.


## Activation information

Install AI Risk and Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **AI Control Tower**

    Use the ServiceNow®AI Control Tower application with AI Risk and Compliance to oversee and manage the AI asset inventory life cycle.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

