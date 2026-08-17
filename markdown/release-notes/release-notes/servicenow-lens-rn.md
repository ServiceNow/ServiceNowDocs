---
title: ServiceNow AI Lens release notes
description: With ServiceNow AI Lens, which is a ServiceNow Otto application, you can use generative AI to scan, extract, comprehend, and synthesize data to optimize your workflows. ServiceNow AI Lens was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-08-19"
reading_time_minutes: 6
keywords: [ai-now-assist]
---

# ServiceNow AI Lens release notes

With ServiceNow AI Lens, which is a ServiceNow® Otto application, you can use generative AI to scan, extract, comprehend, and synthesize data to optimize your workflows. ServiceNow AI Lens was enhanced and updated in the Australia release.

## ServiceNow AI Lens highlights for the Australia release

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

Use ServiceNow AI Lens from your browser to upload one or more files for AI Lens to analyze and auto-fill form fields — no installation required.

Updated the AI experience branding in ServiceNow AI Lens to align with ServiceNow Otto naming and visual guidelines.

[Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md)

Use ServiceNow AI Lens from your browser to capture and analyze screens and auto-fill catalog item forms in Service Portal — no installation required.

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

Lens as a Service now supports auto-mapping of Excel column headers, choice values, and reference values to ServiceNow table fields.

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

Get started with ServiceNow AI Lens by using it directly from the browser. No downloading or installation required.

See [ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens-landing-page.md) for more information.

**Important:** ServiceNow AI Lens is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **Set your default launch preference for AI Lens**

    Choose how AI Lens opens when you start a session — from your browser or the desktop application. You can update this preference at any time.


-   **Upload files from your browser to auto-fill form fields**

    Use AI Lens in your browser to upload files for it to analyze and auto-fill form fields — no installation required. Attach files by dragging or dropping or browsing and then upload the files for AI Lens to analyze and auto-fill form fields. File upload limits apply.


-   **Map related Excel column headers and their values to a single ServiceNow table field**

    Use Lens as a Service to map the data from multiple related Excel column headers and values to a single ServiceNow table field. For example, if your Excel sheet has separate City, State, and Country columns, you can map all three values to a single Location field in your ServiceNow table. The service takes the values from each related column header and maps them as a combined data element to your target field, preserving the relationship between the data. Duplicate rows are automatically removed. This enhancement works with choice mapping and reference mapping.


-   **Map Excel column headers and values to multiple ServiceNow table fields in a single operation**

    Use Lens as a Service to auto-map an Excel column header and its values from a single Excel sheet to multiple ServiceNow table fields simultaneously. For example, if your Excel sheet contains equipment-related data under headers such as Equipment Description, Manufacturer, and Model Name, AI Lens can auto-map these column headers and their values to multiple table fields at the same time. Some columns may map to one table while others map to different tables based on relevance. AI Lens, for example, can auto-map a single column header and its values to multiple table fields. The target tables are specified in your input JSON. Duplicate rows are automatically removed. This enhancement works with schema mapping.


-   **[Capture and analyze screens from your browser to auto-fill catalog item forms in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-record-in-the-service-portal.md)**

    Capture and analyze the contents of your screen directly from your browser to auto-fill catalog item form fields in Service Portal — no installation required. To specify the area of the captured screen that you want AI Lens to analyze, crop the image before submitting it for analysis.


-   **[Excel mapping as a service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-lens-action-service-api.md)**

    Use Lens as a Service to support three auto-mapping services between Excel and ServiceNow tables. Auto-map Excel column headers to ServiceNow table fields. Auto-map Excel choice column values to ServiceNow choice field values. Auto-map Excel reference column values to ServiceNow reference field values.


-   **[Capture and analyze screens from your browser to auto-fill forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-record-sn-lens.md#use-your-browser)**

    Capture and analyze the contents of your screen directly from your browser to auto-fill form fields. To specify the area of the captured screen that you want ServiceNow AI Lens to analyze, crop the image before submitting it for analysis.

-   **[Pre-configure instance URL and enable auto-login for ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-instance-url-and-auto-login.md)**

    After installing the ServiceNow AI Lens desktop application, set up your organization's ServiceNow® instance URL once so that it appears pre-filled on the login screen for all users. You can also enable automatic sign-in so that users are signed in automatically on subsequent launches without being prompted for credentials. If a user signs out or their sign-in expires, ServiceNow AI Lens prompts them to sign in again.


## UI changes

-   **Default app on launch setting on the ServiceNow AI Lens downloads and preferences page**

    The ServiceNow AI Lens Downloads page has been renamed to ServiceNow AI Lens downloads and preferences, and a Default app on launch setting has been added to the page. The setting includes the following options:

    -   Browser \(no installation required\): Launches AI Lens from your browser when you start a session.
    -   Desktop app: Launches AI Lens desktop application when you start a session.
-   **UI updated to reflect ServiceNow Otto branding**

    The UI has been updated to reflect the ServiceNow Otto branding. Icons, and UI text have been updated throughout the interface to use Otto terminology and visual identity.

-   **New Upload button and Upload file dialog**

    The AI Lens page, which opens in your browser when you select Create with Lens or Update with Lens button, now provides an Upload button. Selecting Upload opens the Upload file dialog, where you can add or drag to upload files. After attaching, you can optionally rename the files. To upload the files, select Next. After uploading, submit the files for ServiceNow AI Lens to analyze and auto-fill your form fields.


-   **[Quick visual distinction between AI-filled form fields and manually filled fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-record-sn-lens.md)**

    ServiceNow® AI Lens now uses visual gradient indicators to distinguish AI-filled form fields from manually entered data.


-   **[New screen with browser and desktop app access options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-record-sn-lens.md#use-your-browser)**

    A new ServiceNow AI Lens screen opens when you select the **Create with Lens** button on a list view or **Update with Lens** button on a form. The screen provides the following options:

    -   **Capture screen**: Captures a screen from your browser and lets ServiceNow AI Lens analyze its contents to auto-fill form fields.
    -   **Open AI Lens desktop**: Opens the ServiceNow AI Lens desktop application for the full range of capabilities, including capturing multiple screens and uploading files.
-   **[Preview screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-record-sn-lens.md#use-your-browser)**

    The new preview screen displays the screen that ServiceNow AI Lens captured before submitting for analysis. The screen provides the following options:

    -   **Crop**: Select to crop the captured screen to specify the area that you want ServiceNow AI Lens to analyze, before submitting it for analysis.
    -   **Additional instructions \(Optional\)**: Enter instructions to guide ServiceNow AI Lens in analyzing specific information from the captured screen.
    -   **Re-capture**: Select to discard the current capture and repeat the screen capture process.
    -   **Analyze**: Select to submit the captured screen for analysis and then auto-fill the form fields.

## Changed in this release

No changes in this release.

## Activation information

ServiceNow AI Lens is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using ServiceNow AI Lens, see [Configure ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-sn-lens.md).

## Related ServiceNow applications and features

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve productivity and efficiency in your organization, deliver better self-service, display recommended actions, provide answers, and empower your users to search effectively.

-   **[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)**

    The AI Admin Hub console provides you with quick and easy access to important information needed to set up, configure, and monitor Now Assist applications and features.

-   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills.md)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including content summarization in Docs.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/intelligent-experiences-rn-landing.md)

