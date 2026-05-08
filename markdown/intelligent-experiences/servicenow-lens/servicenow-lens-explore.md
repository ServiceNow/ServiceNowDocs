---
title: Exploring ServiceNow AI Lens
description: ServiceNow AI Lens is a ServiceNow Now Assist application that uses generative AI to scan images and screens, extract information, understand visual data, and help improve your workflows.
locale: en-US
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: concept
last_updated: "2025-03-20"
reading_time_minutes: 5
keywords: [ServiceNow Lens, ServiceNow Lens overview, ServiceNow Lens benefits]
breadcrumb: [ServiceNow AI Lens, Enable AI experiences]
---

# Exploring ServiceNow AI Lens

ServiceNow AI Lens is a ServiceNow® Now Assist application that uses generative AI to scan images and screens, extract information, understand visual data, and help improve your workflows.

## ServiceNow AI Lens overview

Get an overview of the capabilities and a few use cases of ServiceNow AI Lens.

Overview of the ServiceNow AI Lens capabilities and use cases 

The ServiceNow AI Lens application extracts and analyzes data from screens or the screenshots of documents such as a scanned handwritten note or an email that you capture or files that you upload. ServiceNow AI Lens is integrated with the ServiceNow® forms so that you can create or update forms on the ServiceNow instance by auto-filling data.

By connecting to a ServiceNow instance, you can also use ServiceNow AI Lens in a standalone mode to see a preview of the extracted data or get insights about your use cases. For more information, see [ServiceNow AI Lens features](servicenow-lens-features.md).

You can leverage Lens actions to customize the Lens behavior by providing default context, trigger options, and transform response logic for a table. When Lens is triggered to auto-fill a form on this table, it uses the configuration defined in the Lens action to auto-fill the form with the transformed LLM response. You can also define context, trigger options, and post processing instructions in a Lens action, which is used when Lens is triggered from desktop to show preview of extracted data and post process the LLM response. For more information, see [Define ServiceNow AI Lens behavior with Lens actions](servicenow-lens-actions.md#).

Extract data from documents such as an image, a scanned handwritten note, web page, or a Microsoft Word document, and autofill catalog item forms in the Service Portal. For example, autofill a new vendor onboarding form by extracting key details such as vendor name, address, contact email, and banking information from multiple artifacts, including Excel files, emails, images, and PDF documents. For more information, see [Autofill catalog item forms on Service Portal using ServiceNow AI Lens.](../task/create-record-in-the-service-portal.md)

Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from documents such as an image, a scanned handwritten note, web page, or a Microsoft Word document, and auto-fill fields in a form. For more information, see Trigger ServiceNow AI Lens from Now Mobile® and autofill forms.

Get started with ServiceNow AI Lens directly from your browser - no downloading or installation required orby downloading and installing the desktop application for Windows and macOS

## Benefits of ServiceNow AI Lens

ServiceNow AI Lens can do the following tasks automatically for you:

-   Fill in a form without having to do it manually. ServiceNow AI Lens can scan and extract the visual data to auto-fill in your forms. For example, it can scan the invoice receipt to auto-fill the fields on the expense submission form.
-   Scan and identify the information from handwritten notes or images. For example, ServiceNow AI Lens can scan a sequence diagram to generate a script.
-   Search for specific information from images. For example, ServiceNow AI Lens can look for a specific clause in a scanned legal contract.
-   Process the screenshots of multiple images or files at once. For example, ServiceNow AI Lens can extract the data from multiple screenshots of an error or a Microsoft Excel file to get insights on the data at one time.

## ServiceNow AI Lens skill

Now Assist for Platform includes the AI-powered ServiceNow AI Lens skill to read, understand, respond, and act on visual data such as hand-written texts, images, and websites and take powerful actions to boost productivity.

Admins can enable the ServiceNow AI Lens skill in the Now Assist Admin console. Once enabled, users can perform the following actions:

-   Create or update ServiceNow records by auto-filling forms using the extracted data.
-   Preview the extracted data.
-   Provide instructions to extract data in a specific way or to get a specific output.
-   Capture multiple screenshots to gather insights from multiple images.

To view the procedure to enable the ServiceNow AI Lens skill, see [Activate the ServiceNow AI Lens skill](../task/activate-lens-skill.md).

The ServiceNow AI Lens application requires a Workflow Data Fabric \(previously known as Automation Engine\) license and a Now Assist license.

## Available LLMs

You can use Azure OpenAI, Google Gemini, or Anthropic Claude on AWS as the AI model provider for ServiceNow AI Lens skill. You can set skill-level preferences in the [Now Assist Admin console](../../../administer/now-assist-admin/task/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform](../../../administer/general/concept/exploring-large-language-models.md).

## What to explore next

To learn how to configure and use ServiceNow AI Lens, see:

-   [Configure ServiceNow AI Lens](../task/install-sn-lens.md)
-   [Using ServiceNow AI Lens](../task/servicenow-lens-use.md)
-   [ServiceNow AI Lens reference](../reference/servicenow-lens-reference.md)

