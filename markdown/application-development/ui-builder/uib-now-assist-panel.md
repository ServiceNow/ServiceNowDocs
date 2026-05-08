---
title: How to use the Now Assist panel in UI Builder
description: Use the Now Assist panel in UI Builder to request guidance, streamline page building, and better understand the content on your pages.Ask questions and get quick answers without leaving UI Builder.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, Now Assist panel, UI Builder, Now Assist, Now Assist panel, UI Builder]
breadcrumb: [Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# How to use the Now Assist panel in UI Builder

Use the Now Assist panel in UI Builder to request guidance, streamline page building, and better understand the content on your pages.

## Now Assist for UI Builder overview

Now Assist for UI Builder is a powerful tool that can be used to enhance the way you build experiences in UI Builder. Whether you need help configuring a page, adding components or data, or uncovering insights form a page, Now Assist for UI Builder can help you design and deliver the pages you want.

Now Assist for UI Builder enables you to leverage the generative and agentic AI capabilities of the ServiceNow AI Platform. You can configure the Now Assist panel to be accessible from any page within UI Builder.

![Request to build a basic record page](../image/now-assist-page-build-demo.png "Request to build a basic record page")

**Note:** You must install the Now Assist for Creator plugin in the Now Assist Admin console to use the Now Assist panel. For more information, see Now Assist Admin console

For more information on the Now Assist panel, see Now Assist panel.

## What to ask for Conversational Help

Conversational Help uses generative AI to provide instant support from anywhere in your experience, enabling you to ask questions and get quick answers without disrupting your current activity. Conversational Help answers questions based on product documentation, but cannot provide guidance specific to what you've configured in your instance.

Ask questions in the Now Assist panel to discover new features and learn how to complete specific tasks. For example:

-   `Can I configure side navigation?`
-   `How do I bind dynamic data to a repeater?`
-   `Where can I find best practices and design considerations when using Next Experience Components on my page?`
-   `How do I create a reusable page template?`

## What to ask for Page Building help

Now Assist Page Building uses generative AI to add content such as components, data bindings, or events, enabling you to quickly build pages using a simple text prompt. Page building is based on internal recipes that ensure content added to a page will function properly.

-   `Can you create a record page?`
-   `Bind the heading to the current user's name.`
-   `Create a client state parameter named FOO that is type STRING and has an initial value of BAR`
-   `Add a handler so that when I click the Submit button, it saves the record.`

## What to ask for Page Insights

Now Assist Page Insights can extract information from pages, components, and data resources. Use the Now Assist page insights to save time when investigating a page built by a different user or when identifying where data is coming from within a component.

-   `List all the components on my page and say if they are using presets`
-   `How are the components bound to the data resources?`
-   `What components have theme overrides?`
-   `Are there any unused client scripts?`

**Parent Topic:**[Working in UI Builder](using-ui-builder.md)

## Get help with the Now Assist panel in UI Builder

Ask questions and get quick answers without leaving UI Builder.

### Before you begin

-   Role required: ui\_builder\_admin
-   The Now Assist for Creator plugin is activated

### About this task

Responses and outputs from Now Assist can vary, even when the same prompt is used multiple times. Always review the generated content carefully to ensure accuracy and completeness.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  Create or open a page.

4.  In the upper right, select the Now Assist icon ![](../image/uib-sparkle-icon.png) to open the Now Assist panel.

    **Tip:** The Now Assist panel opens in a pinned position by default, keeping it fixed on your screen. Select the pin icon ![](../image/uib-pin-icon.png)to make the panel movable. When unpinned, drag the panel freely across the workspace for greater flexibility and visibility.

5.  Enter your question or task in the text field.

6.  Press the Enter key or select the **Send** button.

    Now Assist uses generative AI to provide immediate answers to your questions.

    ![UI Builder editor with the Now Assist Now Assist panel open, showing a question and a response.](../image/uib-nap-result.png)

7.  Continue the conversation with follow-up questions as needed.


