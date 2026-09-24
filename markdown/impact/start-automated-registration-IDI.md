---
title: Use automated registration to IDI
description: The automated registration process in Guided Setup simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/start-automated-registration-IDI.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Impact Guided Setup, Configuring Impact, Impact]
---

# Use automated registration to IDI

The automated registration process in Guided Setup simplifies the configuration process and connects your Impact Store Application with data from the Impact Delivery Instance.

## Before you begin

[Onboard users to the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/onboard_users_impact_store_application.md)

**Important:** Impact Store Application features that require a connection to the Impact Delivery Instance:

-   Communication with your Impact Squad, including visibility into changes you make in your own Impact Workspace
-   Capabilities Maps
-   Accelerators
-   Recommendations
-   Product Adoption Roadmaps
-   Value Management

See [Impact Delivery Instance overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-delivery-instance-reference.md) for additional information.

Role required: impact app admin and impact admin \(IDI\)

## About this task

This task automates the secure connection to the provider, the Impact Delivery Instance and runs the full onboarding process automatically.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Guided Setup** &gt; **Register your instance**.

2.  Select **Start**.

3.  Select **Learn about registering your instance** to read an overview of these steps.

    See [Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md) for a summary of the configuration steps.

4.  **Mark as Complete** to continue.

5.  Select **Start Automated Registration \(preferred method\)** from the Activities pane.

6.  Select the **Connect to Impact** link.

    **Note:** It may take a few moments to connect to the Impact Delivery Instance and process the registration.

7.  Select **Check registration status** to monitor the provider connection progress.

    **Important:** After your instance registration is established, a success message is generated with the and the status updates only after the registration has been successfully created. You may need to repeat this step to allow the registration to complete.\[Omitted image "guided-setup-start-auto-registration.png"\] Alt text: Connect to Impact link and the check registration status links on the Automated registration page.

8.  When the status updates to Onboarding Complete, select **Close**.

    The Outbound and Inbound statuses for the Provider connection will display Up when successfully connected and onboarded.

    If the state updates to Validation failed, health checks failed and the provider isn't connected.

    \[Omitted image "onboarding-failed.png"\] Alt text: Failed validation banner with the link to the Health Dashboard.

    1.  Select the **Health Dashboard** link in the error banner to be directed to the Service Exchange health dashboard.
    2.  View and diagnose the errors. See [Service Exchange Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-se-center.md) for additional information.
    3.  Follow the steps provided to resolve the issues.

        **Important:** If you are unable to resolve the issues, contact your Customer Service Manager for assistance.

9.  Return to the open tab, **Start automated registration \(Preferred method\)** in Guided Setup and select the **Connect to Impact** link to restart the Automated Registration.

10. Upon successful connection, select **Mark Complete** to continue to verify the connection.


## What to do next

[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/verify-impact-data-connection.md)

-   **[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/verify-impact-data-connection.md)**  
During Impact Guided Setup automated registration, a status is provided to indicate a successful connection. Use the Verify the Connection step to track the progress. If you used manual registration, verify your connection through the Provider Connections page.
-   **[Initiate data migration from IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-migration-idi.md)**  
After the connection is established between your Impact Store Application and the Impact Delivery Instance, next migrate your data.

**Parent Topic:**[Impact Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/guided-setup-impact-in-app.md)

