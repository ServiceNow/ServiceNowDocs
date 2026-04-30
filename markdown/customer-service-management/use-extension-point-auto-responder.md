---
title: Include advanced contextual search results in Auto-Responder notifications
description: Use scripted extension points to include the advanced contextual search results in email notifications for content suggested by the Auto-Responder feature.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Auto-Responder notifications, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Include advanced contextual search results in Auto-Responder notifications

Use scripted extension points to include the advanced contextual search results in email notifications for content suggested by the Auto-Responder feature.

## Before you begin

Role required: admin

-   Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\). For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and [Predictive Intelligence for CSM solution definitions](../concept/predictive-intelligence-for-csm.md).
-   Set the application scope to Email Notification Script for Contextual Search Results. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## About this task

The Email Notification Script for Contextual Search Results plugin \(com.snc.adv\_cxs\_results\_email\_script\) installs the csm\_AdvancedEmailSearchResults script, CSMAdvancedEmailSearchResults script include and CSMAdvancedEmailSearchResultsExtensionPoint extension points.

The csm\_AdvancedEmailSearchResults script is preconfigured for the customer service portal and consumer service portal.

Using extension points makes it easier to integrate customizations without actually altering the base code. You can extend standard base functionality using customized scripts. For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

An implementation is available in the base system for scripted extension points. You can modify the data and add additional fields.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, search for and click **sn\_adv\_emailscript.CSMAdvancedEmailSearchResultsExtensionPoint**.

3.  On the Extension Point form, select a script include to use the CSMAdvancedEmailSearchResultsExtensionPoint extension points.

    -   Modify the existing script by going to the Implementations related list and clicking **CaseAutoresponder**.
    -   Create and register a custom script include.

        For more information, see [Registering custom script includes against the scripted extension points](../../../build/applications/concept/impl-scripted-ext-pts-custom-code.md).

4.  Modify the script to use the extension points available through the CSMAdvancedEmailSearchResults script include.

    You can create multiple implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed first.

<table id="table_qnt_srm_plb"><thead><tr><th>

Configuration

</th><th>

Implementation

</th></tr></thead><tbody><tr><td>

Include a custom portal and search for knowledge articles from the knowledge base associated with the custom portal.**Note:** Applies only to tasks other than customer service cases.

</td><td>

Modify the updateSearchRequestConfig extension point to include the custom portal for your tasks other than customer service cases.

</td></tr><tr><td>

Filter out the content by the duration of the last viewed content.

</td><td>

Modify the getViewedContent extension point by entering the last viewed content duration in days.**Note:** By default, any knowledge articles viewed in the last 30 days by the user are not included in the email notification.

</td></tr><tr><td>

Define the layout of the email notifications.

</td><td>

Modify the printSearchResults extension point to specify a custom layout for the Auto-Responder email notifications.

</td></tr></tbody>
</table>5.  On the Extension Point form, click **Update**.


