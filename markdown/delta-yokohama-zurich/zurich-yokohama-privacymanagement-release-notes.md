---
title: Combined Privacy Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Privacy Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-privacymanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Privacy Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Privacy Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Privacy Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Privacy Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Privacy Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[\[Placeholder link text to key bundle-grc.configure-criticality-factors\]](https://servicenow-staging.fluidtopics.net/access?context=configure-criticality-factors&family=yokohama&ft:locale=en-US)**

Leverage criticality factors to evaluate the initial risks associated with processing activities. Integrate these factors into privacy assessments and automatically generate a criticality score upon assessment approval. These factors are also added to processing activities, enabling you to make updates at any time. Integrating these factors in a privacy assessment eliminates the need for a separate criticality assessment. This consolidation reduces the workload for the privacy teams.

-   **[Smart assessments](https://servicenow-staging.fluidtopics.net/access?context=smart-assessments-in-privacy-management&family=yokohama&ft:locale=en-US)**

Use the new and improved assessment experience that enables:

    -   capturing the data elements, the information object attributes, hierarchies
    -   building the assessment questionnaire
This new experience enables responders to update all the necessary details within the assessments, eliminating the need to update the processing activity separately.

-   **[Configure categories](https://servicenow-staging.fluidtopics.net/access?context=configure-information-object-categories&family=yokohama&ft:locale=en-US)**

Implement Information object categories to tag and classify information objects effectively. For example, attributes like iris scans and fingerprints are often referred to as biometric data, or email addresses and phone numbers can be tagged as contact information. Information object categories enable you to categorize these information objects under these broader classifications. This approach is useful in the following ways:

    -   Enhances compliance with regulations such as GDPR, CCPA, and so on by accurately capturing and tracking required data categories.
    -   Improves clarity for business users, ensuring they can easily identify and work with terms they’re familiar with while adhering to regulatory standards.
    -   Streamlines data governance by creating a structured framework that supports both regulatory needs and business operations.
-   **[Smart assessment for privacy case management action tasks](https://servicenow-staging.fluidtopics.net/access?context=accept-a-case-task&family=yokohama&ft:locale=en-US)**

Use the new assessment experience of Smart Assessment Engine for privacy case action tasks. Only when an action task moves from the **Draft** to the **Assigned** state, the assessment can be sent. To use the smart assessment, a new property called enable\_smart\_assessments \(sn\_grc\_case\_mgmt.enable\_smart\_assessments\) is introduced with the default value as **true**.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Data subjects](https://servicenow-staging.fluidtopics.net/access?context=data-subjects&family=zurich&ft:locale=en-US)**

Select and define the multiple data subject types for each processing activity. You can capture the volume of data subjects that were processed, the specific data elements that were collected from the users, and the user locations. With this feature, you get a realistic, granular, and scalable representation of your processing activities.

-   **[Privacy management dashboard](https://servicenow-staging.fluidtopics.net/access?context=privacy-manager-dashboard&family=zurich&ft:locale=en-US)**

Get an overview of your complete privacy risk and compliance posture from the Privacy Management dashboard so that you can quickly prioritize and remediate your processing activities. By looking at the Processing Activities, Risk &amp; Compliance, and Operations &amp; Case management sections, you can see the overall compliance score, trends, privacy criticality assessment scores, and risk heatmap. From the dashboard, you can also see information about the global legal framework to understand the regional obligations and the built-in risk metrics that automatically assess each processing activity.

-   **[New screening and PIA templates](https://servicenow-staging.fluidtopics.net/access?context=privacy-mgmt-workflow&family=zurich&ft:locale=en-US)**

Use the new Privacy Impact Assessments \(PIAs\) and Screening Assessment templates that provide standardized questions, evaluation criteria, and workflows so that you can perform a processing activity criticality and privacy risk assessment. With these new templates, you can ensure consistency, reduce manual effort, and support compliance with regulatory and organizational requirements.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Privacy Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Tagging of information object tags](https://servicenow-staging.fluidtopics.net/access?context=tag-io-with-pi&family=yokohama&ft:locale=en-US)**

Use the **Data classification** field to tag information objects instead of using the tag icon.

-   **[Initiating privacy assessment](https://servicenow-staging.fluidtopics.net/access?context=send-privacy-asmt-from-pa&family=yokohama&ft:locale=en-US)**

When you initiate a privacy assessment from either an entity or a processing activity, you’re no longer redirected to the **Create new privacy assessment form**, instead, a new pop-up window appears where you can specify all the assessment details.


</td></tr><tr><td>

Zurich

</td><td>

-   ****

-   **[Processing activity tab](https://servicenow-staging.fluidtopics.net/access?context=processing-activity-tab&family=zurich&ft:locale=en-US)**

The revamped Processing Activity overview page provides a unified dashboard that displays key compliance and risk metrics, such as risk scores, compliance scores, and criticality scores. This update makes it easier for privacy managers and analysts to assess the status of each processing activity, track open issues, and prioritize actions.


-   **[Layout for processing activity record view](https://servicenow-staging.fluidtopics.net/access?context=processing-activity-homepage&family=zurich&ft:locale=en-US)**

The vertical layout of a processing activity enables you to see the information in a top-down linear flow. With this layout, you can see the sequential representation of a data processing workflow.

-   **[Privacy management home page](https://servicenow-staging.fluidtopics.net/access?context=privacy-mgmt-ws-privacy-compliance-manager&family=zurich&ft:locale=en-US)**

The enhanced Privacy Management home page now has dedicated tabs for Processing Activity, Risk and compliance, Operations, and Privacy Cases. This updated layout helps to improve readability by organizing your reports into clearly defined sections.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Privacy Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Privacy Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Privacy Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Privacy Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Privacy Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Privacy Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Privacy Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Privacy Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Privacy Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Integrate criticality factors into assessments and processing activities thereby simplifying the assessment process, and reducing the workload for privacy teams.
-   Use the Smart Assessment Engine to capture details regarding information objects and hierarchies, updating all details within the assessments and eliminating the need to separately update processing activities.
-   Implement information Object \(IO\) categories such as biometric data, to align with regulatory classifications and bridge the gap between requirements and user understanding.
-   Empower privacy case analysts to perform assessments on privacy cases using the Smart Assessment Engine

 See [Privacy Management](https://servicenow-staging.fluidtopics.net/access?context=privacy-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   A new external Personal data rights \(PDR\) request form enables customers, ex-employees, and third parties to submit PDR requests from a website with email verification.
-   Access Control by Legal Entity feature enables teams to access only processing activities relevant to their legal entity, maintaining privacy by design principle.
-   Now Assist for Privacy Management plugin uses Generative AI to streamline privacy workflows by summarizing assessments, condensing issues, and merging control objectives.
-   Reporting privacy incidents through email feature enables employees to report privacy incidents directly through email.
-   Impacted and related areas configuration allows privacy case managers to add custom business area types to privacy cases for better context.
-   Revamped Processing Activity overview page provides a unified dashboard showing key compliance and risk metrics for processing activities.

 See [Privacy Management](https://servicenow-staging.fluidtopics.net/access?context=privacy-management&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

