---
title: Configure IO alert notifications for a ServiceNow instance
description: Set up a basic integration between Instance Observer \(IO\) and ServiceNow to route IO alert notifications to a ServiceNow instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Configure notification, Integrations]
breadcrumb: [Alerts in Instance Observer, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Configure IO alert notifications for a ServiceNow instance

Set up a basic integration between Instance Observer \(IO\) and ServiceNow to route IO alert notifications to a ServiceNow instance.

## Before you begin

Role required: admin

## About this task

In addition to email and SMS notifications, you can send IO alert notifications to your ServiceNow instances.

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Go to Instance Observer**.

2.  Log in to Instance Observer and navigate to **Alerts** &gt; **Configure Notification**.

3.  Select **+ Create Integration**.

4.  On the form, fill in the fields.

    For a ServiceNow integration, enter the following:

<table id="table_vt4_ww5_z3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration type

</td><td>

ServiceNow is selected by default.

</td></tr><tr><td>

Integration Name

</td><td>

Name to identify the integration.

</td></tr><tr><td>

Authentication Type

</td><td>

Basic Authentication or an API key for the integration.For API Key, provide the key or username and password for the integration.

</td></tr><tr><td>

User name

</td><td>

User name associated with the integration.

</td></tr><tr><td>

Password

</td><td>

Password for the integration.

</td></tr><tr><td>

Enter URL

</td><td>

Webhook URL as configured on the ServiceNow instance.**Note:** This URL is for commercial instances only.

Create a webhook and web service while selecting the appropriate authentication access using your ServiceNow instance admin role.

For more information, see Create a scripted REST API

</td></tr></tbody>
</table>    ![Create a webhook integration for a ServiceNow instance.](../image/io-webhook-sn-integ.png)

5.  Select **Test Integration** to validate your configuration and verify if you can successfully send the payload to the configured ServiceNow instance.

    If you do not have the correct URL details at hand, you can save the integration as **Draft** and return to complete it later.

    -   If the test is successful, you receive a `HTTP response 200 is successful` response. You can now proceed to submit the integration.
    -   If the test fails, an error message is displayed in red. Review and correct your integration details—such as the webhook URL, username, or password—and test again.

        **Important:** A successful test result is required before you can submit the integration. If you attempt to submit without testing, a validation message is displayed: `Successful Test Integration results required to submit your integration, or save as draft if you don't have a working URL.`

6.  **Submit** the integration and save it when the test is successful.

    The integration is created with a status **Enabled**.

7.  Verify the integration status.

    In the **Integrations** tab, confirm that the integration status shows as **Enabled**.

    **Note:** Only integrations with an **Enabled** status appear in the **Notification Rules** tab to link with the notification rule. Draft integrations are not available for selection until they are completed and enabled.

8.  Link the integration to a notification rule and enable configuration for the notification rule by navigating to the **Notification Rules** tab and selecting the appropriate notification rule.

    You can also select ![ellipsis icon.](../../../reuse/icons/product-icons/ellipsis-horizontal-outline-24.svg) and select the **Edit** option. Once the integration is in **Enabled** status, it is available for selection in the **Notification Rules** list.

    1.  Enter a name for the rule in the **Name** field of the Edit Rule pop-up.

    2.  Enter a description for the notification rule.

    3.  Select the ServiceNow Integration option as the **Notification Type** and select a value from the list.

    4.  Select **Save**.

9.  Verify alert payload delivery in the **Alert Console** by navigating to **Alerts** &gt; **Alert Console**.

    To confirm that your integration is working correctly after an alert is triggered:

    1.  Select your instance and **Get Snapshot** in the **Alert Console**.

    2.  From the **Generate Test Alert** list, select the alert you configured.

        The test alert that you configured appears in the list. For example, **Database Response Time** alert on your instance.

    3.  Verify that the alert payload is successfully delivered to the configured integration endpoint, which is ServiceNow instance.

        The alert payload reaches the ServiceNow instance so long as the webhook URL is still accepting http calls.

    4.  Navigate to your ServiceNow instance and check if the alert has reached its destination.

        If the alert had failed, then the **Alert Type** is in red, which means it has failed.

10. Identify and resolve integration failures.

    If an integration fails after it has been enabled, for example, due to an expired webhook URL, an invalid API key, or expired credentials, then IO detects the failure and flags it for your attention. To identify and resolve a failed integration:

    1.  In the **Alert Console**, look for alerts displayed in red under the **Alert Type** column. A red indicator means the alert payload failed to deliver the notification.
    2.  Select the **Failed** link to view the full error details. For example, a `404` error indicating that the URL is invalid or the API key has expired.
    3.  Select **Update Integration** to edit the integration with the correct credentials or webhook URL, test it successfully, and resubmit to restore the integration to **Enabled** status.
    4.  Alternatively, you can navigate to **Alerts** &gt; **Configure Notification**, and select the integration with Failed status in the **Integration** tab. **Edit** the integration configuration, test the integration, and when it is successful, resubmit it to restore the integration to the Enabled status.
    The **Delete** option remains inactive if the integration is associated with at least one notification rule.

    **Important:** Until the integration is fixed and re-enabled, alert payloads will not be delivered to the failed endpoint.

    -   **IO alert notification channels**

        You can view the integration failures as alerts in three places:

        1.  As **Alert Type** in **Alert** &gt; **Alert Console**
        2.  As Notifications from ![bell icon](../image/io-bell-icon.png). Select **View Notification History** and filter with `Integration Failed`.
        3.  As an email notification with the integration name, error number, and the message.

**Parent Topic:**[Alerts in Instance Observer](../concept/io-alerts-intro.md)

