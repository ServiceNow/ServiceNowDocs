---
title: Use automated registration to connect to the Impact Delivery Instance
description: The automated registration process simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-12-03"
reading_time_minutes: 2
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Use automated registration to connect to the Impact Delivery Instance

The automated registration process simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.

## Before you begin

[Run the Service Exchange pre-configuration scan](perform_pre_configuration_health_checks_impact_store_app.md) before this procedure.

Role required: impact admin and IDI admin

## About this task

The automated registration initiates and establishes the connection to the Impact Delivery Instance, the provider instance, into one combined step. The first task, Learn about registering your instance, is an overview of these steps. See [Configure the Impact Store Application](../concept/configuring-impact-platform.md) for a summary of the configuration steps.

For details on the data connection, see [Secure data transfer using Service Bridge](../concept/service-bridge-overview.md).

Role required: admin, an impact role

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Guided Setup** &gt; **Register your instance**.

2.  Select **Start Automated Registration \(preferred method\)** to register and connect to the Impact Delivery Instance.

3.  Select **Create provider connection**.

    ![Selection for Create provider connection.](../image/create-provider-connection-automated.png)

    The Provider connection record is launched and the fields will be populated.

    ![The Impact Store App provider connection record with the ServiceNow Company, URL, and pre-connection statuses populated.](../image/provider-connection.png)

    |Field|Description|
    |-----|-----------|
    |Company|ServiceNow Impact is pre-populated|
    |URL|The URL to the Impact provider instance is pre-populated.|
    |Outbound status|Not onboarded: The status will be Not onboarded prior to connecting to IDI.|
    |Inbound status|Not onboarded: The status will be Not onboarded prior to connecting to IDI.|

4.  Select **Save** to continue.

    The provider record refreshes.

5.  Select **Connect to Impact**.

    The on-board consumer confirmation message displays.

    ![Confirmation message to onboard the selected instance.](../image/onboard-confirmation.png)

6.  Select **OK** to continue.

    A progression bar displays. The on-boarding process will take a few minutes. You can close the progression window during onboarding.

7.  Return to the open tab, Start automated registration a provider instance in Guided Setup, and select **Mark Complete** to continue to verify the connection.

    ![The required step to mark the new provider connection creation as successful with the Mark as complete button on the Automated Registration page in Guided Setup.](../image/create-provider-connection-automated-mark-complete.png)

    The **Verify the connection** activity becomes available in Guided Setup.

    **Important:** Automated registration does not require manually completing additional connection and registration steps. See [Configure the Impact Store Application](../concept/configuring-impact-platform.md) for an overview of the two registration processes.

    ![Connect you instance menu with the manual registration steps outlined.](../image/manual-registration-steps.png)


## What to do next

[Verify Impact data connection](verify-impact-data-connection.md)

**Parent Topic:**[Configure the Impact Store Application](../concept/configuring-impact-platform.md)

**Previous topic:**[Run the Service Exchange pre-configuration scan](perform_pre_configuration_health_checks_impact_store_app.md)

**Next topic:**[Verify Impact data connection](verify-impact-data-connection.md)

