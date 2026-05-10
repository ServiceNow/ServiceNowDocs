---
title: Exploring Flow generation with images
description: Create a flow or a subflow from an image by using Now Assist. Capture the detailed process in an image and attach the image to Workflow Studio. Now Assist generates a preview of the flow that you can modify and regenerate.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Flow generation with images, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
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

You can use Azure OpenAI, Google Gemini, or Anthropic Claude on AWS as the AI model provider for Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

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

Follow these general guidelines when writing Now Assist directions.

-   **Always describe the trigger first**

    Describe the flow trigger and its data conditions first. After the trigger, describe the actions and flow logic in the same order that you want them to be in the flow.

-   **Avoid spelling errors**

    Avoid misspelling the names of actions, flow logic, or tables. Consider using hash tags to avoid making mistakes with table names.

-   **Be precise and descriptive in your request**

    Make sure that your request is precise and descriptive. Describe the flow trigger, record data, actions, and flow logic in as much detail as you can. If you attach an image, make sure to attach a clear, high quality image of the process.

-   **Be succinct and direct in your request**

    Start by specifying whether you want to generate a flow or a subflow. For example, use the phrase, "`Create a flow that`" to generate a flow. Describe each step the flow in order.

-   **Refer to actions, flow logic, and tables by name**

    Use action, flow logic, and table names as part of your directions. The closer your directions are to the actual names, the easier it is for the LLM to recognize them. For example, use the text `for each` or `do the following in parallel` to refer to those specific flow logic options. For table names, consider using hash tags.

-   **Review the generated flow outline and input values**

    Review each action, flow logic, and subflow in the generated flow outline. Review the generated inputs values to confirm that they contain relevant data references.

-   **Use hash tags to refer to data in a specific table**

    Use a hash tag to select a specific table name. Hash tags are particularly useful to distinguish between tables that have identical or similar display names such as the User \[sys\_user\] and User \[imp\_user\] tables.

-   **Use numbers to distinguish the branches of do the following in parallel flow logic**

    Add a number to each parallel branch. For example, the directions, "`When a P1 incident is created, do the following in parallel: 1. Log its short description and 2. Look up the user assigned to it and send an email`," makes it clear that there are two branches.

-   **Use quotation marks to set exact values**

    Enclose exact data values in quotations marks to help the LLM distinguish between operation names and data values. For example, the directions, "`Log the value, 'incident reopened'`" make it clear that the text "incident reopened" is a data value.


**Parent Topic:**[Flow generation with images](../reference/flow-generation-with-images-landing.md)

