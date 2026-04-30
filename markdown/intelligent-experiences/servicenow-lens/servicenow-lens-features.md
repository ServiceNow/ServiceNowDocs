---
title: ServiceNow AI Lens features
description: Learn about the various ServiceNow AI Lens features to help you get started with analyzing and gathering insights from the visual data.
locale: en-US
release: yokohama
product: ServiceNow Lens
classification: servicenow-lens
topic_type: concept
last_updated: "2025-08-21"
reading_time_minutes: 5
breadcrumb: [Explore, ServiceNow AI Lens, Enable AI experiences]
---

# ServiceNow AI Lens features

Learn about the various ServiceNow AI Lens features to help you get started with analyzing and gathering insights from the visual data.

ServiceNow AI Lens offers the following features:

-   **Capture data**

    Scan and get actionable insights from visual data such as images, emails, handwritten forms and notes, websites, and applications.

    For example, ServiceNow AI Lens can scan an email to gather data for auto-filling the fields on the Incident form.

    ![Lens scanner window captures incident details from email.](../image/lens-scanner-incident-capture.png)

-   **Provide additional instructions**

    Select the Instructions \(![Instructions icon](../image/lens-instructions-icon.png)\) icon and enter additional instructions, if required.

    ![Field to provide additional instructions.](../image/lens-scanner-additional-instructions.png)

-   **Capture multiple screenshots**

    Capture multiple screenshots to analyze and gather data from various images.

    For example, ServiceNow AI Lens can scan multiple bills so that you can submit a consolidated invoice report.

    ![Number of screenshots captured shown.](../image/lens-scanner-multiple-scrnshts-capturd.png)![Lens available for accepting and analyzing the captured data.](../image/lens-scanner-analyze-multiple-scrns.png)

-   **Act on visual data**

    Provide additional instructions to Now Assist on what to do with the captured data.

    For example, ServiceNow AI Lens can provide instructions, such as the extracted name, user email ID, and location from the resumes, and then present the data in a JSON format.

    ![Instruction given to Lens to act on the visual data that it captured.](../image/lens-scanner-instructions.png)

-   **Launch from ServiceNow instance**

    Launch ServiceNow AI Lens from a ServiceNow instance to fill the extracted data automatically into the form fields while you’re creating or updating records.

    ![Create with Lens button on the ServiceNow instance.](../image/luanch-from-sn-instance.png)

    ![Update with Lens button on the ServiceNow instance.](../image/update-with-lens.png)

-   **Use Lens actions to customize Lens behavior**

    You can use Lens actions that define Lens behavior depending on how ServiceNow AI Lens is triggered and what context is set. You can define default instructions, trigger options, custom context, transform response logic, and post processing instructions for the Lens execution. With Lens actions, you can customize how a classic form auto-filled using ServiceNow AI Lens or what data must be extracted for preview and post process the LLM response. For more information, see [Customize ServiceNow AI Lens behavior by creating a Lens action](servicenow-lens-actions.md#).

    For example, you can define a Lens action that is used when Lens is triggered from an instance to populate a form of a particular table. You can also define form fields that must be populated.

    ![ServiceNow AI Lens home page displaying Lens actions.](../image/lens-action-overview.png)

-   **ServiceNow AI Lens in Virtual Agent**

    Trigger ServiceNow AI Lens from a Virtual Agent conversation by using ServiceNow AI Lens topic in Virtual Agent. For more information, see [Enabling ServiceNow AI Lens in Virtual Agent](enabling-lens-for-virtual-agent.md#) and [Extract and analyze data using ServiceNow AI Lens from Virtual Agent](../task/trigger-lens-from-va.md).

    ![ServiceNow AI Lens service in a Virtual Agent conversation on a mobile device.](../image/sn-lens-va-mobile.png)

-   **Use as a back-end service**

    As part of your integration logic, configure a Lens action as one of the steps to invoke a ServiceNow AI Lens service from any part of the ServiceNow AI Platform, such as a workspace form or a portal.

    For your own use cases, you can leverage Lens actions for using Lens as a service in the following ways:

    -   Client service: Launch the Lens client to scan and analyze images. For example, you can configure a UI action on a workspace form or a service portal to launch the Lens client. For more information, see [KB2492775](https://support.servicenow.com/kb?sys_kb_id=d5a3f9a693b3aa18d9743f986cba1094&id=kb_article_view).
    -   Server service: Use Lens as a service to analyze the provided images without launching the Lens client. For example, you can call Lens service from a Script Include or flow action to get the LLM response after analyzing the visual data. For more information, see [Script include - AILensActionService](ai-lens-action-service-api.md#).
-   **Attach images to a record**

    View the captured images attached to the record that is auto-filled using ServiceNow AI Lens. You can later refer the attached images to understand the source of the record data. For more information, see [Customize ServiceNow AI Lens behavior by creating a Lens action](servicenow-lens-actions.md#).

-   **Use as a standalone application**

    Use ServiceNow AI Lens as a standalone application for previewing extracted data or getting insights. You must connect to a ServiceNow instance before you start using ServiceNow AI Lens. For more information, see [Extract and analyze your data by using ServiceNow AI Lens in the standalone mode](../task/sn-lens-standalone-app.md).

    ![ServiceNow AI Lens login screen as a standalone application.](../image/standalone-lens.png)

-   **Autofill form fields in the Now Mobile® application**

    Trigger ServiceNow AI Lens from Now Mobile® application to extract data from artifacts and autofill fields in a form on the Now Mobile® application.. For more information on creating or updating records in the Now Mobile® application, see [ServiceNow AI Lens for mobile](https://www.servicenow.com/docs/access?context=servicenow-lens-mobile&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US).You can add a ServiceNow AI Lens button to input form screens to allow users to quickly extract data from attachments and complete forms faster. For more information, see [Configure a Lens launcher button](https://www.servicenow.com/docs/access?context=configure-lens-launcher-button&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US).

-   **Autofill Catalog Item forms in Service Portal**

    Autofill Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal. ServiceNow AI Lens extracts data from one or more artifacts and auto fills the relevant fields in the form.. For more information on using ServiceNow AI Lens in the Service Portal, see [Autofill catalog item form in the Service Portal](../task/create-record-in-the-service-portal.md).


