---
title: Set up a software model for the Microsoft Endpoint Configuration Manager application
description: Using the applications discovered on the Microsoft Endpoint Configuration Manager server, set up a software model to manage licenses.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Microsoft Endpoint Configuration Manager, Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a software model for the Microsoft Endpoint Configuration Manager application

Using the applications discovered on the Microsoft Endpoint Configuration Manager server, set up a software model to manage licenses.

## Before you begin

Role required:

**Note:** Ensure that the user has one of the two mentioned set of roles.

-   sn\_ms\_epcfgmgr\_spk.Microsoft Endpoint Manager Admin and sn\_csd.CSD Admin
-   admin

Before creating software models, you must discover the applications available for deployment on the Microsoft Endpoint Configuration Manager server. See [CSD 2.0 for Microsoft Endpoint Configuration Manager](../concept/csd2.md) for more information.

## About this task

You can link a Microsoft Endpoint Configuration Manager application to an existing software model or create a new model.

## Procedure

1.  Navigate to **Microsoft Endpoint Configuration Manager** &gt; **Applications**.

    A list of applications discovered on the Microsoft Endpoint Configuration Manager server appears.

2.  Open an application record.

3.  To link to an existing model, click the magnifying glass icon in the **CSD software model** field and select a model from the list.

4.  To create a model, click **Create Software Model** under related link.

    1.  Complete the software model fields.

    2.  Click **Submit**.

        The view returns to the Microsoft Endpoint Configuration Manager Applications list.


**Parent Topic:**[CSD 2.0 for Microsoft Endpoint Configuration Manager](../concept/csd2.md)

