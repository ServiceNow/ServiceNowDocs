---
title: Configure IO alert notifications for a third-party application
description: Set up a basic integration between Instance Observer \(IO\) and third-party integrations to route IO alert notifications to an external system in addition to emails and SMS.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 4
breadcrumb: [Alerts in Instance Observer, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Configure IO alert notifications for a third-party application

Set up a basic integration between Instance Observer \(IO\) and third-party integrations to route IO alert notifications to an external system in addition to emails and SMS.

## Before you begin

Role required: admin

**Important:** Third-party integrations are not supported in Regulated Market.

## About this task

**Note:** Third-party integrations support platforms such as Slack, Microsoft Teams, AWS, GCP, and Azure.

For Third-party integrations, webhook URLs may expire if a subscription is not renewed, or API keys may be invalid over time. Ensure that your integration credentials are kept up to date to avoid missed alert deliveries.

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Go to Instance Observer**.

2.  Log in to Instance Observer and navigate to **Alerts** &gt; **Configure Notification**.

3.  Select **+ Create Integration**.

4.  On the form, fill in the fields.

    For a third-party integration, enter the following:

<table id="table_vt4_ww5_z3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration type

</td><td>

Third-party. ServiceNow is selected by default.

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

Webhook URL as configured on your third-party \(external\) application.For more information, see [Create a scripted REST API](https://www.servicenow.com/docs/access?context=t_CreateAScriptedRESTService&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td></tr></tbody>
</table>    ![Create a webhook integration for a third-party application.](../image/io-webhook-third-party-integ.png)

5.  Select **Test Integration** to validate your configuration and verify if you can successfully send the payload to the configured application.

    If you do not have the correct URL details at hand, you can save the integration as **Draft** and return to complete it later.

    -   If the test is successful, you receive a `HTTP response 200 is successful` response. You can now proceed to submit the integration.
    -   If the test fails, an error message is displayed in red. Review and correct your integration details—such as the webhook URL, username, or password—and test again.

        **Important:** A successful test result is required before you can submit the integration. If you attempt to submit without testing, a validation message is displayed: `Successful Test Integration results required to submit your integration, or save as draft if you don't have a working URL.`

6.  **Submit** the integration and save it when the test is successful.

    The integration is created with a status **Enabled**.

7.  Verify the integration status.

    In the **Integrations** tab, confirm that the integration status shows as **Enabled**.

    **Note:** Only integrations with an **Enabled** status appear in the **Notification Rules** tab to link with the notification rule. Draft integrations are not available for selection until they are completed and enabled.

8.  To configure a notification rule for the third-party integration and send alerts to third-party applications, select the **Notification Rules** tab.

    1.  Select ![ellipsis icon.](../../../reuse/icons/product-icons/ellipsis-horizontal-outline-24.svg) for the notification rule, and select the **Edit** option.

    2.  Enter a name for the rule in the **Name** field of the Edit Rule pop-up.

    3.  Enter a description for the notification rule.

    4.  Select the **Third Party Integration** option as the **Notification Type** and select a value from the list.

    5.  Select **Save**.

9.  Verify alert payload delivery in the **Alert Console** by navigating to **Alerts** &gt; **Alert Console**.

    To confirm that your integration is working correctly after an alert is triggered:

    1.  Select your instance and **Get Snapshot** in the **Alert Console**.

    2.  From the **Generate Test Alert** list, select the alert you configured.

        The test alert that you configured appears in the list. For example, **Database Response Time** alert on your instance.

    3.  Verify that the alert payload is successfully delivered to the configured integration endpoint, which is third-party instance.

        The alert payload reaches the third-party instance so long as the webhook URL accepts the HTTP calls.

    4.  Check if the alert with the specified payload has reached its intended destination.

        If the alert had failed, then you will see that the **Alert Type** is in red, which means it has failed. On selecting the failed **Self-Service** alert icon you will see the message **Third Party Integration – Failed**.

10. To view, edit, or delete the URL in the Edit Integration pop-up, navigate back to **Alerts** &gt; **Configure Notifications** and select ![ellipsis icon.](../../../reuse/icons/product-icons/ellipsis-horizontal-outline-24.svg) for the integration.

    You can update the integration settings by selecting the **Edit** option. The **Delete** option remains inactive if the integration is associated with at least one notification rule.

11. Identify and resolve integration failures.

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

