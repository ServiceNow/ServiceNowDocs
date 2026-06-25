---
title: Enable actionable knowledge feedback
description: The actionable knowledge feedback feature is available when the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\) plugin is activated and the actionable knowledge feedback properties are enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/knowledge-management/configure-act-know-feedback-properties.html
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
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


-   **[Create field mapping from an HR case to a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/map-hrcase-knowledge-article.md)**  
Copy information from an HR case into a knowledge article by creating custom mapping between the HR case table and the KCS article table.
-   **[Add a property to enable creating knowledge articles from HR cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/property-hrcase-knowledge-article.md)**  
Add a property, which is required to allow users to create a knowledge article from an HR case.
-   **[Create a UI action to enable creating knowledge articles from HR cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/ui-action-hrcase-article.md)**  
Create a UI action to add the Knowledge check box to the HR case form.

**Parent Topic:**[Configuring Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/configuring-knowledge-management.md)

**Related topics**  


[Actionable Knowledge Feedback Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/r_KnowledgeProperties.md)

