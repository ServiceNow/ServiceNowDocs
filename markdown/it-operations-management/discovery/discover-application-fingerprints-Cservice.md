---
title: Discover applications using application fingerprints or ITOM Content Service
description: Discover applications using suggestions based on ServiceNow Predictive Intelligence or ServiceNow ITOM Content Service to create configuration items.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discover applications based on fingerprints, Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discover applications using application fingerprints or ITOM Content Service

Discover applications using suggestions based on ServiceNow Predictive Intelligence or ServiceNow ITOM Content Service to create configuration items.

## Before you begin

Role required: discovery\_admin

## About this task

Review application suggestions based on application fingerprints or ITOM Content Service and add them to discovery.

-   Fingerprint-based discovery uses algorithms to identify running processes and organizes them into groups. These process groups become suggested applications or candidates. You review suggested applications and choose which ones to discover. The list of suggested applications is refreshed every hour. To learn more, see [Discover applications based on fingerprints](discover-application-based-process.md).
-   ITOM Content Service identifies the products that you’re currently using and delivers new product suggestions every week. To learn more, see [ITOM Content Service](../concept/discovery-content-services.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Content 360**.

2.  Select an application suggestion to add to discovery based on either application fingerprints or ITOM Content Service.

<table id="choicetable_r5b_jxr_21c"><thead><tr><th align="left" id="d458587e191">

Suggestion source

</th><th align="left" id="d458587e194">

Actions

</th></tr></thead><tbody><tr><td id="d458587e200">

**Application fingerprints**

</td><td>

1.  Select the **AI suggested application fingerprints** widget.
2.  Select the suggestion under **Suggested Group Name**.
3.  On the Application fingerprints suggestion form that is displayed, verify the information.

For information about the form fields, see [Application fingerprint suggestion form](../reference/discovery-admin-app-fingerprint-form.md).

4.  Determine whether to add the suggestion to discovery.
    -   If the suggestion isn't relevant and you don't want to add it, select **Ignore**.
    -   If you want to add it, select **Add to discovery**.


</td></tr><tr><td id="d458587e253">

**ITOM Content Service**

</td><td>

1.  Confirm that you’ve opted in to ITOM Content Service.

**Note:** If the **Opt-in** option is displayed, you have not yet opted in. For more information, see [Share data on ITOM Content Service](share-data-itom-content-service.md).

2.  Select the **Content service suggestions** widget.
3.  Manually sync with suggestions from your system by selecting **Sync candidates**.

**Note:** If a message appears about the application scope, select **OK** to exit the message. Then, change the scope by selecting the application scope icon and selecting **Global**.

4.  In the Sync candidates confirmation window, select **Yes**.
5.  Review the list and select the name of the relevant suggestion to see more detailed information.

**Note:** You can select multiple suggestions to add to discovery at the same time. Select the check box next to each suggestion and then select **Activate**.

6.  Determine whether to add the suggestion to discovery.
    -   If the suggestion isn't relevant and you don't want to add it, return to the list of suggested applications.
    -   If you have made changes to the suggestion but do not want to add it to discovery, select **Save**.
    -   To add the suggestion to discovery select **Activate**.


</td></tr></tbody>
</table>
