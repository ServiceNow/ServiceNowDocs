---
title: Connect a digital interface with CMDB API in Enterprise Architecture
description: Create a relationship between a digital interface and a CMDB API. Use this relationship to find out the digital integration and API connection details and view the APIs that are created from the design specs of the digital interface. You can also find out the environments where the APIs are deployed, and group them as required.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Connect a digital interface with CMDB API in Enterprise Architecture

Create a relationship between a digital interface and a CMDB API. Use this relationship to find out the digital integration and API connection details and view the APIs that are created from the design specs of the digital interface. You can also find out the environments where the APIs are deployed, and group them as required.

## Before you begin

Activate the CMDB CI Class Models \[app-cmdb-content\] store app \(version 1.49.0 or later\). For instructions, see [CMDB CI Class Models app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Role required: sn\_apm.apm\_analyst

## About this task

One digital interface can be connected to one or more APIs. One API can be connected to only one digital interface.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio** &gt; **Digital Interfaces**.

2.  Select an existing digital interface.

3.  Select the **APIs** tab in the digital interface form.

4.  Select **New**.

    On the Digital Interface to API form, fill in the fields. For field descriptions, see [Digital interface to API form in Enterprise Architecture \(formerly APM\)](../reference/apm-dig-interface-api-form.md). Information for the fields Environment, Lifecycle Stage, and Lifecycle Stage Status are derived from the API.

5.  Select **Save**.


**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

