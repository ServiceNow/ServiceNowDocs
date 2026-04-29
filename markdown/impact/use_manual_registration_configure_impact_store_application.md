---
title: Use manual registration to configure the Impact Store Application
description: Manual registration is generally used by advanced users or to obtain configuration support from your Impact Squad. Regulated and GCC customers are also required to use manual registration.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Impact reference, Impact]
---

# Use manual registration to configure the Impact Store Application

Manual registration is generally used by advanced users or to obtain configuration support from your Impact Squad. Regulated and GCC customers are also required to use manual registration.

## Before you begin

Refer to [Configure the Impact Store Application](configuring-impact-platform.md) for prerequisite configuration steps.

**Important:**

Follow the individual topics for each step of the Impact Guided setup. Manual registration is performed in place of the automated registration step 8, [Use automated registration to connect to the Impact Delivery Instance](../task/start-automated-registration-IDI.md).

If the automated registration failed, contact your Impact Squad, as the manual configuration may also fail to complete successfully.

1.  [Install the Impact Store Application from the ServiceNow Store](https://www.servicenow.com/docs/bundle/zurich-impact/page/product/impact/task/install-impact-innovation-lab.html)

    Follow these instructions to install the Impact Store Application.

2.  [Use Guided Setup for Impact Store Application configuration](https://www.servicenow.com/docs/bundle/zurich-impact/page/product/impact/task/guided-setup-impact-in-app.html)

    Use Impact Guided Setup to follow a sequence of tasks that help you configure the Impact Store Application on your ServiceNow instance.

3.  [Use Guided Setup to onboard users to the Impact Store Application](https://www.servicenow.com/docs/bundle/zurich-impact/page/product/impact/task/onboard_users_impact_store_application.html)

    Onboard new and existing users to the Impact Store Application.

4.  [Assign users to Scan Engine groups](https://www.servicenow.com/docs/bundle/zurich-impact/page/product/impact/task/assign-users-scan-engine-groups.html)

    In addition to assigning Impact users to groups, the Platform Health users must also be part of a group.

5.  [Activate Scan Engine and review settings](https://www.servicenow.com/docs/bundle/zurich-impact/page/product/impact/task/configure-initial-scan-engine-settings.html)

    Use Impact Guided Setup to set up the minimum required configuration options in order to run the first system scan.

6.  [Run your first scan with the Scan Engine](https://www.servicenow.com/docs/bundle/zurich-impact/page/product/impact/task/run-scan-engine.html)

    An initial full Scan Engine completion is required to set a baseline from a series of tasks performed that tune the instance environment to complete future scans quickly and efficiently.


Impact

Role required: admin, any Impact role

## Procedure

1.  Complete pre-requisite steps of the Impact Guided setup, as mentioned in the **Before you begin** section.

2.  Complete the manual connection steps:

    1.  [Initiate the connection to the Impact Delivery Instance with manual registration](initiate-the-connection-impact-delivery-instance.md).

    2.  [Use manual registration to establish the connection to the provider instance](../task/connect-instance-impact-store-app.md) with Service Bridge registration

3.  Return to Guided Setup to [Verify Impact data connection](../task/verify-impact-data-connection.md)

4.  [Initiate data migration from IDI](../task/initiate-migration-idi.md) that migrates data from IDI to the Impact Store Application.


1.  [Initiate the connection to the Impact Delivery Instance with manual registration](initiate-the-connection-impact-delivery-instance.md)  
Establish a connection between your Impact Store Application and the Impact Delivery Instance to allow the exchange of data.
2.  [Use manual registration to establish the connection to the provider instance](../task/connect-instance-impact-store-app.md)  
The named contact administrator will establish a secure connection to the Impact Delivery Instance \(provider instance\) to transmit data with the Impact Store Application.

**Parent Topic:**[Impact reference](../reference/impact-reference.md)

