---
title: Request an instance
description: Request the provisioning of a new Amazon EC2 instance through the service catalog.
locale: en-US
release: zurich
product: Self-service
classification: self-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Amazon EC2 instance request from the Service Catalog, Service catalog requests, Exploring Self-service, Self-service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Request an instance

Request the provisioning of a new Amazon EC2 instance through the service catalog.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Select **Amazon EC2 Instance** from the **Request Application Infrastructure** category.

    ![EC2 service catalog 2](../image/EC2ServiceCatalog2.png "EC2 Service Catalog 2")

3.  Select the operating system, the type of instance \(Large or Small\), and the number of instances requested.

    See the specifications for Large and Small instances in Amazon EC2 Instance Types.

4.  Type a reason for the request.

    ![EC2 service catalog](../image/EC2ServiceCatalog.png "EC2 Service Catalog")

5.  Click **Order Now** to order the instance.

    The Order Status form appears, summarizing the request. A status bar tracks the progress of the approval and provisioning of the EC2 instance.

    ![EC2 order status](../image/EC2OrderStatus.png "EC2 Order Status")

    Upon successful creation of the instance, you receive an email containing the instance ID, IP address, and the public DNS for the instances created.


**Parent Topic:**[Amazon EC2 instance request from the Service Catalog](../concept/c_AmazonEC2InstanceRequest.md)

