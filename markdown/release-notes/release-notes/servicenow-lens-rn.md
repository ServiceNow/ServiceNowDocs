---
title: ServiceNow AI Lens release notes
description: With ServiceNow AI Lens, which is a ServiceNow Now Assist application, you can use generative AI to scan, extract, comprehend, and synthesize data to optimize your workflows. ServiceNow AI Lens was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-19"
reading_time_minutes: 6
keywords: [ai-now-assist]
---

# ServiceNow AI Lens release notes

With ServiceNow AI Lens, which is a ServiceNow® Now Assist application, you can use generative AI to scan, extract, comprehend, and synthesize data to optimize your workflows. ServiceNow AI Lens was enhanced and updated in the Zurich release.

## ServiceNow AI Lens highlights for the Zurich release

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Upload files, and then analyze and extract information from them.
-   Auto-map Microsoft Excel sheet headers with the columns of a ServiceNow® table.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill fields in a form.
-   Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use the Lens actions to define default instructions, trigger options, custom context, transform response logic, and post processing instructions for ServiceNow AI Lens execution.
-   Configure Lens actions to launch ServiceNow AI Lens from any part of the ServiceNow AI Platform, such as a workspace form or a portal.
-   Trigger ServiceNow AI Lens from a Virtual Agent conversation on a mobile device or in a portal.
-   View captured images that are attached to an auto-filled record using ServiceNow AI Lens.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.

See [ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=servicenow-lens-landing-page&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** ServiceNow AI Lens is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Auto-map Excel sheet column headers with ServiceNow table columns](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=zurich&pubname=zurich-intelligent-experiences&section=import-excel-sheet-data-to-custom-table&ft:locale=en-US)**

    Use ServiceNow AI Lens directly from the browser without installing the desktop application. No need to request admin permissions. Capture the web page in a browser tab wholly or partly by cropping it and letting ServiceNow AI Lens analyze the data.

-   **[Auto-map Excel sheet column headers with ServiceNow table columns](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=zurich&pubname=zurich-intelligent-experiences&section=import-excel-sheet-data-to-custom-table&ft:locale=en-US)**

    Auto-map the headers in a Microsoft Excel sheet to the columns in a ServiceNow® instance table with the Excel Mapping feature. You can change the mapping, if needed, before inserting the sheet data into the table.

-   **[Assign roles to a Lens action](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=zurich&pubname=zurich-intelligent-experiences&section=create-sn-lens-recipe&ft:locale=en-US#assign-roles-lens-action)**

    Assign roles to a Lens action so that users with those roles can access the Lens action.

-   **[Autofill reference and glide list form field types](https://www.servicenow.com/docs/access?context=field-types-supported&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Auto-fill reference and glide list form field types with the data extracted from captured images or uploaded documents.


-   **[Auto-fill the Catalog Item form in the Service Portal](https://www.servicenow.com/docs/access?context=create-record-in-the-service-portal&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal. ServiceNow AI Lens extracts data from one or more artifacts and auto-fills the relevant fields in the form.

-   **[Handle post-processing in the standalone mode](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=zurich&pubname=zurich-intelligent-experiences&section=create-sn-lens-recipe&ft:locale=en-US)**

    Handle post-processing timeout for previewing data in the standalone mode using the following new fields:

    -   **Wait for processed response**: Option to wait for ServiceNow AI Lens to display the output of post-processing on the Preview window. If turned on, it waits for the post-processing output. If turned off, it doesn't wait for post-processing output, but post-processing continues in the background.
    -   **Max wait time**: Maximum time ServiceNow AI Lens waits to display the output of post-processing. If the output doesn't appear within this duration, the session times out while the post-processing continues in the background until complete.
-   **[Use ServiceNow AI Lens in Now Mobile®](https://www.servicenow.com/docs/access?context=servicenow-lens-mobile&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

    Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill forms on your mobile device.


-   **[ServiceNow AI Lens UI enhancement](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Launch the ServiceNow AI Lens scanner window by using the context defined in the Lens actions or as a standalone application. You can preview the gathered insights or extracted data. You can also see the logged-in user and instance details.

-   **[Use Lens actions to customize Lens behavior](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Define Lens behavior depending on how ServiceNow AI Lens is triggered and what context is set. With Lens actions, you can customize how a classic form is auto-filled. You can define default instructions, trigger options, custom context, transform response logic, and post processing instructions for the ServiceNow AI Lens execution.

        For example, you can define a Lens action that is used when Lens is triggered from an instance to populate a form of a table. You can also define form fields that must be used as context.

    -   As part of your integration logic, configure a Lens action as one of the steps to invoke a ServiceNow AI Lens service from any part of the ServiceNow AI Platform, such as a workspace form or portal.
-   **[Use ServiceNow AI Lens in Virtual Agent](https://www.servicenow.com/docs/access?context=enabling-lens-for-virtual-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Trigger ServiceNow AI Lens from a Virtual Agent conversation by using the ServiceNow AI Lens topic in Virtual Agent.

-   **[Auto-attach images to a record](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=zurich&pubname=zurich-intelligent-experiences&section=create-sn-lens-recipe&ft:locale=en-US)**

    View captured images that are automatically attached to an auto-filled record using ServiceNow AI Lens. You can view the images to understand the source of the auto-filled information.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.


## UI changes

-   **[New Attach button on the home screen](https://www.servicenow.com/docs/access?context=sn-lens-standalone-app&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US#attach-files)**

    An **Attach** button has been added to the home screen of the ServiceNow AI Lens desktop app, enabling you to attach one or more files.

-   **[Upload files icon in the scanner window](https://www.servicenow.com/docs/access?context=sn-lens-standalone-app&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US#attach-files)**

    An Upload files icon has been added to the scanner window to enable you to attach one or more files.

    ![Upload icon in the scanner window.](../../product/servicenow-lens/image/lens-rn-ui-changes-others.png)

-   **[UI changes in the preview window](https://www.servicenow.com/docs/access?context=sn-lens-standalone-app&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US#attach-files)**

    The following have changed in the preview window:

    -   Attached files or captured screenshots appear as cards.
    -   The preview of a file or screenshot opens on its respective default application when you select the card.
    -   An **Upload** button has been added.

-   **[Changes in the scanner window UI](https://www.servicenow.com/docs/access?context=create-record-sn-lens&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The UI of the scanner window has been updated.

    When you open the scanner window, the toolbar is displayed outside of it. However, when you maximize the window, the toolbar moves inside.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

ServiceNow AI Lens is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using ServiceNow AI Lens, see [Configure ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=install-sn-lens&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve productivity and efficiency in your organization, deliver better self-service, display recommended actions, provide answers, and empower your users to search effectively.

-   **[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The Now Assist Admin console provides you with quick and easy access to important information needed to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including content summarization in Docs.


**Parent Topic:**[AI Experiences release notes](../analytics-intelligence-reporting/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

