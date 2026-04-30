---
title: Software Asset Management software suites
description: Software Suites is a way for a software publisher to group related applications as a set.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software Asset Management software suites

Software Suites is a way for a software publisher to group related applications as a set.

## Overview of software suites

Create a suite and add components to the suite so that your organizations' rights are correctly counted during reconciliation.

An example for client software suites is the Microsoft Office suite, which comprises Word, Excel, PowerPoint, Outlook, and Access. Microsoft Office is considered the suite parent and the suite components are the suite children.

A more complex example is the “suite of suites” which is common in server software. Microsoft Core Infrastructure Server \(CIS\) Suite has two suite components: Windows Server and System Center \(which is also a suite\).

Suite components are licensed together using a suite license rather than each software component needing an individual license. Therefore, an entitlement for the suite parent licenses all suite components including suite children that are also suites themselves.

For software subscriptions, only one user subscription suite license is required for each user. For example, the Microsoft 365 suite includes the following components: Office 365, EMS \(Enterprise Mobility plus Security\), and Windows 10. One Microsoft 365 license entitles a user to use one or more of the components.

Software Suites \[cmdb\_m2m\_suite\_model\] table captures the relationship between a suite parent and a suite child.

For any software model, you can specify whether the model is a suite \(parent\) or a component \(child\). A software model can be a component in multiple suites. For example, Microsoft Word is a component in two suites: Microsoft Office Standard and Microsoft Office Professional. Although you can set a single software model as both a suite and a component, software isn’t typically sold as nested suites.

Suite information such as **Suite Components** and **Suite Parents** are found as tabs in the Software Model form. Whenever a software model is automatically created as part of a scheduled job, its child components are automatically created and appear in the [Suite Components](../reference/software-model-fields.md#section_bdp_kmc_xhb) tab in the software model form.

## Predefined suites

The Software Asset Management content library contains predefined suites to simplify your user experience. If suite content exists for a product, the suite information automatically populates the **Suite Components** tab in the Software Model from. Updates to the suite content are downloaded and existing suite definitions are updated via scheduled jobs.

## Allocations

Allocations are used to apply a license to a device or user. In the context of suites, allocations enable the software asset manager to apply an individual component license to a user/device instead of the suite license.

## Use case for allocations

An organization has both Microsoft 365 E5 \(suite\) entitlements as well as Windows 10 entitlements. User A has Windows 10, Word, Excel, and other components of Office 365 installed on their device. User A is allocated the Windows 10 entitlement. User A’s Windows 10 installation is licensed with the Windows 10 entitlement rather than the Microsoft 365 suite entitlement while the remaining components is licensed as part of the Microsoft 365 suite.

## Discovery maps

Discovery Maps \(DMAPs\) are variations of the software as predefined in the SAMP content library. Although a software model can be defined manually by setting the Publisher, Product, Version, Edition, the best approach is using DMAPs whenever possible. The DMAPs associate the relevant content with the Software Model automatically like the suite relationships, downgrade models, lifecycle, and next version.

## Hybrid and subscription software suites

Software Asset Management supports hybrid and subscription-based software suites. In a hybrid software suite, either the suite parent or child component is subscription-based. In a subscription-based software suite, both the suite parent and child component are subscription-based. The license that you use to determine compliance depends on whether the suite parent and child component are subscription-based:

-   If only the suite parent is subscription-based, then all the child component installations are inferred as part of the suite parent. You can determine your license compliance using the suite parent license.
-   If only the child component of a suite parent is subscription-based, then the instances of that child component aren’t inferred as part of the suite parent. You can determine your license compliance using the child component license.
-   If both the suite parent and child components are subscription-based, then the instances of the child components are inferred as part of the suite parent. You can determine your license compliance using the suite parent license. For example, Microsoft 365 E5 is a subscription-based software suite that includes the Office 365 E5, EMS E5, and Windows 10 subscription software. Since both the suite parent and child components are subscription-based, they’re reconciled against the Microsoft 365 E5 parent license.

-   **[Software suites inference](software-suites-inference.md)**  
Suite inference is used to determine whether the software is part of a suite and to infer the best or efficient suite to use when licensing.
-   **[Managing software suites](Manage-software-suites.md)**  
Simplify licensing and lower the cost of licenses from vendors. Get visibility into your complex suite licenses, manage compliance, and optimize your spending on these licenses.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

