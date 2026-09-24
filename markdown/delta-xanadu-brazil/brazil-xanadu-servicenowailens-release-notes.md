---
title: Combined ServiceNow AI Lens release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for ServiceNow AI Lens from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-servicenowailens-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined ServiceNow AI Lens release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for ServiceNow AI Lens from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow AI Lens release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow AI Lens to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for ServiceNow AI Lens.

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

-   **[Auto-fill the Catalog Item form in the Service Portal](https://www.servicenow.com/docs/access?context=create-record-in-the-service-portal&family=yokohama&ft:locale=en-US)**

Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal. ServiceNow AI Lens extracts data from one or more artifacts and auto-fills the relevant fields in the form.

-   **[Handle post-processing in the standalone mode](https://www.servicenow.com/docs/access?context=create-sn-lens-recipe&family=yokohama&ft:locale=en-US)**

The following fields have been added to handle post-processing timeout for previewing data in the standalone mode:

    -   **Wait for processed response**: Option to wait for ServiceNow AI Lens to display the output of post-processing on the Preview window. If turned on, it waits for the post-processing output. If turned off, it doesn't wait for post-processing output, but post-processing continues in the background.
    -   **Max wait time**: Maximum time ServiceNow AI Lens waits to display the output of post-processing. If the output doesn't appear within this duration, the session times out while the post-processing continues in the background until complete.
-   **[Use ServiceNow AI Lens in Now Mobile®](https://www.servicenow.com/docs/access?context=servicenow-lens-mobile&family=yokohama&ft:locale=en-US)**

Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill forms on your mobile device.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Capture and analyze screens from your browser to auto-fill forms](https://www.servicenow.com/docs/access?context=create-record-sn-lens&family=zurich&ft:locale=en-US)**

Capture and analyze the contents of your screen directly from your browser to auto-fill form fields. To specify the area of the captured screen that you want ServiceNow AI Lens to analyze, crop the image before submitting it for analysis.

-   **[Pre-configure instance URL and enable auto-login for ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=configure-instance-url-and-auto-login&family=zurich&ft:locale=en-US)**

After installing the ServiceNow AI Lens desktop application, set up your organization's ServiceNow® instance URL once so that it appears pre-filled on the login screen for all users. You can also enable automatic sign-in so that users are signed in automatically on subsequent launches without being prompted for credentials. If a user signs out or their sign-in expires, ServiceNow AI Lens prompts them to sign in again.


</td></tr><tr><td>

Australia

</td><td>

-   **[Set your default launch preference for AI Lens](https://www.servicenow.com/docs/access?context=download-sn-lens-msi&family=australia&ft:locale=en-US)**

Choose how AI Lens opens when you start a session — from your browser or the desktop application. You can update this preference at any time.


 -   **[Upload files from your browser to auto-fill form fields](https://www.servicenow.com/docs/access?context=create-record-sn-lens&family=australia&ft:locale=en-US)**

Use AI Lens in your browser to upload files for it to analyze and auto-fill form fields — no installation required. Attach files by dragging or dropping or browsing and then upload the files for AI Lens to analyze and auto-fill form fields. File upload limits apply.


 -   **[Map related Excel column headers and their values to a single ServiceNow table field](https://www.servicenow.com/docs/access?context=ai-lens-action-service-api&family=australia&ft:locale=en-US)**

Use Lens as a Service to map the data from multiple related Excel column headers and values to a single ServiceNow table field. For example, if your Excel sheet has separate City, State, and Country columns, you can map all three values to a single Location field in your ServiceNow table. The service takes the values from each related column header and maps them as a combined data element to your target field, preserving the relationship between the data. Duplicate rows are automatically removed. This enhancement works with choice mapping and reference mapping.


 -   **[Map Excel column headers and values to multiple ServiceNow table fields in a single operation](https://www.servicenow.com/docs/access?context=ai-lens-action-service-api&family=australia&ft:locale=en-US)**

Use Lens as a Service to auto-map an Excel column header and its values from a single Excel sheet to multiple ServiceNow table fields simultaneously. For example, if your Excel sheet contains equipment-related data under headers such as Equipment Description, Manufacturer, and Model Name, AI Lens can auto-map these column headers and their values to multiple table fields at the same time. Some columns may map to one table while others map to different tables based on relevance. AI Lens, for example, can auto-map a single column header and its values to multiple table fields. The target tables are specified in your input JSON. Duplicate rows are automatically removed. This enhancement works with schema mapping.


 -   **[Capture and analyze screens from your browser to auto-fill catalog item forms in Service Portal](https://www.servicenow.com/docs/access?context=create-record-in-the-service-portal&family=australia&ft:locale=en-US)**

Capture and analyze the contents of your screen directly from your browser to auto-fill catalog item form fields in Service Portal — no installation required. To specify the area of the captured screen that you want AI Lens to analyze, crop the image before submitting it for analysis.


 -   **[Excel mapping as a service](https://www.servicenow.com/docs/access?context=ailensactionservice-invokelens&family=australia&ft:locale=en-US)**

Use Lens as a Service to support three auto-mapping services between Excel and ServiceNow tables. Auto-map Excel column headers to ServiceNow table fields. Auto-map Excel choice column values to ServiceNow choice field values. Auto-map Excel reference column values to ServiceNow reference field values.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing ServiceNow AI Lens features.

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

-   **[New screen with browser and desktop app access options](https://www.servicenow.com/docs/access?context=create-record-sn-lens&family=zurich&ft:locale=en-US)**

A new ServiceNow AI Lens screen opens when you select the **Create with Lens** button on a list view or **Update with Lens** button on a form. The screen provides the following options:

    -   **Capture screen**: Captures a screen from your browser and lets ServiceNow AI Lens analyze its contents to auto-fill form fields.
    -   **Open AI Lens desktop**: Opens the ServiceNow AI Lens desktop application for the full range of capabilities, including capturing multiple screens and uploading files.
-   **[Preview screen](https://www.servicenow.com/docs/access?context=create-record-sn-lens&family=zurich&ft:locale=en-US)**

The new preview screen displays the screen that ServiceNow AI Lens captured before submitting for analysis. The screen provides the following options:

    -   **Crop**: Select to crop the captured screen to specify the area that you want ServiceNow AI Lens to analyze, before submitting it for analysis.
    -   **Additional instructions \(Optional\)**: Enter instructions to guide ServiceNow AI Lens in analyzing specific information from the captured screen.
    -   **Re-capture**: Select to discard the current capture and repeat the screen capture process.
    -   **Analyze**: Select to submit the captured screen for analysis and then auto-fill the form fields.

</td></tr><tr><td>

Australia

</td><td>

No changes in this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some ServiceNow AI Lens features or functionality were removed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some ServiceNow AI Lens features or functionality were deprecated.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow AI Lens we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

