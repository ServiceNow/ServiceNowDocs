---
title: Use top-down discovery to populate application services
description: Use top-down discovery to populate an application service. This discovery method deploys discovery patterns to find configuration items \(CIs\) belonging to the service and connections between these CIs. Pattern-based discovery creates precise and complete service instances that reliably represent the service-aware view of your organization's IT infrastructure.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a Service instance, Service instances \(Application services\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use top-down discovery to populate application services

Use top-down discovery to populate an application service. This discovery method deploys discovery patterns to find configuration items \(CIs\) belonging to the service and connections between these CIs. Pattern-based discovery creates precise and complete service instances that reliably represent the service-aware view of your organization's IT infrastructure.

## Before you begin

-   Top-Down Discovery is one of several methods for populating an application service with CIs. Choosing a method for populating an application service, is only one step of the generic procedure for creating an application service. Ensure that you have completed the initial steps as described in [Create an application service](../../service-mapping/task/create-it-services.md). The procedure described here is incomplete by itself as it complements that generic procedure.

-   Verify that Service Mapping is set up properly.
-   Ensure you know which entry point to use for this application service and which attributes you must be able to define for this entry point. Learn about Entry point attributes available with Service Mapping.

For information about the different types of application services and the different methods you can use to populate application services, including using top-down discovery, see [Service instances \(Application services\)](../concept/application-services.md).

Role required: sm\_admin

## About this task

A pattern is a sequence of commands designed to detect attributes of a CI and its outbound connections. Service Mapping and Discovery share a set of preconfigured patterns that cover most of the commonly used devices and applications.

Service Mapping starts pattern-based top-down discovery process from the entry point you define.

An entry point is a point where clients access a service instance. Usually, it is either a URL or a combination of the IP address and port. Service Mapping starts the mapping process from this point. For example, to map your electronic mailing service instance, define an IP address or host name of the email server as an entry point.

Entry points vary depending on the nature of the service instance. Service Mapping comes with a wide range of preconfigured entry point types that cover many commonly used applications.

## Procedure

1.  From the **Service Population Method** list in the Choose a Method window, select **Top-Down Discovery**.

2.  From the **Application Type** list, select the CI class of the application that serves as the entry point for this application service.

    Entry point parameters depend on the type you select.

3.  Define attributes for the selected entry point as described in Entry point attributes.

4.  Add free-text comment that may provide useful information for handling this application service later.

5.  Click **Save**.


## What to do next

Complete the generic procedure [Create an application service](../../service-mapping/task/create-it-services.md).

**Related topics**  


[bundle-itom.c_MappingPatternsCustomization]

