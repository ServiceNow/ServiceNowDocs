---
title: View technology risk details in capability map
description: Use the technology risk view of the capability map to know the risk profiles of the technologies that support the business capability.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use capability map for planning, Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# View technology risk details in capability map

Use the technology risk view of the capability map to know the risk profiles of the technologies that support the business capability.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy capability ratings module is moved to the Enterprise Architecture Workspace. To learn more, see [Managing a business portfolio](../concept/manage-business-portfolio.md).

Role required: sn\_apm.apm\_user

## About this task

Enabling the **Technology Risk** view displays the number of underlying technologies of the selected business capability that are at low, medium, and high risks.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Capability Ratings** &gt; **Capability Map**.

2.  Select the **Technology Risk** view.

    The **Technology Risk** view displays the business capabilities \(on the left pane\) with the overall capability risk summary \(on the right pane\). Expand the parent capability to view its sub-capabilities and its associated risk details on the right pane.

    -   **Details**

        The tab shows the number of technologies underlying the selected capability at high, medium, and low risks. Click the capability name to navigate to the Business Capability form and view the record details of the selected capability.

        ![Screenshot showing the technology risk profile of a business capability](../image/BusCapRiskProfile.png "Technology risk profile of a business capability")

    -   **Business Applications**

        You can view the technology risk at a business application level. The risk profile of the business application is stored and retrieved from the Business Application Risk \[sn\_apm\_tpm\_business\_application\_risk\] table.

        ![Business application risk profile](../image/BusAppRiskProfile.png "Business application risk profile")

        -   Click the information icon \(![Information icon](../image/iIcon.png)\) of an application to view the number of capabilities the business application supports and the names of the capabilities.
        -   To view the application record details, click the business application hypertext and navigate to the Business Application form.
        -   Click the view list of related technologies icon \(![View list of related technologies icon](../image/ViewListofRelatedTechnologiesIcon.png)\) to navigate to the Technology Portfolio Management timeline view to view the risk profile of the business application. Filter the applications to take an active measure on the underlying technologies that are at risk.
    -   **Services**

        The tab displays the names of the services that are related to the selected parent business capability on the left pane. You can sort the services in alphabetical or reverse order, search for a service, and view only a selected number of services using the pagination option.

        Click a service hypertext to navigate to the service record form to edit the record. The business capability is related to the service by establishing Provided by::Provides CI relationship.


**Parent Topic:**[Use capability map for planning](view-capability-based-planning.md)

