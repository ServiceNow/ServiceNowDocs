---
title: Create a service set
description: Create your service set \(department\) name in the Universal Request \(UR\) application to use the UR capabilities for a specific service set in your organization. Service sets are the various departments in your organization.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Create a service set

Create your service set \(department\) name in the Universal Request \(UR\) application to use the UR capabilities for a specific service set in your organization. Service sets are the various departments in your organization.

## Before you begin

Role required: admin

Your organisation must have one service set without any services that is marked as a Universal Set. The Universal Set acts as the default department that receives new Universal Requests that are not routed to a specific department. This service set makes sure that when a UR is created it is assigned to the assignment group of the service set under one of the following conditions.

-   A UR is created from Request Help with no department selected. For example, when an employee creates a UR from Request Help with no department selected and when the automatic assignment is not suggested by the ML routing algorithm, then the UR is assigned to the Service Set that is marked as Universal Set.
-   When a UR is transferred with the **I'm not sure** option. For example, when a UR is transferred by a department agent, and the agent is unsure of the department to transfer the request to, the agent can select **I’m not sure** in the department field. In this case, the UR is routed to the Service Set that is marked as the Universal Set.

**Note:** You can have only one service set marked as a Universal Set for your organization.

## Procedure

1.  Navigate to **All** &gt; **Universal Request** &gt; **Administration** &gt; **Service Sets**.

2.  Click **New**.

3.  Enter your service specific department name.

4.  Select the **Universal Set** check box.

    If this check box is selected, the new service set is considered as a Universal Set.

5.  Select the **Mapping Configuration** that you want to define for your service set.

6.  Click **Submit**.


**Parent Topic:**[Configure service to use Universal Request](../concept/config-service-for-ur.md)

