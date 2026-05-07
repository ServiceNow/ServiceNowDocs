---
title: Customize scripted extension points
description: Customize how license expiration dates for Fortinet devices are stored on CIs by implementing scripted extension points.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [extension points scripted fortinet license]
breadcrumb: [Configure Fortinet SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Customize scripted extension points

Customize how license expiration dates for Fortinet devices are stored on CIs by implementing scripted extension points.

## Before you begin

Role required: tsom\_visibility\_admin

Service Graph Connector for Fortinet is installed. For instructions, see [Configure a Fortinet SD-WAN Service Graph Connector](../concept/configure-fortinet-service-graph-connector.md).

## About this task

By default, Fortinet SGC stores license expiration dates as separate CI attributes for each device, using the naming convention `license_expiration_date_*SERVICE\_CODE*`. You can customize this behavior using scripted extension points to implement alternative storage logic, such as storing only the earliest expiration date across all devices.

## Procedure

1.  Navigate to **All** &gt; **System Scripted Extension Points** &gt; **Scripted Extension Points**.

2.  Search for Fortinet in the **Extension Points** search box.

3.  Select **sn\_gnc\_fortinet.FortinetCustomizedContractParsing** from the **API Name** search results list.![Scripted Extension Points page showing FortinetCustomizedContractParsing in the API Name list](../images/fortinet-extension-points.png)

4.  Select **Create implementation**, which is located under **Related Links**.

5.  Implement your custom logic in the provided method.

    The input is the contract items returned by the FortiManager API, which contains the license data for all devices. Your implementation should return the attributes you want to store on the CI.

    ![Contract items parsing implementation interface](../images/contract-items-parsing.png)

6.  Set the **Order** field to a value less than `100`.

    The default implementation has an order of 100; implementations with a lower order number execute first and take precedence.

7.  Select **Update** to save.


