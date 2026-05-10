---
title: Configure Auto-Responder for tasks other than cases
description: Configure the Auto-Responder feature to send helpful resources for tasks other than customer service cases.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Auto-Responder notifications, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Configure Auto-Responder for tasks other than cases

Configure the Auto-Responder feature to send helpful resources for tasks other than customer service cases.

## Before you begin

Role required: admin

Perform the following tasks.

-   Activate the Email Notification Script for Contextual Search Results plugin \(com.snc.adv\_cxs\_results\_email\_script\). For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).
-   Set the application scope to the scope of your task table using the application picker. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).
-   Verify that you have defined a search context for your task to include recommended resources in the Auto-Responder email notifications. For more information, see [Define a search context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/contextual-search/t_DefineSearchContext.md).
-   Verify that you have configured a table for the search context associated with your task. For more information, see [Configure table for a contextual search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/contextual-search/t_DefineContextualSearchForForm.md).

## Procedure

1.  Configure the Notification \[sysevent\_email\_action\] table for your task to use the csm\_AdvancedEmailSearchResults script.

    1.  Navigate to **System Notification** &gt; **Notifications**.

    2.  Select the Notification \[sysevent\_email\_action\] table for your task.

    3.  In the What will it contain related list, enter `${mail_script:csm_AdvancedEmailSearchResults}` in the **Message HTML** field.

    4.  Verify that notifications aren’t sent if there are no search results by entering the `hasResults()` function in the **Advanced condition** field of the When to send related list.

        The `hasResults()` function checks whether search results exist. You can use the return value of the function to avoid the system from sending an email notification if there are no search results. For more information, see [Advanced conditions for email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_OptSpecifyingAdvancedCond.md).

        **Tip:** Refer to the Case auto-responder recommendations notification that uses the `hasResults()` function for returning the search results value. To view a notification, navigate to **System Notification** &gt; **Notifications**.

    5.  Select **Update**.

2.  Map your task table configuration with the email notification for your task.

    1.  Navigate to **Contextual Search** &gt; **Table Configuration**.

    2.  Select the task table configuration link in the **Name** column corresponding to the row containing the search context for your task.

        For the table that you’re configuring, be sure to do the following:

        -   Train the similarity solution for the table. For more information, see [Train the similarity solution for finding Auto-Responder notification content](train-sol-defn-auto-responder.md).
        -   Add the similarity solution in the Additional Resource Configurations tab on the Search Context form.
    3.  In the Email Conﬁgurations related list, link your task table configuration with the Notification \[sysevent\_email\_action\] table.

        -   To create another email configuration for a user field, select **New**.
        -   To edit an existing email configuration, select the preview email configuration for email notification icon \(![Preview Email Configuration for email notification icon.](../image/preview.png)\), and then in the Email Configuration window, select **Open Record**.
    4.  On the Email Configuration form, verify the default field values for your task, or fill in the values for a custom configuration.

<table id="table_i5s_5fq_xlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email notification

</td><td>

Select the email notification for your task.

</td></tr><tr><td>

User field

</td><td>

Reference field that helps narrow down the search results sent as recommended resources in Auto-Responder email notifications. For example, if you select **Caller** for the Incident \[incident\] table, the resources associated only with callers are added to the Auto-Responder email notifications.

**Note:** This is a mandatory field for Auto-Responder. This field must be a reference field of the User table \(sys\_user\) or tables that extend the User table.

</td></tr><tr><td>

Limit

</td><td>

Maximum number of resources you want to include in the Auto-Responder email notifications for your task.

 The maximum allowed limit value is 20. If you enter a value more than 20, the Auto-Responder email notification includes up to 20 resources only.

</td></tr></tbody>
</table>    5.  Update or submit the Email Configuration form.

        -   For a new configuration, select **Submit**.
        -   For an existing configuration, select **Update**.
3.  Enable contextual search results based on text searches in addition to search results based on Predictive Intelligence to be included in Auto-Responder notifications.

    For more information, see [Enable text search recommendations in Auto-Responder notifications](enable-text-based-auto-responder.md).

4.  Configure a custom portal and include advanced contextual search results in email notifications.

    For more information, see [Include advanced contextual search results in Auto-Responder notifications](use-extension-point-auto-responder.md).


