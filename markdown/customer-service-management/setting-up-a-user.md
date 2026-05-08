---
title: Setting up a user as a Unified Consumer
description: Set up a user as a Unified Consumer by creating a single, unified profile that supports both the internal and external personas in the Customer Service Management \(CSM\) application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring a user as a Unified Consumer, Configuring a Unified User, User management, Set up your environment, Configure, Customer Service Management]
---

# Setting up a user as a Unified Consumer

Set up a user as a Unified Consumer by creating a single, unified profile that supports both the internal and external personas in the Customer Service Management \(CSM\) application.

## Overview of Unified Consumer

You can model a single user both as an employee \(snc\_internal\) and a business-to-consumer \(B2C customer\) by creating a unified profile. By unifying multiple profiles for a single user in the Customer Service Management \(CSM\) application, you don't need to create and manage multiple user accounts for that user.

**Note:** You can also configure an external Unified Consumer, who lacks an internal \(snc\_internal\) role and isn’t an employee, by using similar setup tasks.

The following table describes how to set up the tasks for activating a Unified Consumer.

|Task|Description|
|----|-----------|
|Activate a Unified Consumer|Activate a Unified Consumer by updating the ConsumerImpl script include to display other sys\_user records in the reference list for the csm\_consumer table. For more information, see [Activate a Unified Consumer](../task/activate-unified-consumer.md).|
|Create a consumer record|Create a consumer record with the user, designating that user as a consumer. For more information, see [Create a consumer record](../task/create-a-consumer-record.md).|
|Assign a role to a user|Assign the Unified Consumer \(sn\_customerservice.unified\_consumer\) role to the user. For more information, see Assign a role to a user.|
|Associate an existing user with a consumer record|Associate a Unified Consumer user with a consumer record by creating a consumer user and then linking the user with a consumer record. For more information, see [Associate an existing user to a consumer record](associating-users-to-a-consumer-record.md#).|

**Note:** Both a consumer record and the Unified Consumer role are required for consumer functionality. Create the consumer record before assigning the role. If the role is assigned without a linked consumer record, the user cannot perform consumer activities and may experience unexpected behavior. If the consumer record exists but the role is missing, the user cannot access consumer features such as cases, sold products, or install base items.

**Related topics**  


[Configuring a user as a Unified Consumer](configuring-employee-as-a-consumer.md)

[Roles installed with Employee as a Consumer](../reference/roles-installed-with-employee-as-consumer.md)

[Supported and unsupported roles and features](../reference/features-supp-and-unsupp-by-unified-consumer.md)

