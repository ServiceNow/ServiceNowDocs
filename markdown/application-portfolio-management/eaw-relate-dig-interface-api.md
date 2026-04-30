---
title: Connect a digital interface with the CMDB API in the EA Workspace
description: Create a relationship between a digital interface and a CMDB API. The relationship helps you find out which digital integration uses which API, which APIs are built out of the design specs of the digital interface, and what environments are deployed. The relationship helps to group the deployed APIs.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Digital interfaces in Enterprise Architecture Workspace, Working with an application portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Connect a digital interface with the CMDB API in the EA Workspace

Create a relationship between a digital interface and a CMDB API. The relationship helps you find out which digital integration uses which API, which APIs are built out of the design specs of the digital interface, and what environments are deployed. The relationship helps to group the deployed APIs.

## Before you begin

Activate the CMDB CI Class Models \[app-cmdb-content\] store app \(version 1.49.0 or later\). For instructions, see [CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Role required: sn\_apm.apm\_analyst

## About this task

One digital interface can be connected to one or more APIs. One API can be connected to only one digital interface.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  In the left navigation, open the Portfolio List view by selecting the Portfolio icon \(![Portfolio icon](../../image/portfolio-icon.png)\).

3.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Application Portfolio**.

4.  Select **Digital Interfaces**.

5.  Select an existing digital interface.

6.  Select the **APIs** tab.

7.  Select **New**.

8.  On the Digital Interface to API form, fill in the fields.

    For field descriptions, see [Digital interface to API form](../../reference/eaw-reference/eaw-dig-interface-api-form.md). Information for the fields Environment, Lifecycle Stage, and Lifecycle Stage Status are derived from the API. ![Connect digital interface to API](../../image/eaw-image/eaw-dig-interface-to-api.png)

9.  Select **Save**.


**Parent Topic:**[Digital interfaces in Enterprise Architecture Workspace](../../concept/eaw-concept/eaw-digital-interface.md)

