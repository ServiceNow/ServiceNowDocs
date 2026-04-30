---
title: Install ERP Data Hub
description: Install the ERP Data Hub \(Enterprise Resource Planning\) application \(sn\_erp\_integration\) if you have the admin role from the ServiceNow Store.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring ERP Data Hub, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Install ERP Data Hub

Install the ERP Data Hub \(Enterprise Resource Planning\) application \(sn\_erp\_integration\) if you have the admin role from the ServiceNow Store.

## Before you begin

For a complete list of prerequisites for installing ERP Data Hub, including licensing information, see [Requirements for installing ERP Data Hub](../reference/erpc-prereqs-for-installation.md).

Role required: admin

## Procedure

1.  Go to the [ServiceNow Store](https://store.servicenow.com).

2.  In search type, `ERP Data Hub`.

3.  Select the **ERP Data Hub** tile.

4.  Select **Get**.

5.  Log in using your ServiceNow credentials.

    Federal customers should select **Are you a federal customer?** and follow the instructions. If you don't have ServiceNow credentials and aren't a federal customer, select **Are you a customer who doesn't have ServiceNow ID?** and follow the instructions.

6.  Check that you have entitlements \(or licenses\) to the product and dependent applications by viewing **Your Subscription Status**.

7.  Select **Request Install**.

    When complete, confirm the installation of ERP Data Hub and select **Close** to return to the ServiceNow Store.


## What to do next

After you install ERP Data Hub, you must enable the **sn\_erp\_integration.enableModelModification** property so users can customize ERP models. After you enable the **sn\_erp\_integration.enableModelModification** property, ERP Data Hub retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.System properties are maintained in the System Property table \[sys\_properties\], which you can access using the module navigator, or by directly typing `sys_properties.list` in the Navigator Filter.

**Parent Topic:**[Configuring ERP Data Hub](../concept/erp-integration-configuration-overview.md)

