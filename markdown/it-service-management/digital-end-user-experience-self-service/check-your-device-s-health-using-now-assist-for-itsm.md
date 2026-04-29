---
title: Check device health using Now Assist for ITSM Virtual Agent
description: Use the Now Assist for ITSM Virtual Agent to monitor device performance, diagnose potential issues, and use suggested resolutions to address them.
locale: en-US
release: australia
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Check device health using Now Assist for ITSM Virtual Agent

Use the Now Assist for ITSM Virtual Agent to monitor device performance, diagnose potential issues, and use suggested resolutions to address them.

## Before you begin

-   Install the Digital End-User Experience \(sn\_dex\) application. For more information, see [Install Digital End-User Experience](install-app-device-health.md).
-   Configure Now Assist for ITSM to access the Check Device health topic in the Virtual Agent chat box.
-   Install the Desktop Assistant \[sn\_dex\_desktop\] plugin if you're launching Virtual Agent from Desktop Assistant. For more information, see [Download and install Desktop Assistant](download-desktop-experience.md).

Role required: none

## Procedure

1.  Select the Virtual Agent or chat icon \(![Virtual agent or chat icon](../image/icon-virtual-agent.png)\) that appears on any portal or on the Desktop Assistant header.

2.  Perform any of the following actions to begin a conversation:

    -   In the chat window, enter a phrase related to Device health check and press Enter.

        For example, `Check my device health`.

        **Note:** If you enter a phrase related to a category or subcategory, the Virtual Agent directly provides the corresponding resolution. For example, entering a phrase like `How is my device battery health` prompts the Virtual Agent to provide the battery health status and resolutions to improve it.

    -   Select the **Show my options** button, and then select the **Check Device Health** topic.
    The Virtual Agent displays a list of devices to check the device health if there are multiple devices. After you select a device, or if only one device is available, its status is displayed.

    The Virtual Agent also suggests a list of resolutions to improve the device performance.

3.  If you have more than one device, select a device to check its health.

4.  Select a resolution to improve device performance.

<table id="table_z5k_bwb_glb"><thead><tr><th>

Resolution Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remedial action

</td><td>

If configured, the Virtual Agent asks for your consent to continue with the selected remedial action.

 -   If the resolution is successful, the Virtual Agent returns a success message and guides you to the pending actions, if any.
-   If the resolution is not successful, the Virtual Agent returns a failure message and guides you to the next pending actions.
-   If resolution is in progress, the Virtual Agent updates you on its status and confirms that it will notify you once the action is complete.


</td></tr><tr><td>

Self-help instruction

</td><td>

The Virtual Agent lists the steps to resolve the issue.

</td></tr><tr><td>

Link to help resources

</td><td>

When you select the link, the Virtual Agent opens it in a new browser tab. For example, link to a Knowledge Base article.

</td></tr></tbody>
</table>    After you implement the suggested resolutions, the Virtual Agent returns the following messages based on the device health.

<table id="table_t2j_5mr_fgc"><thead><tr><th>

Condition

</th><th>

Virtual Agent response

</th></tr></thead><tbody><tr><td>

Actions triggered during the conversation are still in progress

</td><td>

If a triggered action takes longer than expected to complete, the Virtual Agent informs you that the action is in progress and will notify you once it's complete. After completion, selecting the notification resumes the conversation with an updated summary.

</td></tr><tr><td>

Pending actions remain to improve device health

</td><td>

The Virtual Agent displays the pending actions.

 -   Select **Yes** to trigger the pending actions.
-   Select **No** to see a summary of the incidents, requests, and actions performed during the conversation.


</td></tr><tr><td>

There are no pending actions

</td><td>

The Virtual Agent provides a summary of all resolutions used in the current conversation.

</td></tr></tbody>
</table>5.  Submit feedback about whether the suggested resolution helped resolve an issue.

    -   If you select **Yes**, the Virtual Agent prompts you for feedback and acknowledges your response.
    -   If you select **No**, the Virtual Agent provides a fallback action based on the configured resolutions.

        Fallback actions depend on the number of resolutions triggered during the conversation.

<table id="table_snq_pkr_fgc"><thead><tr><th>

Number of resolutions

</th><th>

Fallback action

</th></tr></thead><tbody><tr><td>

Single resolution

</td><td>

Depending on the fallback action configured in the resolution, the Virtual Agent redirects you to a live agent, creates an incident, or prompts you to create an incident.The DEX administrator configures the resolutions and fallback actions. For more information, see [Engagement Settings for Proactive Engagement](../../proactive-engagement/reference/engagement-settings.md).

</td></tr><tr><td>

Multiple resolutions

</td><td>

The Virtual Agent provides an option to create an incident.

</td></tr></tbody>
</table>6.  Provide a rating at the end of the conversation.


