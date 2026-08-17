---
title: ServiceNow AI Lens release notes
description: With ServiceNow AI Lens, which is a ServiceNow Otto application, you can use generative AI to scan, extract, comprehend, and synthesize data to optimize your workflows. ServiceNow AI Lens was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-19"
reading_time_minutes: 12
keywords: [ai-now-assist]
---

# ServiceNow AI Lens release notes

With ServiceNow AI Lens, which is a ServiceNow® Otto application, you can use generative AI to scan, extract, comprehend, and synthesize data to optimize your workflows. ServiceNow AI Lens was enhanced and updated in the Zurich release.

## ServiceNow AI Lens highlights for the Zurich release

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)

Use ServiceNow AI Lens from your browser to upload one or more files for AI Lens to analyze and auto-fill form fields — no installation required.

Updated the AI experience branding in ServiceNow AI Lens to align with ServiceNow Otto naming and visual guidelines.

[Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)

Use ServiceNow AI Lens from your browser to capture and analyze screens and auto-fill catalog item forms in Service Portal — no installation required.

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

Lens as a Service now supports auto-mapping of Excel column headers, choice values, and reference values to ServiceNow® table fields.

[Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Upload files, and then analyze and extract information from them.
-   Auto-map Microsoft Excel sheet headers with the columns of a ServiceNow® table.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill fields in a form.
-   Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Use the Lens actions to define default instructions, trigger options, custom context, transform response logic, and post processing instructions for ServiceNow AI Lens execution.
-   Configure Lens actions to launch ServiceNow AI Lens from any part of the ServiceNow AI Platform, such as a workspace form or a portal.
-   Trigger ServiceNow AI Lens from a Virtual Agent conversation on a mobile device or in a portal.
-   View captured images that are attached to an auto-filled record using ServiceNow AI Lens.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.

See [ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-landing-page.md) for more information.

**Important:** ServiceNow AI Lens is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Set your default launch preference for AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/download-sn-lens-msi.md)**

    Choose how AI Lens opens when you start a session — from your browser or the desktop application. You can update this preference at any time.

-   **[Upload files from your browser to auto-fill form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-record-sn-lens.md)**

    Use ServiceNow AI Lens in your browser to upload files for it to analyze and auto-fill form fields — no installation required. Attach files by dragging or dropping or browsing and then upload the files for AI Lens to analyze and auto-fill form fields. File upload limits apply.

-   **[Map related Excel column headers and their values to a single ServiceNow table field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-lens-action-service-api.md)**

    Use Lens as a Service to map the data from multiple related Excel column headers and values to a single ServiceNow table field. For example, if your Excel sheet has separate City, State, and Country columns, you can map all three values to a single Location field in your ServiceNow table. The service takes the values from each related column header and maps them as a combined data element to your target field, preserving the relationship between the data. Duplicate rows are automatically removed. This enhancement works with choice mapping and reference mapping.

-   **[Map Excel column headers and values to multiple ServiceNow table fields in a single operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-lens-action-service-api.md)**

    Use Lens as a Service to auto-map an Excel column header and its values from a single Excel sheet to multiple ServiceNow table fields simultaneously. For example, if your Excel sheet contains equipment-related data under headers such as Equipment Description, Manufacturer, and Model Name, AI Lens can auto-map these column headers and their values to multiple table fields at the same time. Some columns may map to one table while others map to different tables based on relevance. AI Lens, for example, can auto-map a single column header and its values to multiple table fields. The target tables are specified in your input JSON. Duplicate rows are automatically removed. This enhancement works with schema mapping.

-   **[Capture and analyze screens from your browser to auto-fill catalog item forms in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-record-in-the-service-portal.md)**

    Capture and analyze the contents of your screen directly from your browser to auto-fill catalog item form fields in Service Portal — no installation required. To specify the area of the captured screen that you want AI Lens to analyze, crop the image before submitting it for analysis.

-   **[Excel mapping as a service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-lens-action-service-api.md)**

    Use Lens as a Service to support three auto-mapping services between Excel and ServiceNow tables: auto-map Excel column headers to ServiceNow® table fields, auto-map Excel choice column values to ServiceNow choice field values, and auto-map Excel reference column values to ServiceNow® reference field values.


-   **[Capture and analyze screens from your browser to auto-fill forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-record-sn-lens.md#use-your-browser)**

    Capture and analyze the contents of your screen directly from your browser to auto-fill form fields. To specify the area of the captured screen that you want ServiceNow AI Lens to analyze, crop the image before submitting it for analysis.

-   **[Pre-configure instance URL and enable auto-login for ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-instance-url-and-auto-login.md)**

    After installing the ServiceNow AI Lens desktop application, set up your organization's ServiceNow® instance URL once so that it appears pre-filled on the login screen for all users. You can also enable automatic sign-in so that users are signed in automatically on subsequent launches without being prompted for credentials. If a user signs out or their sign-in expires, ServiceNow AI Lens prompts them to sign in again.


-   **[Auto-map Excel sheet column headers with ServiceNow table columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-actions.md)**

    Use ServiceNow AI Lens directly from the browser without installing the desktop application. No need to request admin permissions. Capture the web page in a browser tab wholly or partly by cropping it and letting ServiceNow AI Lens analyze the data.

-   **[Auto-map Excel sheet column headers with ServiceNow table columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-actions.md)**

    Auto-map the headers in a Microsoft Excel sheet to the columns in a ServiceNow® instance table with the Excel Mapping feature. You can change the mapping, if needed, before inserting the sheet data into the table.

-   **[Assign roles to a Lens action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-actions.md#assign-roles-lens-action)**

    Assign roles to a Lens action so that users with those roles can access the Lens action.

-   **[Autofill reference and glide list form field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/field-types-supported.md)**

    Auto-fill reference and glide list form field types with the data extracted from captured images or uploaded documents.


-   **[Auto-fill the Catalog Item form in the Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-record-in-the-service-portal.md)**

    Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal. ServiceNow AI Lens extracts data from one or more artifacts and auto-fills the relevant fields in the form.

-   **[Handle post-processing in the standalone mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-actions.md)**

    Handle post-processing timeout for previewing data in the standalone mode using the following new fields:

    -   **Wait for processed response**: Option to wait for ServiceNow AI Lens to display the output of post-processing on the Preview window. If turned on, it waits for the post-processing output. If turned off, it doesn't wait for post-processing output, but post-processing continues in the background.
    -   **Max wait time**: Maximum time ServiceNow AI Lens waits to display the output of post-processing. If the output doesn't appear within this duration, the session times out while the post-processing continues in the background until complete.
-   **[Use ServiceNow AI Lens in Now Mobile®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/mobile/servicenow-lens-mobile.md)**

    Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill forms on your mobile device.


-   **[ServiceNow AI Lens UI enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-explore.md)**

    Launch the ServiceNow AI Lens scanner window by using the context defined in the Lens actions or as a standalone application. You can preview the gathered insights or extracted data. You can also see the logged-in user and instance details.

-   **[Use Lens actions to customize Lens behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-actions.md)**
    -   Define Lens behavior depending on how ServiceNow AI Lens is triggered and what context is set. With Lens actions, you can customize how a classic form is auto-filled. You can define default instructions, trigger options, custom context, transform response logic, and post processing instructions for the ServiceNow AI Lens execution.

        For example, you can define a Lens action that is used when Lens is triggered from an instance to populate a form of a table. You can also define form fields that must be used as context.

    -   As part of your integration logic, configure a Lens action as one of the steps to invoke a ServiceNow AI Lens service from any part of the ServiceNow AI Platform, such as a workspace form or portal.
-   **[Use ServiceNow AI Lens in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enabling-lens-for-virtual-agent.md)**

    Trigger ServiceNow AI Lens from a Virtual Agent conversation by using the ServiceNow AI Lens topic in Virtual Agent.

-   **[Auto-attach images to a record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-actions.md)**

    View captured images that are automatically attached to an auto-filled record using ServiceNow AI Lens. You can view the images to understand the source of the auto-filled information.

-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.


## UI changes

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)

-   **[Default app on launch setting on the ServiceNow AI Lens downloads and preferences page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/download-sn-lens-msi.md)**

    The ServiceNow AI Lens Downloads page has been renamed to ServiceNow AI Lens downloads and preferences, and a Default app on launch setting has been added to the page. The setting includes the following options:

    -   **Browser \(no installation required\)**: Launches AI Lens from your browser when you start a session.
    -   **Desktop app**: Launches AI Lens desktop application when you start a session.
-   **[UI updated to reflect ServiceNow Otto branding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-lens-features.md)**

    The UI has been updated to reflect the ServiceNow Otto branding. Icons, and UI text have been updated throughout the interface to use Otto terminology and visual identity.

-   **[New Upload button and Upload file dialog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-record-sn-lens.md)**

    The ServiceNow AI Lens page, which opens in your browser when you select Create with Lens or Update with Lens button, now provides an Upload button. Selecting Upload opens the Upload file dialog, where you can add or drag files to attach the files. After attaching, you can optionally rename the files. To upload the files, select Next. After uploading, submit the files for ServiceNow AI Lens to analyze and auto-fill your form fields.


[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   **[Quick visual distinction between AI-filled form fields and manually filled fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-record-sn-lens.md)**

    ServiceNow AI Lens now uses visual gradient indicators to distinguish AI-filled form fields from manually entered data.


-   **[New screen with browser and desktop app access options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-record-sn-lens.md#use-your-browser)**

    A new ServiceNow AI Lens screen opens when you select the **Create with Lens** button on a list view or **Update with Lens** button on a form. The screen provides the following options:

    -   **Capture screen**: Captures a screen from your browser and lets ServiceNow AI Lens analyze its contents to auto-fill form fields.
    -   **Open AI Lens desktop**: Opens the ServiceNow AI Lens desktop application for the full range of capabilities, including capturing multiple screens and uploading files.
-   **[Preview screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-record-sn-lens.md#use-your-browser)**

    The new preview screen displays the screen that ServiceNow AI Lens captured before submitting for analysis. The screen provides the following options:

    -   **Crop**: Select to crop the captured screen to specify the area that you want ServiceNow AI Lens to analyze, before submitting it for analysis.
    -   **Additional instructions \(Optional\)**: Enter instructions to guide ServiceNow AI Lens in analyzing specific information from the captured screen.
    -   **Re-capture**: Select to discard the current capture and repeat the screen capture process.
    -   **Analyze**: Select to submit the captured screen for analysis and then auto-fill the form fields.

-   **[New Attach button on the home screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/sn-lens-standalone-app.md#attach-files)**

    An **Attach** button has been added to the home screen of the ServiceNow AI Lens desktop app, enabling you to attach one or more files.

-   **[Upload files icon in the scanner window](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/sn-lens-standalone-app.md#attach-files)**

    An Upload files icon has been added to the scanner window to enable you to attach one or more files.

    \[Omitted image "lens-rn-ui-changes-others.png"\] Alt text: Upload icon in the scanner window.

-   **[UI changes in the preview window](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/sn-lens-standalone-app.md#attach-files)**

    The following have changed in the preview window:

    -   Attached files or captured screenshots appear as cards.
    -   The preview of a file or screenshot opens on its respective default application when you select the card.
    -   An **Upload** button has been added.

-   **[Changes in the scanner window UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-record-sn-lens.md)**

    The UI of the scanner window has been updated.

    When you open the scanner window, the toolbar is displayed outside of it. However, when you maximize the window, the toolbar moves inside.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

ServiceNow AI Lens is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using ServiceNow AI Lens, see [Configure ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-sn-lens.md).

## Related ServiceNow applications and features

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve productivity and efficiency in your organization, deliver better self-service, display recommended actions, provide answers, and empower your users to search effectively.

-   **[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    The AI Admin Hub console provides you with quick and easy access to important information needed to set up, configure, and monitor Now Assist applications and features.

-   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including content summarization in Docs.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

