---
title: Install Zero Copy Connector for ERP
description: Install the Zero Copy Connector for ERP \(Enterprise Resource Planning\) application \(sn\_erp\_integration\) if you have the admin role from the ServiceNow Store.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Zero Copy Connector for ERP, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Install Zero Copy Connector for ERP

Install the Zero Copy Connector for ERP \(Enterprise Resource Planning\) application \(sn\_erp\_integration\) if you have the admin role from the ServiceNow Store.

## Before you begin

For a complete list of prerequisites for installing Zero Copy Connector for ERP, including licensing information, see [Requirements for installing Zero Copy Connector for ERP](../reference/erpc-prereqs-for-installation.md).

Role required: admin

## Procedure

1.  Go to the [ServiceNow Store](https://store.servicenow.com).

2.  In search type, `ERP Canvas`.

3.  Select the **ERP Canvas** tile.

4.  Select **Get**.

5.  Log in using your ServiceNow credentials.

    Federal customers should select **Are you a federal customer?** and follow the instructions. If you don't have ServiceNow credentials and aren't a federal customer, select **Are you a customer who doesn't have ServiceNow ID?** and follow the instructions.

6.  Check that you have entitlements \(or licenses\) to the product and dependent applications by viewing **Your Subscription Status**.

7.  Select **Request Install**.

    When complete, confirm the installation of Zero Copy Connector for ERP and select **Close** to return to the ServiceNow Store.


## What to do next

After installing Zero Copy Connector for ERP, an admin or a user with the sn\_erp\_integration.erp\_admin role must enable the **sn\_erp\_integration.enableModelModification** property so users can customize ERP models. After enabling the **sn\_erp\_integration.enableModelModification** property, Zero Copy Connector for ERP retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.System properties are maintained in the System Property table \[sys\_properties\], which you can access using the module navigator, or by directly typing `sys_properties.list` in the Navigator Filter.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](../concept/erp-integration-configuration-overview.md)

