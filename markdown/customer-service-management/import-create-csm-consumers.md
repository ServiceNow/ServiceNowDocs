---
title: Create consumers
description: A consumer is a customer in the business-to-consumer \(B2C\) business model. Use the Customer Service Management application to create consumer records.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure consumers, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Create consumers

A consumer is a customer in the business-to-consumer \(B2C\) business model. Use the Customer Service Management application to create consumer records.

## Before you begin

Role required: One of the following roles:

-   sn\_crm\_consumer\_data\_manager
-   sn\_crm\_consumer\_relationship\_data\_manager
-   sn\_crm\_foundation\_data\_manager
-   sn\_crm\_foundation\_admin
-   sn\_customerservice.consumer\_agent
-   sn\_customerservice\_manager
-   admin

## About this task

Consumers can have multiple addresses, one of which is the primary address.

**Note:** Note: Creating a consumer record is only one part of setting up a consumer persona. The user must also be assigned a consumer role \(sn\_customerservice.consumer or sn\_customerservice.unified\_consumer\) to access consumer functionality. Without both the consumer record and the role, you can't perform consumer activities such as viewing cases, sold products, or install base items.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Consumers**.

2.  Select **New** and fill in the fields on the Consumer form.

3.  Enter the consumer information, such as the name, email address, and phone numbers.

4.  Fill in the fields on the Primary Address tab.

    A consumer can have multiple addresses but only one primary address. The primary address is stored in the Primary Address tab of the consumer form within the Addresses related list.

5.  Set the desired fields on the Preferences tab.

6.  Select **Submit**.

    The record is added to the Consumers table \(csm\_consumer\). The primary address is added to the **Addresses** related list and the **Primary** field is set to **true**.


