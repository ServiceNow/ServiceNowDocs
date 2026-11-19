---
title: Use manual registration to configure the Impact Store Application
description: Manual registration is generally used by advanced users or to obtain configuration support from your Impact Squad. Regulated and GCC customers are also required to use manual registration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/impact/use\_manual\_registration\_configure\_impact\_store\_application.html
release: zurich
topic_type: task
last_updated: "2026-01-07"
reading_time_minutes: 3
breadcrumb: [Impact reference, Impact]
---

# Use manual registration to configure the Impact Store Application

Manual registration is generally used by advanced users or to obtain configuration support from your Impact Squad. Regulated and GCC customers are also required to use manual registration.

## Before you begin

Refer to [Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/configuring-impact-platform.md) for prerequisite configuration steps.

**Important:**

Follow the individual topics for each step of the Impact Guided setup. Manual registration is performed in place of the automated registration step 8, [Use automated registration to connect to the Impact Delivery Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/start-automated-registration-IDI.md).

If the automated registration failed, contact your Impact Squad, as the manual configuration may also fail to complete successfully.

1.  [Install the Impact Store Application from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/install-impact-innovation-lab.md)

    Follow these instructions to install the Impact Store Application.

2.  [Use Guided Setup for Impact Store Application configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/guided-setup-impact-in-app.md)

    Use Impact Guided Setup to follow a sequence of tasks that help you configure the Impact Store Application on your ServiceNow instance.

3.  [Use Guided Setup to onboard users to the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/onboard_users_impact_store_application.md)

    Onboard new and existing users to the Impact Store Application.

4.  [Assign users to Scan Engine groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/assign-users-scan-engine-groups.md)

    In addition to assigning Impact users to groups, the Platform Health users must also be part of a group.

5.  [Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/configure-initial-scan-engine-settings.md)

    Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.

6.  [Run your first scan with the Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/run-scan-engine.md)

    An initial full Scan Engine completion is required to set a baseline from a series of tasks performed that tune the instance environment to complete future scans quickly and efficiently.

7.  [Run the Service Bridge pre-configuration scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/perform_pre_configuration_health_checks_impact_store_app.md)

    Track errors on recent transactions, see connection status, run health checks, and receive recommendations to improve the health of your Impact instance for connection with Service Exchange.


Impact

Role required: admin, any Impact role

## Procedure

1.  Complete steps 1-7 of the Impact Guided setup, as mentioned in the **Before you begin** section.

2.  Complete the manual connection steps:

    1.  [Initiate the connection to the Impact Delivery Instance with manual registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/initiate-the-connection-impact-delivery-instance.md).

    2.  [Use manual registration to establish the connection to the provider instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/connect-instance-impact-store-app.md) with Service Bridge registration

3.  Return to Guided Setup to [Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/verify-impact-data-connection.md)

4.  [Initiate data migration from IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/initiate-migration-idi.md) that migrates data from IDI to the Impact Store Application.


-   **[Initiate the connection to the Impact Delivery Instance with manual registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/initiate-the-connection-impact-delivery-instance.md)**  
Establish a connection between your Impact Store Application and the Impact Delivery Instance to allow the exchange of data.
-   **[Use manual registration to establish the connection to the provider instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/connect-instance-impact-store-app.md)**  
The named contact administrator will establish a secure connection to the Impact Delivery Instance \(provider instance\) using Now Service Exchange to transmit data with the Impact Store Application.

**Parent Topic:**[Impact reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/impact-reference.md)

