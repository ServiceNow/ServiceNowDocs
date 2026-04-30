---
title: Exploring Flow generation with images
description: Create a flow or a subflow from an image by using Now Assist. Capture the detailed process in an image and attach the image to Workflow Studio. Now Assist generates a preview of the flow that you can modify and regenerate.
locale: en-US
release: zurich
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2025-08-07"
reading_time_minutes: 2
breadcrumb: [Flow generation with images, Now Assist for Creator, Build workflows]
---

# Exploring Flow generation with images

Create a flow or a subflow from an image by using Now Assist. Capture the detailed process in an image and attach the image to Workflow Studio. Now Assist generates a preview of the flow that you can modify and regenerate.

## Activation

The skill Flow generation with images is installed with the Now Assist for Creator \(sn\_now\_creator\) application. You can install this application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Benefits

Enable flow generation with images to gain these benefits.

-   Build a multi-step flow or subflow from an image in Workflow Studio. Supported triggers and actions are configured with appropriate data pill values.
-   Use standard flow design patterns.

## Supported LLMs

You can use Azure OpenAI, Google Gemini, or Anthropic Claude on AWS as the AI model provider for Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Supported trigger types

Flow generation supports a limited number of trigger types. You can use text directions to specify these trigger types.

-   Scheduled triggers
-   Record triggers
    -   Created
    -   Created or Updated
    -   Updated
-   Service Level Agreements triggers
-   Inbound email triggers
-   Service Catalog triggers

## General guidelines

Follow these general guidelines when generating a flow or subflow from an image by using Now Assist.

-   **Use clear images**

    Use high resolution images with clear shapes, text, and arrows. Avoid using blurred screenshots and images of unclear whiteboard diagrams.

-   **Keep it simple**

    Don't overload the diagram with excessive nodes. Break complex flows into smaller flows or subflows.

-   **Use standard symbols**

    Stick to the common flow chart notions so that AI can interpret the structure accurately. For example, rectangle for steps and diamond for decisions.

-   **Use clear and consistent labeling**

    Ensure that the step names, labels, and annotations are legible and consistent across the image.

-   **Start with triggers**

    Clearly indicate the flow trigger first, followed by actions and flow logic in the same order that you want them to be in the flow. Clearly indicate the expected outcome to avoid ambiguity.

-   **Show decision points explicitly**

    Use clearly marked yes/no decision branches.

-   **Use modular approach**

    Instead of generating one large and complex flow, generate multiple subflows through separate images and use them together in Workflow Studio.


