---
title: Use manual registration to establish the connection to the provider instance
description: The named contact administrator will establish a secure connection to the Impact Delivery Instance \(provider instance\) to transmit data with the Impact Store Application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/connect-instance-impact-store-app.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use manual registration to configure the Impact Store Application, Impact reference, Impact]
---

# Use manual registration to establish the connection to the provider instance

The named contact administrator will establish a secure connection to the Impact Delivery Instance \(provider instance\) to transmit data with the Impact Store Application.

## Before you begin

-   Confirm [Initiate the connection to Impact data with manual registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/initiate-the-connection-impact-delivery-instance.md) is completed.
-   A registration email with a direct link to the IDI provider connection form is sent to the named contact administrator in order during the initial connection to IDI.

Role required: Any Impact Store App role, IDI admin

## Procedure

1.  As the named contact administrator, open the **Welcome email** or access the instance registration tab in the Impact Delivery Instance.

    **Note:** If you didn’t receive the registration email, reach out to your Impact Squad.

2.  Select **Connect with Impact IDI** in the registration email to go to the Provider connection form to initiate the connection between the Impact Store Application and the Impact Delivery Instance.

    Detailed screens are available in the Impact Store Application manual registration steps.

    \[Omitted image "manual-registration-establish-connection.png"\] Alt text: The manual registration step to establish a connection between IDI and the Impact Store App.

3.  Complete the form.

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

-   Empty: No status available before initiating the connection to the provider.
-   Not onboarded: Status prior to connecting to IDI.
-   Up


</td></tr><tr><td>

Inbound status \(read-only\)

</td><td>

-   Empty: No status available prior to initiating the connection to the provider.
-   Not onboarded: Status prior to connecting to IDI.
-   Up


</td></tr></tbody>
</table>4.  Select **Save** on the Provider Connection New Record form.

5.  Select **Connect to Provider**.

6.  Select **Save** to continue.

    -   Validation checks are performed during the onboarding process while the state reflects awaiting validation.
    -   When the state reflects Validated, the health checks processed successfully and the **Connect to provider** button becomes available.
    **Note:** If the state updates to Validation failed, health checks failed and the provider isn't connected. Select the **Health Dashboard** link in the error banner to be directed to the Service Exchange health dashboard. View and diagnose errors and follow the steps provided to resolve the errors. If you are unable to resolve the issues, contact your Customer Service Manager for assistance.

7.  Select **Connect to provider**.

    A status message displays and updates confirming the synchronization process:

    -   Provider onboarding started: The connection is validated between the Impact Store App and the Impact Delivery Instance.
    -   Syncing settings to complete onboarding: Necessary components and settings are synchronizing and required for alignment.
    -   Onboarding Complete: All settings have synced and you're ready to sync data from the Impact Delivery Instance.
    \[Omitted image "onboarding-complete-png.png"\] Alt text: Provider and onboarding connection status and confirmation message.

8.  When the status updates to Onboarding Complete, select **Close**.

    The Outbound and Inbound statuses for the Provider connection will display Up when successfully connected and onboarded.

9.  Return to Guided Setup, and select **Mark Complete** to continue to verify the connection.

    \[Omitted image "create-provider-connection-automated-mark-complete.png"\] Alt text: The required step to mark the new provider connection creation as successful with the Mark as complete button on the Automated Registration page in Guided Setup.

    The **Verify the connection** activity becomes available in Guided Setup.


## What to do next

[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/verify-impact-data-connection.md).

**Parent Topic:**[Use manual registration to configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/use_manual_registration_configure_impact_store_application.md)

**Previous topic:**[Initiate the connection to Impact data with manual registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/initiate-the-connection-impact-delivery-instance.md)

**Next topic:**[Secure data transfer using Service Bridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/service-bridge-overview.md)

