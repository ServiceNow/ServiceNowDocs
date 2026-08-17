---
title: Add topic prompts for the Topic Assist widget
description: Add preconfigured chat prompts to a topic so employees can start a conversation with the assistant directly from the topic page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-add-topic-prompts.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
keywords: [Topic Assist, topic prompts, Employee Slate, ServiceNow Otto]
breadcrumb: [Browse and topic experience, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Add topic prompts for the Topic Assist widget

Add preconfigured chat prompts to a topic so employees can start a conversation with the assistant directly from the topic page.

## Before you begin

Configure the browse experience for your Employee Slate experience. For more information, see [Configure browse experience in Employee Slate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-configure-browse-experience.md).

Role required: admin or sn\_hr\_sp.esc\_admin

## About this task

The Topic Assist widget shows on a topic page only when the experience chat type is Moveworks.

**Note:** For other experiences, the topic assist isn't available.

## Procedure

1.  Go to the topic record, and open the **Suggested Prompts** related list.

    \[Omitted image "es-ask-otto-prompts.png"\] Alt text: Topic record Suggested prompts related list showing entries for label, active status, order, and prompt text.

2.  Select **New**, and set the following fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

The text that employees see on the prompt in the Topic Assist widget, for example, `Avoid phishing scams`.

</td></tr><tr><td>

**Instruction**

</td><td>

The exact question or request sent to the assistant when an employee selects the label.**Note:** Max size of prompt instruction can be 255 characters.

</td></tr></tbody>
</table>3.  Save the record.

4.  Repeat the previous steps to add more prompts for the topic.

    The prompts are now saved.

5.  Go to any other tab such as **Application** or **Quick Link** to associate with the topic.


## Result

Employees who open the topic page see the Topic Assist widget with the configured prompts. Selecting a prompt starts a conversation with the assistant using the associated prompt text. When you configure other tabs such as **Featured Content** or **Application** or **Quick Link**, your employees can see associated apps, quick links, and content.

