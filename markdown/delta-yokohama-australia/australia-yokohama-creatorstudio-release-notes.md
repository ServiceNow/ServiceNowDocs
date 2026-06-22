---
title: Combined Creator Studio release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Creator Studio from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-creatorstudio-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Creator Studio release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Creator Studio from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Creator Studio release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Creator Studio to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Creator Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Generate a form from text prompts using the Build with Now Assist tab](https://www.servicenow.com/docs/access?context=creator-studio-dynamic-behavior&family=yokohama&ft:locale=en-US)**

Enable users to generate forms automatically from text prompts by using the Build with Now Assist dialog box.

-   **[Auto-populate question values on a form](https://www.servicenow.com/docs/access?context=creator-studio-edit-form&family=yokohama&ft:locale=en-US)**

Help users complete forms faster with the new **Add auto-fill** option, which automatically populates answers based on answers to questions that are record choices.

-   **[Use catalog variables in playbook activities and decisions](https://www.servicenow.com/docs/access?context=creator-studio-add-automation&family=yokohama&ft:locale=en-US)**

Playbook activities and decision branches can now be triggered by answers to one or more questions on a form when you configure the conditions.

-   **[Select your development experience](https://www.servicenow.com/docs/access?context=crs-choosing-your-experience&family=yokohama&ft:locale=en-US)**

Seamlessly change between development environments using the new experience switcher. Depending on the products and versions that are installed and the role you have, you can switch between the following environments:

    -   Creator Studio to get a no-code experience
    -   ServiceNow Studio to get a platform coding experience
    -   ServiceNow IDE to get a pro-code ServiceNow experience
-   **[Test forms with the new Try it button](https://www.servicenow.com/docs/access?context=creator-studio-try-it&family=yokohama&ft:locale=en-US)**

As of Creator Studio version 27.2.2,you can test using published forms through a **Try it** button. After you submit the form, any associated playbooks run and their results appear in the generated record that opens in a new tab within Creator Studio.

-   **[Change the table for an app](https://www.servicenow.com/docs/access?context=creator-studio-admin-app-table&family=yokohama&ft:locale=en-US)**

As of Creator Studio version 27.2.2, admins can change the table where data from apps built in Creator Studio is saved.

-   **[Seamlessly open apps in ServiceNow Studio](https://www.servicenow.com/docs/access?context=view-apps-creator-studio-home-page&family=yokohama&ft:locale=en-US)**

As of Creator Studio version 27.2.2, you can open an app in ServiceNow Studio to make additional, more complicated edits by selecting an **Open with ServiceNow Studio** link from the app's tile on the Creator Studio home page.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Customizable email notifications](https://www.servicenow.com/docs/access?context=crs-admining-notifications&family=zurich&ft:locale=en-US)**

Promote consistent branding by having admins create custom email notifications and templates, which are sent when users request something from an app or the request was changed or closed. In support, several of the standard email notification activities are now in the public scope, and a new Configure email notifications item is available in Guided Setup.

-   **[New playbook activity to update record fields](https://www.servicenow.com/docs/access?context=creator-studio-add-activities-automation&family=zurich&ft:locale=en-US)**

Enable apps to change several fields automatically on the submitted record using the new Update submission playbook activity. In support, a new Configure playbook activities item is available in Guided Setup.

-   **[New question types for forms](https://www.servicenow.com/docs/access?context=creator-studio-form-elements-ref&family=zurich&ft:locale=en-US)**

Two new question types are available for forms: Duration and Attachment.

    -   Duration enables users to specify a length of time.
    -   Attachment enables users to upload an attachment as a question. The **Attachment** field differs from the **Add attachment** option for the form, because the Attachment question type can be used in dynamic behavior questions.
-   **[Granular configuration admin roles](https://www.servicenow.com/docs/access?context=roles-creator-studio&family=zurich&ft:locale=en-US)**

Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[Delete unpublished forms](https://www.servicenow.com/docs/access?context=crs-delete-form&family=zurich&ft:locale=en-US)**

You can now delete unpublished forms from Creator Studio, which completely removes the record for the form from the ServiceNow AI Platform.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Creator Studio features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Playbooks use only published forms](https://www.servicenow.com/docs/access?context=creator-studio-add-automation&family=yokohama&ft:locale=en-US)**

As of Creator Studio version 27.2.2, forms must now be published \(marked as ready\) before you can use them to create an automated playbook.

-   **[Hide the App Engine Studio template with a new system property](https://www.servicenow.com/docs/access?context=creator-studio-components-installed&family=yokohama&ft:locale=en-US)**

As of Creator Studio version 27.2.2, Creator Studio users who have both App Engine Studio \(AES\) and Creator Studio installed will no longer see the AES template when they create an app. Admins can choose to show the AES template using the new **com.glide.creator\_studio.template\_deny\_list** system property.

-   **[Form location removed from form creation](https://www.servicenow.com/docs/access?context=creator-studio-edit-form-settings&family=yokohama&ft:locale=en-US)**

Defining the catalogs and topics for a form is now accomplished by modifying the form settings rather than being done during the form creation process. If you haven't defined a location for a form, you are prompted to do so before you can mark it as ready.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Deleting questions from unpublished forms removes the record](https://www.servicenow.com/docs/access?context=creator-studio-delete-forms-questions&family=zurich&ft:locale=en-US)**

When you delete a question from an unpublished form, the record for the question is now also removed from the ServiceNow AI Platform.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Creator Studio features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Creator Studio features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Creator Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Creator Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Creator Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install Creator Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Creator Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

You must have the App Engine Enterprise license to use Creator Studio.

</td></tr><tr><td>

Zurich

</td><td>

You must have the App Engine Enterprise license to use Creator Studio.

</td></tr><tr><td>

Australia

</td><td>

Check your entitlements to determine whether you have access to Creator Studio.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Creator Studio we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Creator Studio, such as specific requirements or compliance levels.

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

-   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


 For more information, see [Dark mode in Creator Studio](https://www.servicenow.com/docs/access?context=crs-enabling-dark-mode&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

The following updates were made to support accessibility:

-   Form elements now have accurate interactive ARIA roles, enabling screen readers to identify and announce them accurately.
-   Rich text area and form elements are now accurately labeled so screen readers can announce them correctly when focused.
-   Keyboard focus now remains within the expanded template preview modal for the duration of the modal interaction.
-   The rich text frame **Long Description** now has the correct label, enabling screen readers to identify and announce it correctly.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Creator Studio we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Creator Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Create forms quickly by using Now Assist.
-   As of Creator Studio version 27.2.2, revamped navigation means you can more easily see what's in your app.
-   Populate any question on the form based on the answer given for a record choice question.
-   Use answers to form questions to trigger an activity in playbooks.
-   Switch seamlessly between no-code, mid-skill, and pro-code app development experiences for a more unified development platform with the new experience switcher.

 See [Creator Studio](https://www.servicenow.com/docs/access?context=creator-studio-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Create customized email notifications that are sent by the apps that you build.
-   Add playbooks with a new activity that automatically updates some fields on the app's generated record.
-   Augment forms with the new Duration and Attachment question types.

 See [Creator Studio](https://www.servicenow.com/docs/access?context=creator-studio-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Distinguish AI-generated apps and features at a glance using updated icons.
-   Use improved screen reader support and keyboard navigation when interacting with forms and templates using assistive technologies.

 See [Creator Studio](https://www.servicenow.com/docs/access?context=creator-studio-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

