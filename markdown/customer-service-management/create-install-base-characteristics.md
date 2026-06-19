---
title: Create the install base characteristics for an install base item
description: Create a set of configurable characteristics for an install base item on the Customer Service Management \(CSM\) application. You can then view the details about the install base item and the services that are associated to it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/create-install-base-characteristics.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install base characteristics, Install base items, Configure install base, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Create the install base characteristics for an install base item

Create a set of configurable characteristics for an install base item on the Customer Service Management \(CSM\) application. You can then view the details about the install base item and the services that are associated to it.

## Before you begin

Role required: sn\_customerservice\_manager

## About this task

Each product has its own set of attributes, some of which are configurable by the user and some that are non-configurable. Configurable characteristics are a set of characteristics related to an install base item that the user can choose or customize at the time of purchase. These characteristics differ from user to user and product to product. However, non-configurable characteristics are a set of fixed characteristics that are related to an install base item and can't be chosen or customized by the user at the time of purchase. To know more about characteristics, see [Install base characteristics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/attributes-and-configuration-of-install-base-management.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Install Base Items**.

2.  Open an install base item from the list.

3.  Navigate to the Install Base Characteristics related list.

4.  Select **New**.

5.  In the **Characteristic** field, select a characteristic.

    Choose a string type or value for the **Characteristic** field. If the characteristic field has a string type, then the **Value** field appears as shown in the following example.



    \[Omitted image "characteristic-value.png"\] Alt text: Value field that is based on the selected characteristic string.

    If the characteristic field has an option, then the **Characteristic option** field appears as shown in the following example.

    \[Omitted image "characteristic-option.png"\] Alt text: Characteristic option field that is based on the selected characteristic option.

6.  Select **Submit**.


## Result

After creating an install base characteristic, the characteristic appears in the related list on the install base item form.

