---
title: Service Owner Workspace integrations
description: Align with other product applications to add value to your Service Owner Workspace monitoring experience.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Service Owner Workspace integrations

Align with other product applications to add value to your Service Owner Workspace monitoring experience.

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](SPM2-premium.md).

## Service Owner Workspace and product alignment

Activate and integrate with these products to expand the functionality of Service Owner Workspace:

-   **Vendor Manager Workspace**

    Activate the Vendor Manager Workspace plugin \(com.snc.vlm.vmw\) to align this workspace data with Service Owner Workspace.

    Manage your vendors from the same workspace interface to effectively gain knowledge of all vendor-related information.

    Monitor and view vendor performance reports from the workspace view.

    Decide what vendor metrics to monitor and manage in workspace view.

    Calculate and view vendor CSAT weight and vendor service offering performance weight.

-   **Financial Management**

    Activate the Service Portfolio Management Estimated Spend plugin \(com.snc.spm.spend\) to view service offering spend, enabling you to select between your local cost model and the cost model provided by the Financial Management application.

    Activate the Financial Management for SPM plugin \(com.snc.financial\_management\_for\_spm\) to provide preconfigured service offering cost models to view in Service Owner Workspace. Select between your local cost model and the Financial Management application model, when used.

-   **Continual Improvement Management \(CIM\)**

    Display existing CIM records in Service Owner Workspace when a service relation is indicated on associated forms.

    Service owners can initiate a CIM record when a performance issue with a service or offering is displayed.

-   **Incident Management — Major Incident Management**

    Activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) to provide a consolidated workbench to view major incidents via the Service Owner Workspace activity stream.


## Integration with Common Service Data Model

Improve your measurement and evaluation by using services and offering references on multiple IT Service Management task forms, including:

-   Problem
-   Change
-   Continual Improvement Management
-   Incident

Directly reference a service offering as the target of a problem, change, or incident for consistency with the Common Service Data Model \(CSDM\). The system filters available offerings based on the service selected.

View and define the service model **Model ID** reference field on the Service and Offering forms to integrate with the CSDM.

When the Service Portfolio Management Premium plugin \(com.snc.spm\) is activated with CSDM is applied, the navigational pane includes the modules **Manage Technical Services** and **Sell and Consume**. Service offerings with associated catalog items are available to view and manage via **Technology Request Catalog** and **Business Request Catalog** within these modules. For complete information about CSDM and how it relates to Service Portfolio Management Premium, refer to [Applying the CSDM guidelines to your product](https://www.servicenow.com/docs/access?context=use-cases&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

