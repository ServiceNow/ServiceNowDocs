---
title: Install Zero Copy Connector for ERP
description: Install the Zero Copy Connector for ERP \(Enterprise Resource Planning\) application \(sn\_erp\_integration\) from the ServiceNow Store.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, install, store]
breadcrumb: [Configure, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Install Zero Copy Connector for ERP

Install the Zero Copy Connector for ERP \(Enterprise Resource Planning\) application \(sn\_erp\_integration\) from the ServiceNow Store.

## Before you begin

For a complete list of prerequisites for installing Zero Copy Connector for ERP, including licensing information, see [Requirements for installing Zero Copy Connector for ERP](../reference/erpc-prereqs-for-installation.md).

Role required: admin

## Procedure

1.  Go to the [ServiceNow Store](https://store.servicenow.com).

2.  In search enter, `Zero Copy Connector for ERP`.

3.  Select the **Zero Copy Connector for ERP** tile.

4.  Select **Buy**.

5.  Log in using your ServiceNow credentials.

    Federal customers should select **Are you a federal customer?** and follow the instructions. If you don't have ServiceNow credentials and aren't a federal customer, select **Are you a customer who doesn't have ServiceNow ID?** and follow the instructions.

6.  Check that you have entitlements \(or licenses\) to the product and dependent applications by viewing **Your Subscription Status**.

7.  Select **Request Install**.

8.  When complete, confirm the installation of Zero Copy Connector for ERP.

9.  Select **Close** to return to the ServiceNow Store


## What to do next

An admin or a user with the sn\_erp\_integration.erp\_admin role must enable the **sn\_erp\_integration.enableModelModification** property for you to edit, customize, and clone ERP models and tables. The property must be enabled on the correct scope.After enabling the property, Zero Copy Connector for ERP retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.The property must be configured for either a non-production or production state. \(Enabling the property on a production instance can create metadata records when new models and fields are added in Zero Copy Connector for ERP.\) System properties are maintained in the System Property table \[sys\_properties\], which you can access by entering `sys_properties.list` directly in the Navigator Filter.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](../concept/erp-integration-configuration-overview.md)

