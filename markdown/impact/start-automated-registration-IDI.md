---
title: Use automated registration to connect to the Impact Delivery Instance
description: The automated registration process simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Use automated registration to connect to the Impact Delivery Instance

The automated registration process simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.

## Before you begin

[Run your first scan with the Scan Engine](run-scan-engine.md) before this procedure.

Role required: impact app admin and impact admin \(IDI\)

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Guided Setup** &gt; **Register your instance**.

2.  Select **Start**.

3.  Select **Learn about registering your instance** to read an overview of these steps.

    See [Configure the Impact Store Application](../concept/configuring-impact-platform.md) for a summary of the configuration steps.

4.  **Mark as Complete** to continue.

5.  Select **Start Automated Registration \(preferred method\)** from the Activities pane.

6.  Select the **Create registration** link.

    ![Create registration link and the check registration status links on the registration page.](../image/guided-setup-start-auto-registration.png)

    **Note:** It may take a few moments to connect to the Impact Delivery Instance and process the registration.

7.  Select **Check registration status** to monitor the provider connection progress and generate the connection link.

    **Important:** After your instance registration is established, a success message is generated with the **Create provider connection** link. The status updates only after the registration has been successfully created. You may need to repeat this step to allow the registration to complete.

8.  Select the **Create provider connection** link in the success message.

    A new Provider connection registration record is created and linked to your Impact Delivery Instance.

    ![The Impact Store App provider connection record with the ServiceNow Company, URL, and pre-connection statuses populated.](../image/provider-connection.png)

9.  Refer to the Provider Connection record table for information about the form:

<table id="table_fbs_gqq_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Company

</td><td>

ServiceNow Impact is pre-populated. If necessary, select ServiceNow Impact from the field selector.

</td></tr><tr><td>

State \(read-only\)

</td><td>

-   Pending: Connection is in progress.
-   Awaiting validation: After saving the record, Service Exchange Health scan checks are performed.
-   Validated: Health checks succeed and the provider is connected.
-   Validation failed: Health checks failed, the provider isn't connected.


</td></tr><tr><td>

URL \(read-only\)

</td><td>

The URL to the Impact provider instance is pre-populated.

</td></tr><tr><td>

Outbound status \(read-only\)

</td><td>

-   Blank: No status available prior to initiating the connection to the provider.
-   Not onboarded: Status prior to connecting to IDI.
-   Up


</td></tr><tr><td>

Inbound status \(read-only\)

</td><td>

-   Blank: No status available prior to initiating the connection to the provider.
-   Not onboarded: Status prior to connecting to IDI.
-   Up


</td></tr></tbody>
</table>10. Select **Save** to continue.

    Validation checks are performed during the onboarding process while the state reflects Awaiting validation.

    When the state reflects Validated, the health checks processed successfully and the **Connect to provider** button becomes available.

    If the state updates to Validation failed, health checks failed and the provider isn't connected.

    ![Failed validation banner with the link to the Health Dashboard.](../image/onboarding-failed.png)

    1.  Select the **Health Dashboard** link in the error banner to be directed to the Service Exchange health dashboard.
    2.  View and diagnose the errors.
    3.  Follow the steps provided to resolve the issues.

        **Important:** If you are unable to resolve the issues, contact your Customer Service Manager for assistance.

    4.  Select the **Provider connection record link** and restart the Automated registration.
11. Select **Connect to provider**.

    A status message displays and updates confirming the synchronization process:

    -   Provider onboarding started...: The connection is validated between the Impact Store App and the Impact Delivery Instance.
    -   Syncing settings to complete onboarding...: Necessary components and settings are synchronizing and required for alignment.
    -   Onboarding Complete: All settings have synced and you are ready to sync data from the Impact Delivery Instance.
    ![Provider and onboarding connection status and confirmation message.](../image/onboarding-complete-png.png)

12. When the status updates to Onboarding Complete, select **Close**.

    The Outbound and Inbound statuses for the Provider connection will display Up when successfully connected and onboarded.

13. Return to the open tab, **Start automated registration a provider instance** in Guided Setup, and select **Mark Complete** to continue to verify the connection.

    ![The required step to mark the new provider connection creation as successful with the Mark as complete button on the Automated Registration page in Guided Setup.](../image/create-provider-connection-automated-mark-complete.png)

    Upon successful connection, you can skip, manual registration and proceed to the **Verify the connection** activity in Guided Setup.


## What to do next

[Verify Impact data connection](verify-impact-data-connection.md)

**Parent Topic:**[Configure the Impact Store Application](../concept/configuring-impact-platform.md)

**Previous topic:**[Run your first scan with the Scan Engine](run-scan-engine.md)

**Next topic:**[Verify Impact data connection](verify-impact-data-connection.md)

