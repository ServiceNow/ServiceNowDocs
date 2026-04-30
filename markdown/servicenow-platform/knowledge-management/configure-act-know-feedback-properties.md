---
title: Enable actionable knowledge feedback
description: The actionable knowledge feedback feature is available when the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\) plugin is activated and the actionable knowledge feedback properties are enabled.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable actionable knowledge feedback

The actionable knowledge feedback feature is available when the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\) plugin is activated and the actionable knowledge feedback properties are enabled.

## Before you begin

Role required: admin

## About this task

The actionable feedback feature is available in the Knowledge Management Service Portal and Agent Workspace. To use the actionable feedback feature in other service portals, you can activate the Knowledge Article View page route map. For new customers, the Knowledge Article View page route map is activated by default.

**Note:** The actionable knowledge feedback is not supported in Knowledge Management v3.

A feedback task is created for an article when the article is flagged. For generating feedback tasks when an article is marked as not helpful or rated below a set value, you must set the following associated properties.

**Note:** When you select **No** on the article form, an actionable feedback pop-up window appears. On the Actionable feedback form, choose one of the reasons to provide feedback. If you choose **Other** as a reason consider providing feedback details.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Properties**.

2.  In the **Actionable Feedback Properties** section, configure the following properties:

<table id="table_eyc_mnl_kdb"><thead><tr><th>

Property

</th><th>

Setting

</th></tr></thead><tbody><tr><td>

Create actionable feedback task when an article is flagged

</td><td>

By default, the property is set to **Yes** and feedback tasks are created when the article is flagged.

</td></tr><tr><td>

Create actionable feedback task when an article is marked as not helpful

</td><td>

Select **Yes**.

</td></tr><tr><td>

Create actionable feedback task when an article is rated at or lower than this value. 0 or no value indicates that actionable feedback tasks are not enabled for Rating type feedback

</td><td>

Enter a value from 1 to 5 to specify the rating threshold for generating a feedback task. For example, if you set this value to 3, a feedback task is generated when a user selects three or less stars to rate an article.

 **Note:** If you enter '0', a negative article feedback does not generate a feedback task.

</td></tr><tr><td>

Create actionable feedback task only when feedback details are provided for the negative feedback

</td><td>

Select the check box to enable actionable feedback task generation for the negative feedback. Set this value to "True", to activate this feature.

</td></tr></tbody>
</table>3.  Click **Save**.


**Related topics**  


[Actionable Knowledge Feedback Properties](../reference/r_KnowledgeProperties.md#)

