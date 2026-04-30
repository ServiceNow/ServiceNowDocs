---
title: Initiate the connection to the Impact Delivery Instance
description: Connect between your Impact Store Application with the Impact Delivery Instance to exchange data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configuring the Impact Store Application, Impact Store Application, Impact]
---

# Initiate the connection to the Impact Delivery Instance

Connect between your Impact Store Application with the Impact Delivery Instance to exchange data.

## Before you begin

**Important:** A named contact administrator must be allocated to perform the installation and implementation of the Impact Store Application. The person initiating registration may not be the named contact administrator.

-   The named contact administrator must have an Impact role for both the Impact Store Application and the Impact Delivery Instance to configure the integration of data.
-   The named contact administrator performs the configuration starting with a registration email sent from the Impact Squad.
-   The registration email contains a direct link to the IDI provider connection form.

Role required: An Impact role

## Procedure

1.  [Install the Impact Store Application from the ServiceNow Store](install-impact-innovation-lab.md).

2.  Log in to the Impact Delivery Instance to initiate the Impact Store Application instance registration.

3.  Navigate to **Activity Center** &gt; **Instance registration**.

4.  Select **Add instance**.

    The Initiate instance registration page loads.

5.  Complete the form.

<table id="table_rp1_tj2_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Instance type

</td><td>

Production or non-production

</td></tr><tr><td>

Instance to register

</td><td>

Name of the instance to be registered

</td></tr><tr><td>

Impact Store Application instance

</td><td>

URL to the Impact Store Application**Note:** The URL should auto-populate, otherwise, contact your Impact Squad for assistance.

</td></tr><tr><td>

Contact \(administrator who receives the email to complete setup\)

</td><td>

-   Named contact administrator that is allocated to perform the installation and implementation of the Impact Store Application.
-   Must have Impact roles for both IDI and the Impact Store App


</td></tr></tbody>
</table>6.  Select **Initiate registration**.

    The registration information is displayed along with the generated registration link. The details are also emailed to the named contact administrator.


## What to do next

The named contact administrator will [Connect to the provider instance](../task/connect-instance-impact-store-app.md).

