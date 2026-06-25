---
title: Connect a digital interface with the CMDB API in the EA Workspace
description: Create a relationship between a digital interface and a CMDB API. The relationship helps you find out which digital integration uses which API, which APIs are built out of the design specs of the digital interface, and what environments are deployed. The relationship helps to group the deployed APIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-relate-dig-interface-api.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with digital interfaces, Working with digital integration management in Enterprise Architecture Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Connect a digital interface with the CMDB API in the EA Workspace

Create a relationship between a digital interface and a CMDB API. The relationship helps you find out which digital integration uses which API, which APIs are built out of the design specs of the digital interface, and what environments are deployed. The relationship helps to group the deployed APIs.

## Before you begin

Activate the CMDB CI Class Models \[app-cmdb-content\] store app \(version 1.49.0 or later\). For instructions, see [CMDB CI Class Models app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models.md).

Role required: sn\_apm.apm\_analyst

## About this task

One digital interface can be connected to one or more APIs. One API can be connected to only one digital interface.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  In the left navigation, open the Portfolio List view by selecting the Portfolio icon \(\[Omitted image "portfolio-icon.png"\] Alt text: Portfolio icon\).

3.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon\) next to **Application Portfolio**.

4.  Select **Digital Interfaces**.

5.  Select an existing digital interface.

6.  Select the **APIs** tab.

7.  Select **New**.

8.  On the Digital Interface to API form, fill in the fields.

    For field descriptions, see [Digital interface to API form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-dig-interface-api-form.md). Information for the fields Environment, Lifecycle Stage, and Lifecycle Stage Status are derived from the API. \[Omitted image "eaw-dig-interface-to-api.png"\] Alt text: Connect digital interface to API

9.  Select **Save**.


**Parent Topic:**[Working with digital interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-work-with-digital-interfaces.md)

**Related topics**  


[View all digital interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-view-all-dig-interfaces.md)

[Relate an SDLC component to a digital interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-dig-interface-add-sdlc-comp.md)

[Manage architectural artifacts of a digital interface in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-artifacts-digital-interface.md)

[Add or edit a digital interface in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-digital-interface.md)

[Relate credentials to a digital interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-dig-interface-add-credential.md)

[Relate an information object to a digital interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-dig-interface-add-info-object.md)

