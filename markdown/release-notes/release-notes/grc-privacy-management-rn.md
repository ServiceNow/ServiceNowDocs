---
title: Privacy Management release notes
description: The ServiceNow Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. Privacy Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Privacy Management release notes

The ServiceNow® Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. Privacy Management was enhanced and updated in the Zurich release.

## Privacy Management highlights for the Zurich release

-   A new external Personal data rights \(PDR\) request form enables customers, ex-employees, and third parties to submit PDR requests from a website with email verification.
-   Access Control by Legal Entity feature enables teams to access only processing activities relevant to their legal entity, maintaining privacy by design principle.
-   Now Assist for Privacy Management plugin uses Generative AI to streamline privacy workflows by summarizing assessments, condensing issues, and merging control objectives.
-   Reporting privacy incidents through email feature enables employees to report privacy incidents directly through email.
-   Impacted and related areas configuration allows privacy case managers to add custom business area types to privacy cases for better context.
-   Revamped Processing Activity overview page provides a unified dashboard showing key compliance and risk metrics for processing activities.

See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Privacy Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Personal Data Rights \(PDR\) external-facing form](https://www.servicenow.com/docs/access?context=pdr-external-facing&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    A new external-facing form for personal data rights \(PDR\) requests is now available, enabling customers, ex-employees, and third party individuals to initiate PDR requests directly from a company's website, without needing Employee Center access. The form allows users to submit various requests, including Right to Know, Right to Delete, Right to Correct, and Right to Opt-Out, with the flexibility to add additional request types as required. An email-based verification process ensures security before processing the PDR request. The PDR form is customizable and can be easily embedded on external sites.


-   **[Accessing control through organizational structure](https://www.servicenow.com/docs/access?context=access-control-by-legal-entity&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Access control by legal entity feature allows teams to access processing activities relevant only to their legal entity. This ensures teams view only their own records, maintaining adherence to the privacy by design principle. By limiting access according to legal entities, this feature reduces operational risks and enables organizations to manage privacy requests and regulatory compliance effectively.


-   **[Now Assist for Privacy Management](https://www.servicenow.com/docs/access?context=now-assist-for-privacy-management&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Now Assist for Privacy Management leverages GenAI to support privacy workflows by summarizing risk assessments, condensing issue details, and identifying redundant control objectives and merging them into a common control objective. Now Assist for Privacy Management is delivered as a separate plugin, requiring administrators to activate specific skills and assign the new sn\_prm\_gen\_ai.user role to access these features.


-   **[Report a privacy case through email](https://www.servicenow.com/docs/access?context=add-issues-email&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Employees can now report privacy incidents directly through email, eliminating the need for complex forms or portals. This enhancement simplifies the reporting process, enabling faster case handling and efficient tracking of privacy issues.


-   **[Impacted and related areas configuration](https://www.servicenow.com/docs/access?context=configure-record-type-area&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Record Type Configuration feature allows privacy case managers or analysts to add additional relevant business area types in impacted and related areas. When creating or updating a privacy case, users can select from pre-defined options to add these areas, ensuring that each case accurately reflects its business context.


-   **[Data subjects](https://www.servicenow.com/docs/access?context=data-subjects&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Select and define the multiple data subject types for each processing activity. You can capture the volume of data subjects that were processed, the specific data elements that were collected from the users, and the user locations. With this feature, you get a realistic, granular, and scalable representation of your processing activities.

-   **[Privacy management dashboard](https://www.servicenow.com/docs/access?context=privacy-manager-dashboard&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Get an overview of your complete privacy risk and compliance posture from the Privacy Management dashboard so that you can quickly prioritize and remediate your processing activities. By looking at the Processing Activities, Risk &amp; Compliance, and Operations &amp; Case management sections, you can see the overall compliance score, trends, privacy criticality assessment scores, and risk heatmap. From the dashboard, you can also see information about the global legal framework to understand the regional obligations and the built-in risk metrics that automatically assess each processing activity.

-   **[New screening and PIA templates](https://www.servicenow.com/docs/access?context=privacy-mgmt-workflow&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Use the new Privacy Impact Assessments \(PIAs\) and Screening Assessment templates that provide standardized questions, evaluation criteria, and workflows so that you can perform a processing activity criticality and privacy risk assessment. With these new templates, you can ensure consistency, reduce manual effort, and support compliance with regulatory and organizational requirements.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Processing activity tab](https://www.servicenow.com/docs/access?context=processing-activity-tab&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The revamped Processing Activity overview page provides a unified dashboard that displays key compliance and risk metrics, such as risk scores, compliance scores, and criticality scores. This update makes it easier for privacy managers and analysts to assess the status of each processing activity, track open issues, and prioritize actions.


-   **[Layout for processing activity record view](https://www.servicenow.com/docs/access?context=processing-activity-homepage&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The vertical layout of a processing activity enables you to see the information in a top-down linear flow. With this layout, you can see the sequential representation of a data processing workflow.

-   **[Privacy management home page](https://www.servicenow.com/docs/access?context=privacy-mgmt-ws-privacy-compliance-manager&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The enhanced Privacy Management home page now has dedicated tabs for Processing Activity, Risk and compliance, Operations, and Privacy Cases. This updated layout helps to improve readability by organizing your reports into clearly defined sections.


## Activation information

Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

