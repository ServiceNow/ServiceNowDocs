---
title: Initiate the connection to the Impact Delivery Instance with manual registration
description: Establish a connection between your Impact Store Application and the Impact Delivery Instance to allow the exchange of data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Use manual registration to IDI, Impact reference, Impact]
---

# Initiate the connection to the Impact Delivery Instance with manual registration

Establish a connection between your Impact Store Application and the Impact Delivery Instance to allow the exchange of data.

## Before you begin

**Important:** A named contact administrator must be allocated to perform the installation and implementation of the Impact Store Application. The person initiating registration may not be the named contact administrator.

-   The named contact administrator performs the configuration starting with a registration email sent from the Impact Squad.
-   The registration email contains a direct link to the IDI provider connection form.

Role required: An Impact role

## Procedure

1.  [Install the Impact Store Application from the ServiceNow Store](../task/install-impact-innovation-lab.md).

2.  Log in to the Impact Store Application.

3.  Navigate to **Guided Setup** &gt; **Register your instance** &gt; **Initiate connection to the Impact Delivery Instance**.![Initiate connection to the Impact Delivery Instance in Impact Guided Setup manual registration.](../image/manual-registration-gui.png)

    The login screen for IDI displays to enter IDI credentials.

4.  Log in to the Impact Delivery Instance.

5.  Navigate to **Activity Center** &gt; **Instance registration**.

    The Instance registration page loads.

6.  Select **Add instance**.

    The Initiate instance registration form loads.

7.  Complete the form.

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

Do you have a custom URL?

</td><td>

Custom or vanity URL to the Store App-   No: The URL Impact Store Application auto-populates.
-   Yes:
    -   Navigate to the Impact Store App **All** &gt; **Custom URLs**.
    -   Copy the value from the **Domain Name** column.
    -   Paste the Domain name into the Custom URL field.
**Note:** See the following image for an example. Contact your Impact Squad for assistance.

</td></tr><tr><td>

Contact \(administrator who receives the email to complete setup\)

</td><td>

-   Named contact administrator that is allocated to perform the installation and implementation of the Impact Store Application.
-   Must have Impact roles for both IDI and the Impact Store App


</td></tr></tbody>
</table>    ![Custom URL example in the Domain name table.](../image/custom-url.png)

8.  Select **Initiate registration**.

    The registration information is displayed along with the generated registration link. The details are also emailed to the named contact administrator.


## What to do next

The named contact administrator will [Use manual registration to establish the connection to the provider instance](../task/connect-instance-impact-store-app.md).

**Parent Topic:**[Use manual registration to configure the Impact Store Application](use_manual_registration_configure_impact_store_application.md)

**Previous topic:**[Use manual registration to configure the Impact Store Application](use_manual_registration_configure_impact_store_application.md)

**Next topic:**[Use manual registration to establish the connection to the provider instance](../task/connect-instance-impact-store-app.md)

