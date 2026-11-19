---
title: Prerequisites for configuring CPQ Configurator
description: Verify that you have completed the prerequisites before configuring the ServiceNow CPQ configurator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/guided-setup-prereq.html
release: zurich
topic_type: task
last_updated: "2026-05-30"
reading_time_minutes: 2
breadcrumb: [With guided setup, CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Prerequisites for configuring CPQ Configurator

Verify that you have completed the prerequisites before configuring the ServiceNow CPQ configurator.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Install the following plugins searching by name or ID; if the plugin does not appear in the results, request it from the ServiceNow Store.

    Select a version and **Load demo data** as required.

    -   CSM and FSM Workspace Foundation\(sn\_cwf\_wrkspc\)
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
    -   Customer Service Portal \(sn\_csm\_portal\)
    -   CPQ Integration \(sn\_cpq\_intg\)
    -   CPQ Configurator \(sn\_cpq\_config\)
    -   Contracts and Entitlement Workflows \(sn\_contract\_ent\_wf\)
    -   Sales Quota Application \(sn\_quota\_app\)
    The following are dependent plugins that are installed with the above mentioned plugins. Review and install the plugins if they aren't installed already.

    -   Product Catalog Management Core \(sn\_prd\_pm\) - installed with Price Management, Product Configurator, Product Offering Recommendations
    -   Customer Life Cycle Management Workflows \(sn\_l2c\_cust\_flows\) - installed with Order management and Quote Management Application, Contracts and Entitlement Workflows
    -   Price Management \(sn\_csm\_pricing\) - installed with Product and pricing rules, Sales Cart
    -   Order Management \(sn\_ind\_tmt\_orm\) - installed with Order Management Portal, Order Operations Case Management
    -   CPQ Integration \(sn\_cpq\_intg\) - installed with CPQ Configurator
3.  Gather information regarding your instance.

    1.  Navigate to `https://<service_instance_url>/oauth_entity.do?sys_id=3b119df83b566210a0c0989e53e45a15` for the OAuth Entity record to retrieve the Client ID and Secret.

        **Note:** Replace `<service_instance_url>` with your ServiceNow instance in the URL mentioned above.

    2.  Verify the ServiceNow CPQ Admin UI Application Registry exists with a **ClientID** and **Client secret**.

    3.  Select the lock icon of the **Client secret** field to make it visible.

    4.  Copy the  **Client ID ** and **Client secret** if exists; use them to request a ServiceNow CPQ instance.

4.  Request a ServiceNow CPQ instance using the following the steps.

    1.  Navigate to [Now Support](https://support.servicenow.com/now?id=ns_get_help).

    2.  Select **Create a case**.

    3.  In the ServiceNow Otto panel, select **Create a case**.

    4.  Select **Service request**.

    5.  In the subject field, enter `Request a new CPQ instance` and select **Next**.

    6.  Choose your instance and select **Next**.

        **Note:** Contact Primary Customer Administrator \(PCA\) if your instance is not listed in the instances list.

    7.  Select **Continue**.

    8.  In the **Describe the issue** field, enter the following details.

        -   Client ID and Client Secret fetched from Step 3
        -   Primary Business Contact \(name and email address\)
        -   Instance Owner \(name and email address\)
        -   ServiceNow Instance URL
    9.  Select **Continue**.

    10. Review the summary and select **Confirm and Submit**.


## Result

You will receive an email with the ServiceNow CPQ details. Select the **View request** to access the support portal and set a password.

**Note:** You can proceed with the guided setup only after you receive ServiceNow CPQ details.

## What to do next

[Set up CPQ Configurator using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/configure-cpq-using-guided-setup.md)

