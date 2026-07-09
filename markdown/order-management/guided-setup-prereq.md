---
title: Prerequisites for configuring CPQ Configurator
description: Verify that you have completed the prerequisites before configuring the ServiceNow CPQ configurator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/guided-setup-prereq.html
release: zurich
topic_type: task
last_updated: "2026-05-30"
reading_time_minutes: 1
breadcrumb: [With guided setup, CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Prerequisites for configuring CPQ Configurator

Verify that you have completed the prerequisites before configuring the ServiceNow CPQ configurator.

## Before you begin

Role required: admin

## Procedure

1.  Install the required plugins by following the steps mentioned below.

    The required plugins are:

    -   CSM and FSM Configurable Workspace Foundation\(sn\_cwf\_wrkspc\)
    -   Order Management \(sn\_ind\_tmt\_orm\)
    -   Product Catalog Management Core \(sn\_prd\_pm\)
    -   Price Management \(sn\_csm\_pricing\)
    -   Quote Management Application \(sn\_quote\_mgmt\)
    -   Product Configurator \(sn\_prd\_config\_ui\)
    -   Customer Life Cycle Management Workflows \(sn\_l2c\_cust\_flows\)
    -   Product and pricing rules \(sn\_csm\_price\_mtrx\)
    -   Opportunity Management Application \(sn\_opty\_mgmt\)
    -   Product Offering Recommendations \(sn\_prd\_pm\_ra\)
    -   Order Management Portal \(sn\_ord\_mgmt\_portal\)
    -   Order Operations Case Management \(sn\_order\_case\)
    -   Case Management for Invoice Operations \(sn\_csm\_invoice\)
    -   Sales Cart \(sn\_sales\_cart\)
    -   Customer Life Cycle Managment Self Service \(sn\_clm\_selfservice\)
    -   Contracts and Entitlement Workflows \(sn\_contract\_ent\_wf\)
    -   Sales Quota Application \(sn\_quota\_app\)
    -   Customer Service Portal \(sn\_csm\_portal\)
    -   CPQ Integration \(sn\_cpq\_intg\)
    -   CPQ Configurator \(sn\_cpq\_config\)
    1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

    2.  Find the plugin using the filter criteria and search bar.

        Search by name or ID. If the application does not appear in the results, request it from the ServiceNow Store.

    3.  Select a version from the list.

    4.  Select the **Load demo data** check box.

    5.  Select **Install**.

2.  View the Client ID and Client secret in your instance.

    1.  Navigate to `https://<service_instance_url>/oauth_entity.do?sys_id=3b119df83b566210a0c0989e53e45a15`

        **Note:** Replace `<service_instance_url>` with your ServiceNow instance in the URL mentioned above.

    2.  Check that the Logik.AI Admin UI Application Registry exists with a ClientID and Client secret.

        This information is required in the following step.

3.  Request a ServiceNow CPQ instance by completing the following the step.

    1.  Navigate to [Now Support](https://support.servicenow.com/now?id=ns_get_help).

    2.  Select **Create a case**.

    3.  In the Now Assist chat, select the option to open a case form.

    4.  Select **Service request**.

    5.  Enter `Request a new CPQ instance` and select **Next**.

    6.  Select your instance and select **Next**.

        **Note:** Contact PCA if your instance in not listed in the instances list.

    7.  Select **Continue**.

    8.  Enter the Client ID and Client secret fetched from Step 2.

    9.  Select **Continue**.

    10. Review the summary and select **Confirm and Submit**


## Result

You will receive an email with the Logik Tenant details. Select the **View request** to access the support portal and set a password.

**Note:** You can proceed with the guided setup only after you receive Logik Tenant details. For more information see, [Set up CPQ Configurator using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/configure-cpq-using-guided-setup.md).

