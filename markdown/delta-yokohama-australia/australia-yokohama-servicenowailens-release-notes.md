---
title: Combined ServiceNow AI Lens release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for ServiceNow AI Lens from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-servicenowailens-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined ServiceNow AI Lens release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for ServiceNow AI Lens from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow AI Lens release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow AI Lens to Australia

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

Between your current release family and Australia, new features were introduced for ServiceNow AI Lens.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[ServiceNow AI Lens UI enhancement](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&family=yokohama&ft:locale=en-US)**

Use ServiceNow AI Lens to launch the scanner window by using the context defined in Lens actions or as a standalone application. You can preview the gathered insights or extracted data. You can also see the logged-in user and instance details.

-   **[Use Lens actions to customize Lens behavior](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&family=yokohama&ft:locale=en-US)**
    -   Define Lens behavior depending on how ServiceNow AI Lens is triggered and what context is set. With Lens actions, you can customize how a classic form is auto-filled. You can define default instructions, trigger options, custom context, transform response logic, and post processing instructions for the ServiceNow AI Lens execution.

For example, you can define a Lens action that is used when Lens is triggered from an instance to populate a form of a table. You can also define form fields that must be used as context.

    -   As part of your integration logic, configure a Lens action as one of the steps to invoke a ServiceNow AI Lens service from any part of the ServiceNow AI Platform, such as a workspace form or portal.
-   **[Use ServiceNow AI Lens in Virtual Agent](https://www.servicenow.com/docs/access?context=enabling-lens-for-virtual-agent&family=yokohama&ft:locale=en-US)**

Trigger ServiceNow AI Lens from a Virtual Agent conversation by using ServiceNow AI Lens topic in Virtual Agent.

-   **[Auto-attach images to a record](https://www.servicenow.com/docs/access?context=create-sn-lens-recipe&family=yokohama&ft:locale=en-US)**

View captured images that are automatically attached to the record that is auto-filled using ServiceNow AI Lens. You can view the images to understand the source of the auto-filled information.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Auto-map Excel sheet column headers with ServiceNow table columns](https://www.servicenow.com/docs/access?context=import-excel-sheet-data-to-custom-table&family=zurich&ft:locale=en-US)**

Use ServiceNow AI Lens directly from the browser without installing the desktop application. No need to request admin permissions. Capture the web page in a browser tab wholly or partly by cropping it and letting ServiceNow AI Lens analyze the data.

-   **[Auto-map Excel sheet column headers with ServiceNow table columns](https://www.servicenow.com/docs/access?context=import-excel-sheet-data-to-custom-table&family=zurich&ft:locale=en-US)**

Auto-map the headers in a Microsoft Excel sheet to the columns in a ServiceNow® instance table with the Excel Mapping feature. You can change the mapping, if needed, before inserting the sheet data into the table.

-   **[Assign roles to a Lens action](https://www.servicenow.com/docs/access?context=create-sn-lens-recipe&family=zurich&ft:locale=en-US)**

Assign roles to a Lens action so that users with those roles can access the Lens action.

-   **[Autofill reference and glide list form field types](https://www.servicenow.com/docs/access?context=field-types-supported&family=zurich&ft:locale=en-US)**

Auto-fill reference and glide list form field types with the data extracted from captured images or uploaded documents.


</td></tr><tr><td>

Australia

</td><td>

-   **[Capture and analyze screens from your browser to auto-fill forms](https://www.servicenow.com/docs/access?context=create-record-sn-lens&family=australia&ft:locale=en-US)**

Capture and analyze the contents of your screen directly from your browser to auto-fill form fields. To specify the area of the captured screen that you want ServiceNow AI Lens to analyze, crop the image before submitting it for analysis.

-   **[Pre-configure instance URL and enable auto-login for ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=configure-instance-url-and-auto-login&family=australia&ft:locale=en-US)**

After installing the ServiceNow AI Lens desktop application, set up your organization's ServiceNow® instance URL once so that it appears pre-filled on the login screen for all users. You can also enable automatic sign-in so that users are signed in automatically on subsequent launches without being prompted for credentials. If a user signs out or their sign-in expires, ServiceNow AI Lens prompts them to sign in again.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow AI Lens features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Changes in the scanner window UI](https://www.servicenow.com/docs/access?context=create-record-sn-lens&family=yokohama&ft:locale=en-US)**

The UI of the scanner window has been changed. See the following image.\[Omitted image "image.lens-scanner-new-ui"\] Alt text: Screenshot of the Lens scanner new UI.

When you open the scanner window, the toolbar is displayed outside of it. However, when you maximize the window, the toolbar moves inside.


 -   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Default app on launch setting on the ServiceNow AI Lens downloads and preferences page](https://www.servicenow.com/docs/access?context=download-sn-lens-msi&family=zurich&ft:locale=en-US)**

The ServiceNow AI Lens Downloads page has been renamed to ServiceNow AI Lens downloads and preferences, and a Default app on launch setting has been added to the page. The setting includes the following options:

    -   **Browser \(no installation required\)**: Launches AI Lens from your browser when you start a session.
    -   **Desktop app**: Launches AI Lens desktop application when you start a session.
-   **[UI updated to reflect ServiceNow Otto branding](https://www.servicenow.com/docs/access?context=servicenow-lens-features&family=zurich&ft:locale=en-US)**

The UI has been updated to reflect the ServiceNow Otto branding. Icons, and UI text have been updated throughout the interface to use Otto terminology and visual identity.

-   **[New Upload button and Upload file dialog](https://www.servicenow.com/docs/access?context=create-record-sn-lens&family=zurich&ft:locale=en-US)**

The ServiceNow AI Lens page, which opens in your browser when you select Create with Lens or Update with Lens button, now provides an Upload button. Selecting Upload opens the Upload file dialog, where you can add or drag files to attach the files. After attaching, you can optionally rename the files. To upload the files, select Next. After uploading, submit the files for ServiceNow AI Lens to analyze and auto-fill your form fields.


</td></tr><tr><td>

Australia

</td><td>

-   **[New screen with browser and desktop app access options](https://www.servicenow.com/docs/access?context=create-record-sn-lens&family=australia&ft:locale=en-US)**

A new ServiceNow AI Lens screen opens when you select the **Create with Lens** button on a list view or **Update with Lens** button on a form. The screen provides the following options:

    -   **Capture screen**: Captures a screen from your browser and lets ServiceNow AI Lens analyze its contents to auto-fill form fields.
    -   **Open AI Lens desktop**: Opens the ServiceNow AI Lens desktop application for the full range of capabilities, including capturing multiple screens and uploading files.
-   **[Preview screen](https://www.servicenow.com/docs/access?context=create-record-sn-lens&family=australia&ft:locale=en-US)**

The new preview screen displays the screen that ServiceNow AI Lens captured before submitting for analysis. The screen provides the following options:

    -   **Crop**: Select to crop the captured screen to specify the area that you want ServiceNow AI Lens to analyze, before submitting it for analysis.
    -   **Additional instructions \(Optional\)**: Enter instructions to guide ServiceNow AI Lens in analyzing specific information from the captured screen.
    -   **Re-capture**: Select to discard the current capture and repeat the screen capture process.
    -   **Analyze**: Select to submit the captured screen for analysis and then auto-fill the form fields.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow AI Lens features or functionality were removed.

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

Between your current release family and Australia, some ServiceNow AI Lens features or functionality were deprecated.

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

Review information on how to activate ServiceNow AI Lens.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Activation information**

ServiceNow AI Lens is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using ServiceNow AI Lens, see [Configure](https://www.servicenow.com/docs/access?context=install-sn-lens&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

ServiceNow AI Lens is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using ServiceNow AI Lens, see [Configure](https://www.servicenow.com/docs/access?context=install-sn-lens&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

ServiceNow AI Lens is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using ServiceNow AI Lens, see [Configure](https://www.servicenow.com/docs/access?context=install-sn-lens&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow AI Lens we have noted them here.

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
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow AI Lens we have noted them here.

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

Review details on accessibility information for ServiceNow AI Lens, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for ServiceNow AI Lens we have noted them here.

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

If there are specific highlight considerations for ServiceNow AI Lens we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill fields in a form.
-   Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal.

 [Yokohama Patch 6](https://www.servicenow.com/docs/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Use the Lens actions to define default instructions, trigger options, custom context, transform response logic, and post processing instructions for ServiceNow AI Lens execution.
-   Configure Lens actions to launch ServiceNow AI Lens from any part of the ServiceNow AI Platform, such as a workspace form or a portal.
-   Trigger ServiceNow AI Lens from a Virtual Agent conversation on a mobile device or in a portal.
-   View captured images that are now attached to the record that is auto-filled using ServiceNow AI Lens.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.

 [Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   Boost productivity by scanning artifacts and auto-filling information into forms instead of manually entering the information into forms.
-   Provide specific instructions to ServiceNow AI Lens on what to do with the data that it captures.
-   Get insights from multiple images so that you know what actions to do next.

 See [ServiceNow Lens](https://www.servicenow.com/docs/access?context=servicenow-lens-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

 Use ServiceNow AI Lens from your browser to upload one or more files for AI Lens to analyze and auto-fill form fields — no installation required.

 Updated the AI experience branding in ServiceNow AI Lens to align with ServiceNow Otto naming and visual guidelines.

 [Zurich Patch 11](https://www.servicenow.com/docs/access?context=zurich-patch-11&family=zurich&ft:locale=en-US)

 Use ServiceNow AI Lens from your browser to capture and analyze screens and auto-fill catalog item forms in Service Portal — no installation required.

 [Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US)

 Lens as a Service now supports auto-mapping of Excel column headers, choice values, and reference values to ServiceNow® table fields.

 [Zurich Patch 9](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US)

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Upload files, and then analyze and extract information from them.
-   Auto-map Microsoft Excel sheet headers with the columns of a ServiceNow® table.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill fields in a form.
-   Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Use the Lens actions to define default instructions, trigger options, custom context, transform response logic, and post processing instructions for ServiceNow AI Lens execution.
-   Configure Lens actions to launch ServiceNow AI Lens from any part of the ServiceNow AI Platform, such as a workspace form or a portal.
-   Trigger ServiceNow AI Lens from a Virtual Agent conversation on a mobile device or in a portal.
-   View captured images that are attached to an auto-filled record using ServiceNow AI Lens.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.

 See [ServiceNow Lens](https://www.servicenow.com/docs/access?context=servicenow-lens-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

 Use ServiceNow AI Lens from your browser to upload one or more files for AI Lens to analyze and auto-fill form fields — no installation required.

 Updated the AI experience branding in ServiceNow AI Lens to align with ServiceNow Otto naming and visual guidelines.

 [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

 Use ServiceNow AI Lens from your browser to capture and analyze screens and auto-fill catalog item forms in Service Portal — no installation required.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

 Lens as a Service now supports auto-mapping of Excel column headers, choice values, and reference values to ServiceNow table fields.

 [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

 Get started with ServiceNow AI Lens by using it directly from the browser. No downloading or installation required.

 See [ServiceNow Lens](https://www.servicenow.com/docs/access?context=servicenow-lens-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

