---
title: Use automated registration to connect to the Impact Delivery Instance
description: The automated registration process simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/impact/start-automated-registration-IDI.html
release: zurich
topic_type: task
last_updated: "2025-12-03"
reading_time_minutes: 2
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Use automated registration to connect to the Impact Delivery Instance

The automated registration process simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.

## Before you begin

[Run your first scan with the Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/run-scan-engine.md) before this procedure.

**Important:** Impact Store Application features that require a connection to the Impact Delivery Instance:

-   Communication with your Impact Squad, including visibility into changes you make in your own Impact Workspace
-   Capabilities Maps
-   Accelerators
-   Recommendations
-   Product Adoption Roadmaps
-   Value Management

Role required: impact app admin and impact admin \(IDI\)

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Guided Setup** &gt; **Register your instance**.

2.  Select **Start Automated Registration \(preferred method\)** to register and connect to the Impact Delivery Instance.

3.  Select **Create provider connection**.

    \[Omitted image "create-provider-connection-automated.png"\] Alt text: Selection for Create provider connection.

    The Provider connection record is launched and the fields will be populated.

    \[Omitted image "provider-connection.png"\] Alt text: The Impact Store App provider connection record with the ServiceNow Company, URL, and pre-connection statuses populated.

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

    \[Omitted image "onboard-confirmation.png"\] Alt text: Confirmation message to onboard the selected instance.

6.  Select **OK** to continue.

    A progression bar displays. The on-boarding process will take a few minutes. You can close the progression window during onboarding.

7.  Return to the open tab, Start automated registration a provider instance in Guided Setup, and select **Mark Complete** to continue to verify the connection.

    \[Omitted image "create-provider-connection-automated-mark-complete.png"\] Alt text: The required step to mark the new provider connection creation as successful with the Mark as complete button on the Automated Registration page in Guided Setup.

    The **Verify the connection** activity becomes available in Guided Setup.

    **Important:** Automated registration does not require manually completing additional connection and registration steps. See [Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/configuring-impact-platform.md) for an overview of the two registration processes.

    \[Omitted image "manual-registration-steps.png"\] Alt text: Connect you instance menu with the manual registration steps outlined.


## What to do next

[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/verify-impact-data-connection.md)

**Parent Topic:**[Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/configuring-impact-platform.md)

**Previous topic:**[Run the Service Exchange pre-configuration scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/perform_pre_configuration_health_checks_impact_store_app.md)

**Next topic:**[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/verify-impact-data-connection.md)

