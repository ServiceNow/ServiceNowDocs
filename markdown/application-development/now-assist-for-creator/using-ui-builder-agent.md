---
title: Using UI Builder agent
description: Use the UI Builder agent to learn about features and functionality, understand your page setup, and accelerate page configuration.Use this feature to learn about UI Builder.Use this feature to understand the architecture and functionality of a page and its elements.Use this feature to build and modify your page.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 5
breadcrumb: [Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Using UI Builder agent

Use the UI Builder agent to learn about features and functionality, understand your page setup, and accelerate page configuration.

The UI Builder agent introduces key features to enhance user experience. It offers an informative resource to answer questions about the features and functionality of UI Builder and provides links to relevant documentation. Additionally, it gives an overview of page configuration, helping developers understand the structure and interconnections of page elements. It also streamlines the process of modifying and enhancing pages by enabling you to apply different layouts, configure components, and update styles.

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

**Parent Topic:**[Using UI generation](using-ui-generation.md)

## Learn about UI Builder

Use this feature to learn about UI Builder.

### Before you begin

Install Now Assist for UI generation application. For more information, see [Install UI generation](../task/install-ui-generation.md).

Role required: ui\_builder\_admin

### About this task

This feature answers your questions about the UI Builder. It provides information about the features and functionalities of the UI Builder. Additionally, it includes links to relevant product documentation.

### Procedure

1.  Navigate to **All** &gt; **UI Builder**

2.  Create a new experience or navigate to an existing one.

    For more information about creating an experience, see [Create an AI-generated experience](../task/generate-ui.md#).

3.  Create a new page or navigate to an existing one.

4.  From the page editor, open the Now Assist panel.

5.  In the chat panel, ask a question about UI Builder.

    **Tip:** You can ask about specific features or tasks, such as `What is a data resource?`, or `How can I add a component to my page?`

    You receive instant responses based on the latest ServiceNow documentation.


### Result

The UI Builder agent processes your question and provides answers, along with relevant documentation links.

For example:

![In the Now Assist panel, ask a question about UI Builder to get instant answers.](../image/ui-gen-agent-learn-uib.png)

**Note:** The UI Builder agent operates only within UI Builder.

## Understand page configuration

Use this feature to understand the architecture and functionality of a page and its elements.

### Before you begin

Install Now Assist for UI generation application. For more information, see [Install UI generation](../task/install-ui-generation.md).

Role required: ui\_builder\_admin

### About this task

This feature provides insights into how a page is constructed, including its design and structure. It can describe how various elements on the page are configured. This feature helps developers to quickly anticipate how future changes might impact functionality.

### Procedure

1.  Navigate to **All** &gt; **UI Builder**

2.  Create a new experience or navigate to an existing one.

    For more information about creating an experience, see [Create an AI-generated experience](../task/generate-ui.md#).

3.  Create a new page or navigate to an existing one.

4.  From the page editor, open the Now Assist panel.

5.  In the chat panel, enter your question.

    **Tip:** You can inquire about the configuration of your page. For instance, you might ask, `Is dynamic theming implemented on my page?`, or `Are any client scripts utilized on my page?`.


### Result

Based on your request, the UI Builder agent provides a detailed explanation of the page configuration.

For example:

![In the Now Assist panel, ask a question about the page configuration to get instant answers.](../image/ui-gen-agent-understand-page-configpng.png)

**Note:**

-   The UI Builder agent operates only within UI Builder.
-   This feature is available only when you’re viewing a page in the page editor.

## Accelerate page configuration

Use this feature to build and modify your page.

### Before you begin

Install Now Assist for UI generation application. For more information, see [Install UI generation](../task/install-ui-generation.md).

Role required: ui\_builder\_admin

### About this task

This feature enables you to easily modify and enhance your page. You can apply different layouts, such as a single row or a three-column format. Additionally, you can add and configure components, such as buttons with labels and links that direct users to external websites. You can also update the styling of your page, such as changing the background color.

### Procedure

1.  Navigate to **All** &gt; **UI Builder**

2.  Create a new experience or navigate to an existing one.

    For more information about creating an experience, see [Create an AI-generated experience](../task/generate-ui.md#).

3.  Create a new page or navigate to an existing one.

4.  From the page editor, open the Now Assist panel.

5.  In the chat panel, request a page modification, and then select **Send**.

    **Tip:** You can request to apply layouts \(such as single-row or three-column\), add components \(such as buttons with labels and links to external websites\), and update the page styles \(for example, changing the background color\).


### Result

UI Builder agent implements the modifications and enhancements to the design and functionality of your page.

For example: ![In the Now Assist panel, request a page modification.](../image/ui-gen-agent-accelerate-page-config.png)

**Note:**

-   The UI Builder agent operates only within UI Builder.
-   This feature is available only when you’re viewing a page in the page editor.

|Symptom|Cause|Resolution|
|-------|-----|----------|
|UI Builder Agent does not respond|The UI Builder Agent skill is disabled, or the user is outside of UI Builder.|Enable the UI Builder Agent in Now Assist Admin. The agent operates only within UI Builder and is not available in other areas of the platform.|

**Related topics**  


[UI Builder Agent](uib-builder-agent-concept.md)

[Use case: Using UI Builder Agent](use-case-ui-builder-agent.md)

