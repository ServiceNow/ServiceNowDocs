---
title: Combined Smart Assessment Engine release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Smart Assessment Engine from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-smartassessmentengine-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Smart Assessment Engine release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Smart Assessment Engine from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Smart Assessment Engine release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Smart Assessment Engine to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Smart Assessment Engine.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Use template designer](https://www.servicenow.com/docs/access?context=sae-template-designer&family=xanadu&ft:locale=en-US)**

By using the template designer in Smart Assessment Engine, you can easily create assessment templates and add instructions, questions, and reference information to an assessment template.

    -   [Add instructions and questions to an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-template-populate&family=xanadu&ft:locale=en-US): SAE supports the most commonly used question types such as radio buttons, check boxes, drop-down lists, and more. Smart assessments are highly customizable so that you can do the following tasks:
        -   Organize questions into sections and subsections for clarity.
        -   Add instructions to help the assessors understand the context and requirements of each question to improve the accuracy and relevance of the responses.
        -   Configure the question guidance texts to help the assessors answer questions.
        -   Configure the questions to appear or hide depending on the assessor's previous answers.
        -   Integrate the response justification prompts that provide the assessors with the explanations that are based on their selected responses.
        -   Require the assessors to attach the supporting documents like contracts, permits, or invoices that are based on the responses.
    -   [Add reference information to an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-add-reference&family=xanadu&ft:locale=en-US): Incorporate the live data from the Assessment Scope as reference information to help ensure that the assessors have immediate access to the necessary information while they’re responding to the assessments. This live data minimizes the need for external references.
    -   [Create an assessment template category](https://www.servicenow.com/docs/access?context=sae-asmnt-template-category-create&family=xanadu&ft:locale=en-US): Create a template category as a container of related assessment templates. By creating an assessment template category, you can help to ensure that only authorized personnel can access and change the template.
-   **[Respond to assessments](https://www.servicenow.com/docs/access?context=sae-respond-to-asmnt&family=xanadu&ft:locale=en-US)**

Navigate through the assessments more efficiently by using a progress indicator that shows how much of the assessment is completed. The questions are paginated to help you more easily navigate the assessment. Your work is automatically saved, which eliminates the need for manual saving and helps to prevent data loss. You also have the option to reassign in-progress assessments to another user or cancel assessments that are no longer needed.

-   **[Trigger assessments](https://www.servicenow.com/docs/access?context=sae-asmnt-triggering&family=xanadu&ft:locale=en-US)**

Initiate an assessment by using the Trigger Smart Assessment flow action that is based on a published assessment template. You can assign an assessment to a designated assessor with a defined scope and deadline.

-   **[Combine multiple assessments into a single, unified submission](https://www.servicenow.com/docs/access?context=sae-asmnt-combine&family=xanadu&ft:locale=en-US)**

Combine multiple assigned assessments into a single, streamlined view. You can efficiently manage, submit, or reassign these combined assessments at one time. You can use features, like Bulk Submit or Bulk Reassign, to handle all assessments in one action.

-   **[Domain-separated Deployment](https://www.servicenow.com/docs/access?context=sae-domain-separation&family=xanadu&ft:locale=en-US)**

Domain separation in the Smart Assessment Engine is supported starting with the Xanadu release, enabling data, processes, and administrative tasks to be organized into distinct domains. Within this framework, templates are separated by a process, while assessments are separated by data, helping to ensure controlled access and visibility according to the domain.

-   **[Migrate legacy assessment metric types to Smart assessment templates](https://www.servicenow.com/docs/access?context=sae-asmnt-template-migrating&family=xanadu&ft:locale=en-US)**

Migrate existing assessment designs from the ServiceNow® Assessments and Surveys application. Your templates are automatically transferred as drafts with just one click. After you migrate the designs, you must review and publish these drafts, and confirm the results. The sets of questions in the Assessments and Surveys application are saved as metric types. When migrated, these metric types are saved as question types. Custom, Duration, Image scale, Percentage, Rankings, and Ratings question types aren’t supported for migration.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Copy an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-template-duplicate&family=yokohama&ft:locale=en-US)**

Create a copy of an existing smart assessment template, including all questions, sections, and existing configurations. This feature enables you to duplicate a fully configured assessment, so you don't need to recreate the content. You can then customize the copied template to fit new requirements or scenarios.

-   **[Filter unanswered questions](https://www.servicenow.com/docs/access?context=sae-respond-to-asmnt&family=yokohama&ft:locale=en-US)**

Filter questions in the assessments to display only unanswered questions, helping you focus on the remaining questions.

-   **[Use template designer](https://www.servicenow.com/docs/access?context=sae-template-designer&family=yokohama&ft:locale=en-US)**

Search for text within assessment sections, subsections, or questions, enabling you to locate specific information or keywords. This feature enhances navigation and enables you to find relevant content without manually scrolling through the entire assessment.

-   **[Auto-copy responses to all templates](https://www.servicenow.com/docs/access?context=combine-assessments&family=yokohama&ft:locale=en-US)**

Replicate your responses across all applicable assessments while combining assessments by enabling the auto-copy feature. It saves time and effort by copying your answers consistently without the need for manual repetition.

-   **[Automate responses](https://www.servicenow.com/docs/access?context=automate-response&family=yokohama&ft:locale=en-US)**

Set up automatic responses for questions to enable assessors to complete assessments efficiently. You can either create default responses for all question types or define a script to fetch and map the values or data to responses.

-   **[Assessment scoring and analysis](https://www.servicenow.com/docs/access?context=scoring-in-assessments&family=yokohama&ft:locale=en-US)**

Calculate meaningful scores for assessment responses at the assessment, section, or subsection levels. These scores can then be used for reporting.

-   **[Post-assessment automation](https://www.servicenow.com/docs/access?context=impact-automation&family=yokohama&ft:locale=en-US)**

Automate actions based on assessment responses. Template designers can predefine actions using a rule engine, such as updating fields, creating follow-up assessments, or generating other records.

-   **[Descriptive images in assessment questions](https://www.servicenow.com/docs/access?context=sae-q-text-create&family=yokohama&ft:locale=en-US)**

Attach descriptive images in the guidance section of the assessment questions. This means that template managers can include helpful visuals to assist respondents, making the instructions clearer and easier to understand.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Smart Assessment Engine features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Smart Assessment Engine features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Smart Assessment Engine features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Smart Assessment Engine.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install SAE by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Smart Assessment Engine by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Smart Assessment Engine we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Check your entitlements to determine whether you have access to the post-assessment automations and response automation for the SAE application.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Smart Assessment Engine we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Smart Assessment Engine, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were done to create a configurable workspace that supports WCAG 2.1 Level AA conformance.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Smart Assessment Engine we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Smart Assessment Engine we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Create your assessments by using the new template designer.
-   Improve your assessment processes with the new SAE Assessment experience.
-   Combine the multiple assessments into a single, unified submission.
-   Migrate the legacy assessment metric types to SAE templates.

 See [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Configure default responses for questions.
-   Copy an existing SAE template with all questions, sections, instructions, and configurations to save time.
-   Filter questions in an assessment to display only unanswered questions.
-   Search for text within assessment sections, subsections, and questions.
-   Auto-copy responses to all assessments when combining assessments, saving time and effort.
-   Calculate scores for assessment responses at the assessment, section, or subsection levels.
-   Set up post-assessment actions based on assessment responses.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.
-   Descriptive images are now supported in the guidance section for questions.

 See [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

