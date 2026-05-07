---
title: Use case: Create an AI-generated experience
description: Learn how to generate a multi-page UI experience from a natural language description.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Use case, Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Use case: Create an AI-generated experience

Learn how to generate a multi-page UI experience from a natural language description.

## Scenario

A government agency is rolling out a new citizen-facing service request portal on ServiceNow. A team of developers with varying levels of UI Builder experience needs to deliver multiple portal experiences quickly, including a dashboard for tracking request status by category, a tabbed experience for managing open cases by priority, and a breadcrumb-style experience for change requests. The team is under a tight deadline and cannot afford to build each experience from scratch.

## Problem

Manually creating a multi-page experience in UI Builder involves several steps, including configuring the experience structure, navigation style, chart types, page layouts, and data sources. This process can be particularly challenging for developers who are less familiar with UI Builder, as it presents a steep learning curve. Furthermore, even experienced developers may find the manual creation of multiple experiences to be repetitive and time-consuming, increasing the risk of inconsistencies throughout the portal.

## Solution

Experience generation empowers developers to create seamless experiences using natural language directly within the UI Builder. With this feature, developers can articulate their desired experience in a straightforward manner.

Now Assist automatically generates a fully structured multi-page experience preview, allowing developers to review the output. They can choose to save the generated experience or refine their prompt to regenerate it for further adjustments.

This functionality ensures that all team members, regardless of their level of expertise, can quickly produce a working experience within minutes. Subsequently, any necessary fine-tuning can be performed manually, streamlining the development process and enhancing overall productivity.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](../task/install-ui-generation.md) and [Grant UI Builder admin role](../task/grant-ui-builder-admin-role.md).

## Configuration steps

Perform the following steps to use Expereice generation feature in UI Builder:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  From the UI Builder Home page, select **Create**, then select **AI-Generated experience**.
3.  In the **Create an experience** form, enter a detailed description.

    For example:

    ```
    Create a Tabbed experience called Service Request Tracker to help track open cases by priority using a bar chart.
    ```

    **Tip:** The quality of the generated experience largely depends on the clarity of your prompt. Include the following details: the name of the experience, the navigation style \(such as Tabbed or Breadcrumb\), the type of chart, and the table that users interact with. To see examples of effective prompts, you use the **Try an example** option in the **Create an Experience** form before writing your own.

4.  Select **Generate preview**.

    Now Assist generates and displays a preview of the experience.

5.  Review the generated experience. If satisfied, select **Save and edit experience**.

    If not, refine the description and select **Regenerate preview**.

6.  After saving, review the main experience page to confirm the URL, app shell, roles, and page variants are correctly configured.
7.  Repeat the steps to create additional experience \(for example, Change Request Tracking and Request Status Dashboard experiences\).
8.  Open each saved experience in the page editor to fine-tune layouts, data sources, and styling as needed.

## Outcome

The development team creates three experiences in a few minutes, which is significantly faster than the hours it would take to build each one manually. Developers of all experience levels contribute, ensuring that the generated experiences have a consistent structure throughout the portal. As a result, the team can focus most of its time on meaningful customization rather than basic configuration.

**Parent Topic:**[UI Generation use cases](../task/ui-generation-use-cases.md)

**Related topics**  


[Experience Generation](concept-experience-generation.md)

[Create an AI-generated experience](../task/generate-ui.md#)

