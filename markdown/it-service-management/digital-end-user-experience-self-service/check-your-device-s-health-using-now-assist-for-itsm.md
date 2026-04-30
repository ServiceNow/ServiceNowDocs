---
title: Check your device’s health using Now Assist for ITSM
description: Use the Now Assist for ITSM Virtual Agent to monitor your device's performance and diagnose potential issues. DEX Self-service provides information about your device's health and helps you improve it.
locale: en-US
release: yokohama
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: task
last_updated: "2025-03-27"
reading_time_minutes: 4
breadcrumb: [Using Digital End-user Experience Self-service, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Check your device’s health using Now Assist for ITSM

Use the Now Assist for ITSM Virtual Agent to monitor your device's performance and diagnose potential issues. DEX Self-service provides information about your device's health and helps you improve it.

## Before you begin

Confirm that the DEX plugin \(sn\_dex\) is installed.

You must configure the Now Assist for ITSM to access the Check Device health topic in the Virtual Agent chat box.

Role required: none

## Procedure

1.  Select the Virtual Agent or chat icon \(![Virtual agent or chat icon](../image/icon-virtual-agent.png)\) that appears on any portal or Desktop Assistant header.

    **Note:** If you're launching the Virtual Agent from Desktop Assistant, make sure the DEX Desktop Assistant \[sn\_dex\_desktop\] plugin and the Desktop Assistant application are installed. For more details, see [Install Digital End-User Experience](install-app-device-health.md)and [Download and install Desktop Assistant](download-desktop-experience.md).

2.  Perform any of the following actions to begin a conversation:

    -   In the chat window, enter a phrase related to Device health check and press Enter, for example, “I want to check my device health”.

        **Note:** If you enter a phrase related to a category or subcategory, the Virtual Agent directly provides the resolution based on the entered category, and the conversation starts with those resolutions. For example, if you enter the phrase "How is my device battery health," the Virtual Agent returns the device's battery health status and provides resolutions to improve it

    -   Select the **Show my options** button, and then select the **Check Device Health** topic.
    The Virtual Agent displays a list of devices to check the device health if there are multiple devices. After you select a device, or if only one device is available, its status is displayed.

    The Virtual Agent also suggests a list of required resolutions to improve the device performance.

3.  If you have more than one device, select the required device to check its health.

    ![Check device's health using Now Assist for ITSM](../image/Check_device_health_first_image.png)

4.  Select the required resolution to improve the device performance.

    **Note:** The resolution can either be a remedial action, a self-help instruction, or an URL. For more information, see [Resolution for Proactive Engagement](../../proactive-engagement/reference/resolutions.md)

<table id="table_z5k_bwb_glb"><thead><tr><th>

Resolution Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

If the selected resolution is of type remedial action.

</td><td>

The Virtual Agent ask for your consent to continue with the selected remedial action if it is configured to do so.![Remedial action in Now Assist for ITSM](../image/Check_device_check_in_now_assist_remedial_action.png)

 -   If the resolution is successful, the Virtual Agent returns a success message and allows you to proceed to any pending actions.
-   If the resolution is not successful, the Virtual Agent returns a failure message and allows you to proceed to any pending actions.
-   If resolution is still in progress, the virtual agent returns a message that says “We have executed this resolution and it is in progress. We will let you know once it is completed”.


</td></tr><tr><td>

If the selected resolution provides self-help resolution.

</td><td>

Virtual Agent displays the steps to resolve the issue.![Self help instructions in Now Assist for ITSM](../image/Check_device_health_check_self_help_instructions.png)

</td></tr><tr><td>

If the selected resolution provides a URL as a resolution.

</td><td>

Virtual Agent opens the URL in a new browser tab when clicked. For example, it can be a URL of a KB article.

</td></tr><tr><td class="sub-head" colspan="2">

After the resolution is provided, the Virtual Agent returns the following messages based on the device health.

</td></tr><tr><td>

If there are any pending actions left to improve the device performance.

</td><td>

When the Virtual Agent returns pending actions, you can do any of the following actions:

 -   Select **Yes** to trigger the pending actions.
-   Select **No** to see the incidents or request created in the conversation along with the summary of all the actions performed during conversation flow appears. Then it asks the if the conversation was helpful.


</td></tr><tr><td>

If any of the triggered actions selected during the conversation are still in progress.

</td><td>

If the triggered action takes longer than expected time, the Virtual Agent returns a message “We have executed this resolution and it is in progress. We will let you know once it is completed”. After the action is complete, the Virtual Agent sends a notification. Clicking the notification resumes the conversation with an updated summary.

</td></tr><tr><td>

If there are no pending actions.

</td><td>

The Virtual Agent provides a summary of all resolutions used in the current conversation, then asks if the conversation was helpful.

</td></tr></tbody>
</table>    After all the available resolutions suggested by the Virtual Agent are triggered, the virtual agent now checks if the conversation was helpful.

5.  Confirm to the Virtual Agent if this conversation was helpful.

    -   If you select **Yes**, the virtual agent asks for feedback rating, followed by a thank you message.
    -   If you select **No**, the virtual agent provides a fallback action based on the configured resolutions.
    **Note:**

    The fallback action depends on the number of resolutions triggered in the conversation:

    -   -   **One resolution**

    The Virtual Agent either redirects to a live agent, or creates an incident, or asks the user to create an incident, this is decided based on the fallback action configured in the resolution.

    **Note:**

    The resolutions and fallback options are defined by the admin in ServiceNow Proactive Engagement. To know more, see [Engagement Settings for Proactive Engagement](../../proactive-engagement/reference/engagement-settings.md)

    -   -   **More than one resolution**

    The Virtual Agent provides an option to create an incident.

6.  Rate the conversation at the end.

    The Virtual Agent returns a thank you message.


