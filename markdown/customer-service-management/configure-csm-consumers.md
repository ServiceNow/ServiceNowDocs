---
title: Configure consumers
description: A consumer is a customer in the business-to-consumer \(B2C\) business model.Use Customer Service Management guided setup to import existing consumers.A consumer is a customer in the business-to-consumer \(B2C\) business model. Use the Customer Service Management application to create consumer records.Consumers can have multiple addresses, including one primary address.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure consumers

A consumer is a customer in the business-to-consumer \(B2C\) business model.

## Before you begin

Role required: admin

## About this task

Consumers can have multiple addresses, one of which is the primary address.

## Procedure

-   You can import existing consumers using a guided setup.

-   You can create consumers using the Customer Service Management application.


## Import consumers with guided setup

Use Customer Service Management guided setup to import existing consumers.

### Before you begin

Role required: admin

### About this task

Consumers can have multiple addresses, one of which is the primary address.

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup** and click **Get Started**

2.  In the Foundation Data category, click **Get Started** and then click **Import Consumers \(B2C\)**.

3.  Upload data from an external data source into an import set.

4.  Create a transform map.

5.  Execute the transform map to transfer the data.

6.  Verify that the data records are imported into the target table.


## Create consumers

A consumer is a customer in the business-to-consumer \(B2C\) business model. Use the Customer Service Management application to create consumer records.

### Before you begin

Role required: sn\_customerservice.consumer\_agent, sn\_customerservice\_manager, or admin

### About this task

Consumers can have multiple addresses, one of which is the primary address.

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Consumers**.

2.  Click **New** and fill in the fields on the Consumer form.

3.  Enter the consumer information, such as the name, email address, and phone numbers.

4.  Fill in the fields on the Primary Address tab.

    A consumer can have multiple addresses but only one primary address. The primary address is stored in the Primary Address tab on the Consumer form and in the **Addresses** related list.

5.  Set the desired fields on the Preferences tab.

6.  Click **Submit**.

    The record is added to the Consumers table \(csm\_consumer\). The primary address is added to the **Addresses** related list and the **Primary** field is set to **true**.


### Create additional consumer addresses

Consumers can have multiple addresses, including one primary address.

#### Before you begin

Role required: sn\_customerservice.consumer\_agent, sn\_customerservice\_manager, or admin

#### About this task

The primary address is stored in the Primary Address tab on the Consumer form and in the **Addresses** related list. When you fill in the fields in the Primary Address tab and click **Submit**, this information is added to the **Addresses** related list as the primary address, with the **Primary** field set to true. Any changes made to the **Primary Address** fields are also updated in the related list. A consumer can have only one primary address.

Other addresses, such as billing or shipping addresses, can be created and stored in the **Addresses** related list. For these other addresses, the **Primary** field is set to **false**.

#### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Consumers**.

2.  Click the number of the desired consumer.

3.  In the **Addresses** related list, click **New**.

4.  Fill in the fields on the Location form.

5.  To denote this address as the primary address for the consumer, enable the **Primary** check box.

    A consumer can have multiple addresses but only one primary address.

6.  Click **Submit**.


