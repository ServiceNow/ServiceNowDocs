---
title: Request information about entry points for application services
description: The most important attribute you must know and configure to discover an service instance is an entry point. If you do not know the entry points for the service instance, request this information from the service instance owner.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Map a single application service using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Request information about entry points for application services

The most important attribute you must know and configure to discover an service instance is an entry point. If you do not know the entry points for the service instance, request this information from the service instance owner.

## Before you begin

Requesting information about entry points is an optional part of [mapping a single application service](t_DefineNewBusinessService.md).

Roles required: service\_mapping\_admin

## About this task

An entry point is a point where clients access a service instance. Usually, it is either a URL or a combination of the IP address and port. Service Mapping starts the mapping process from this point. For example, to map your electronic mailing service instance, define an IP address or host name of the email server as an entry point.

Entry points vary depending on the nature of the service instance. Service Mapping comes with a wide range of preconfigured entry point types that cover many commonly used applications.

## Procedure

1.  Click the **Request data** link.

    The Request for data window opens.

2.  If the **Assigned to** list is empty, select the name of the service instance owner.

3.  Enter your questions about this service instance in the **Description** field.

    For example, you can ask what the entry points are.

4.  Click **Submit**.

    The system opens ServiceNow task for the owner and automatically sends an email notification.

5.  Review information added by the owner on the **Other Entry Points** and **Components** tabs.

    Once the owner provides missing information, you receive an email notification.

6.  Click the link in the email to open the Questionnaire screen for the relevant service instance.

7.  Continue [mapping a single application service](t_DefineNewBusinessService.md).


**Parent Topic:**[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

