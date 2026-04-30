---
title: ServiceNow AI Lens release notes
description: With ServiceNow AI Lens, which is a ServiceNow Now Assist application, you can use generative AI to scan, extract, comprehend, and synthesize data to optimize your workflows. ServiceNow AI Lens is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-19"
reading_time_minutes: 6
---

# ServiceNow AI Lens release notes

With ServiceNow AI Lens, which is a ServiceNow® Now Assist application, you can use generative AI to scan, extract, comprehend, and synthesize data to optimize your workflows. ServiceNow AI Lens is a new application in the Yokohama release.

## ServiceNow AI Lens highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill fields in a form.
-   Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use the Lens actions to define default instructions, trigger options, custom context, transform response logic, and post processing instructions for ServiceNow AI Lens execution.
-   Configure Lens actions to launch ServiceNow AI Lens from any part of the ServiceNow AI Platform, such as a workspace form or a portal.
-   Trigger ServiceNow AI Lens from a Virtual Agent conversation on a mobile device or in a portal.
-   View captured images that are now attached to the record that is auto-filled using ServiceNow AI Lens.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Boost productivity by scanning artifacts and auto-filling information into forms instead of manually entering the information into forms.
-   Provide specific instructions to ServiceNow AI Lens on what to do with the data that it captures.
-   Get insights from multiple images so that you know what actions to do next.

See [ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=servicenow-lens-landing-page&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** ServiceNow AI Lens is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Auto-fill the Catalog Item form in the Service Portal](https://www.servicenow.com/docs/access?context=create-record-in-the-service-portal&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal. ServiceNow AI Lens extracts data from one or more artifacts and auto-fills the relevant fields in the form.

-   **[Handle post-processing in the standalone mode](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=yokohama&pubname=yokohama-intelligent-experiences&section=create-sn-lens-recipe&ft:locale=en-US)**

    The following fields have been added to handle post-processing timeout for previewing data in the standalone mode:

    -   **Wait for processed response**: Option to wait for ServiceNow AI Lens to display the output of post-processing on the Preview window. If turned on, it waits for the post-processing output. If turned off, it doesn't wait for post-processing output, but post-processing continues in the background.
    -   **Max wait time**: Maximum time ServiceNow AI Lens waits to display the output of post-processing. If the output doesn't appear within this duration, the session times out while the post-processing continues in the background until complete.
-   **[Use ServiceNow AI Lens in Now Mobile®](https://www.servicenow.com/docs/access?context=servicenow-lens-mobile&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill forms on your mobile device.


-   **[ServiceNow AI Lens UI enhancement](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use ServiceNow AI Lens to launch the scanner window by using the context defined in Lens actions or as a standalone application. You can preview the gathered insights or extracted data. You can also see the logged-in user and instance details.

-   **[Use Lens actions to customize Lens behavior](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**
    -   Define Lens behavior depending on how ServiceNow AI Lens is triggered and what context is set. With Lens actions, you can customize how a classic form is auto-filled. You can define default instructions, trigger options, custom context, transform response logic, and post processing instructions for the ServiceNow AI Lens execution.

        For example, you can define a Lens action that is used when Lens is triggered from an instance to populate a form of a table. You can also define form fields that must be used as context.

    -   As part of your integration logic, configure a Lens action as one of the steps to invoke a ServiceNow AI Lens service from any part of the ServiceNow AI Platform, such as a workspace form or portal.
-   **[Use ServiceNow AI Lens in Virtual Agent](https://www.servicenow.com/docs/access?context=enabling-lens-for-virtual-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Trigger ServiceNow AI Lens from a Virtual Agent conversation by using ServiceNow AI Lens topic in Virtual Agent.

-   **[Auto-attach images to a record](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=yokohama&pubname=yokohama-intelligent-experiences&section=create-sn-lens-recipe&ft:locale=en-US)**

    View captured images that are automatically attached to the record that is auto-filled using ServiceNow AI Lens. You can view the images to understand the source of the auto-filled information.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.


-   **[Capture data](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Get actionable insights from such visual data as images, handwritten notes and forms, emails, websites, and applications. For example, ServiceNow AI Lens can scan an email to gather data for auto-filling the fields on the Incident form.

-   **[Act on visual data](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Provide instructions to Now Assist on what to do with the captured data. For example, you can convert the extracted data into a JSON format.

-   **[Launch from ServiceNow forms](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Launch ServiceNow AI Lens from a form to fill the extracted data automatically into the form fields.

-   **[Use as a standalone application](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use ServiceNow AI Lens as a standalone application for previewing extracted data when you're connected to a ServiceNow instance.


## UI changes

-   **[Changes in the scanner window UI](https://www.servicenow.com/docs/access?context=create-record-sn-lens&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The UI of the scanner window has been changed. See the following image.![Screenshot of the Lens scanner new UI.](../../product/servicenow-lens/image/lens-scanner-new-ui.png)

    When you open the scanner window, the toolbar is displayed outside of it. However, when you maximize the window, the toolbar moves inside.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

## Activation information

ServiceNow AI Lens is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using ServiceNow AI Lens, see [Configure ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=install-sn-lens&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The Now Assist Admin console provides you with quick and easy access to the important information that you must set up, configure, and monitor in Now Assist applications and features.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including content summarization in Docs.


**Parent Topic:**[AI Experiences release notes](../analytics-intelligence-reporting/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

