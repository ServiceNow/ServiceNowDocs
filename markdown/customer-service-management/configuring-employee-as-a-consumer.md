---
title: Configuring a user as a Unified Consumer
description: By creating a unified profile, you can integrate both internal and external personas or consumers in your organization. A user who has a unified profile has synchronized user's login interactions across the Customer Service Management \(CSM\) application.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring a Unified User, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configuring a user as a Unified Consumer

By creating a unified profile, you can integrate both internal and external personas or consumers in your organization. A user who has a unified profile has synchronized user's login interactions across the Customer Service Management \(CSM\) application.

## Overview

Before a unified profile was available, a platform user could only hold either an snc\_internal or an snc\_external role, but not both roles due to role collision issues. Modeling a user as both an employee and a consumer wasn't possible in the past because the sn\_customerservice.consumer role inherited the snc\_external role. The role inheritance that was combined with the platform's behavior to help prevent role collision restricted a user from performing internal duties while that user was also a consumer.

With this new unified user functionality, a single user who is an employee \(snc\_internal\) can also be a business-to-consumer \(B2C\) customer. With a unified profile, your user can switch between different user records and seamlessly transition between roles.

For example, in a financial institution, an individual could be both an employee and a personal account holder. Similarly, in the telecommunications industry, an internal employee might also use company voice services for personal use.

**Note:**

You can activate this functionality by enabling the Customer Service \(com.sn\_customerservice\) plugin.

## Using a query rules framework

You can use the Unified Consumer feature only within the query rules framework. For example, when you update a consumer record, the associated user records synchronize through a business rule **sync\_consumer** to **csm\_consumer\_user** through a business rule. This synchronization occurs only if the associated user class has the **csm\_consumer\_user** record and not any other user record. When you modify the following fields for the consumer user, the associated records also automatically update:

-   First name
-   Middle name
-   Last name
-   Email
-   Mobile phone
-   Business phone
-   Home phone

You can synchronize all types of user records by customizing the business rule to the **sys\_user** record instead of the **csm\_consumer\_user** record.

**Related topics**  


[Roles installed with Employee as a Consumer](../reference/roles-installed-with-employee-as-consumer.md)

[Supported and unsupported roles and features](../reference/features-supp-and-unsupp-by-unified-consumer.md)

[Setting up a user as a Unified Consumer](setting-up-a-user.md)

