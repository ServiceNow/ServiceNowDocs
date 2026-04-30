---
title: Export data to the FTP server
description: Export a file from a local source, a remote network server, or another instance by providing a path and authentication information.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Perform export steps, Procurement File Transfer Framework, Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Export data to the FTP server

Export a file from a local source, a remote network server, or another instance by providing a path and authentication information.

## Before you begin

You can use Data Source to pull the data from an FTP server. However, you can't use Data Source to post the data to the FTP server.

Role required: admin

## About this task

Integrate your FTP Server to export all the confirmed orders using Flow Designer.

## Procedure

1.  Navigate to **All** &gt; **Procurement Integration** &gt; **Ordering** &gt; **Outbound Orders**.

    A list of outbound orders appears.

    Use the Flow Designer to automate processes of data movement from ServiceNow to third-party applications. Flow Designer lets you move the procurement data between a ServiceNow instance and external applications, data sources, and services.


## Example

You can use Flow Designer subflows to move the data into a mid server and then to external resources. Here is a quick example for processing the **Purchase Order Queue**.

-   Look up for FTP integration record with the supplier ID. For example, **Process Purchase Order Outbound Queue**.
-   Generate Purchase Order payload.
-   Push to Mid server.
-   Wait for duration of time.
-   Push to FTP server.
-   Assign subflow outputs.
-   Add an action, flow logic, or subflow as required.

    **Note:** Based on your business requirements, add additional actions, triggers, or subflows.


**Parent Topic:**[Perform export steps](validate-errors.md)

**Related topics**  


[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Introduction to credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

