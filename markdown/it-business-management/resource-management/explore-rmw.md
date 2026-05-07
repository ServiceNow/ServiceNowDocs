---
title: Exploring Resource Management Workspace
description: Learn about the features, functionalities, and business value that the Resource Management Workspace provides.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Exploring Resource Management Workspace

Learn about the features, functionalities, and business value that the Resource Management Workspace provides.

This provides a centralized view of the resource allocation and requests. As a Resource manager, you get a dedicated workspace to view the team's allocation and breakdown of the work assigned to the resources.

Resource Management Workspace provides a centralized view of the resource allocations and resource requests. This workspace eases resource management problems and is designed to cover a wider set of use cases.

## Features and benefits

|Feature|Benefit|
|-------|-------|
|Persistent card view|Create focused view to view and work on resource allocations.|
|Resource allocation view|Breakdown view of resource allocations at weekly or monthly level.|
|Allocate the unassigned work|Filter the unassigned tasks to view and allocate the work.|
|Integration with Microsoft Teams|Effortlessly collaborate with the task owner for additional insights.|
|Approve work for resources|Move the assigned work status to Approved, Unapproved, or Pending to allocate the prioritized work.|
|Iconography|Identify overallocated resources and reassign to maintain allocations within the resource bandwidth.|
|Heatmap modals|Breakdown view of the assigned work and efforts.|

## Resource Management Workspace overview

The Resource Management Workspace provides a centralized view for managing resource allocations and work assignments.

![Resource Management Workspace main interface showing resource cards, allocation view, and unassigned tasks tray.](../images/rmw-rsrc-portfolio-view.png "Resource Management Workspace main interface")

The workspace is organized into the following areas:

-   Resource board: Create filtered views to focus on specific teams, roles, or skills. For more information, see [Create a resource card](../task/rmw-create-rsrc-card.md).
-   Resource allocation view \(top tray\): Displays assigned work for each resource with weekly or monthly allocation breakdown and availability indicators.
-   Unassigned tasks \(bottom tray\): Shows pending resource requests that needs to be assigned. For more information, see [Assign unassigned work](../task/allocate-resources-rmw.md).

## Resource finder

Resource managers often spend significant time manually searching for the right person to staff an unassigned assignment. The AI Resource Finder removes this guesswork by using Now Assist skills to analyze your resource pool and recommend the best-fit candidates, ranked by a fit score and accompanied by a plain-language rationale explaining each recommendation.

Resource finder uses the Resource fit analysis skill, which considers multiple dimensions simultaneously: whether the resource's planning attributes \(such as role and skills group\) align with what the assignment demands, how much capacity the resource has during the assignment period, and how the resource's historical allocation patterns compare to the requested effort.

The output of this matching process is two-fold:

-   Fit score - a percentage that represents how closely a resource matches the requirements of an assignment. The score blends attribute alignment, temporal availability, and workload balance into one number so you can compare candidates at a glance.
-   Rationale - a short explanation of why the Resource fit analysis considers them a good fit. The rationale references specific factors like availability windows, complementary pairing opportunities, and attribute matches.

a expressed as a percentage, and a rationale that explains the reasoning in plain language. For example, a resource might receive a 30% fit score with a rationale noting that the person is available only in April and July, and suggesting they be paired with another resource to cover the May and June gap. The score gives you a quick ranking; the rationale gives you the context to act on it.

The Resource finder lets you compare each resource's available capacity against the requested effort for the assignment. Effort values respect the unit and cadence based on user preference such as hours, FTE, or person days on a weekly or monthly basis.

The availability heatmap uses color coding to make this comparison instant. A green cell means the resource has enough capacity to meet the requested effort for that period. A red cell means they fall short. For example, if the requested effort is 1 FTE per month and a candidate shows 1 for April and 0 for May, April appears green and May appears red helping you to immediately see the gap without doing any mental math.

Advantages of using Resource finder

-   Quickly staff an unassigned assignment: Resource managers use the Resource finder option from the unassigned assignment's three-dot menu. The AI insights presents a ranked shortlist which the resource manager can reviews the rationale, confirm availability, and assigns the best fit within a single modal flow.
-   Handle partial availability with resource pairing: Resource Finder surfaces the real-time availability through its rationale, which suggests pairing two resources to cover the complete period. For example, one resource covers April and July while another covers May and June.
-   Balancing workloads: resource board indicator in the Resource finder highlights which candidates already belong to the manager's boards, making it easier to redistribute work within the existing team before pulling in resources from other groups.

## Getting started

Follow these steps to begin using the workspace.

1.  [Configure the workspace](../task/config-rmw.md) to enable the required features and permissions.
2.  [Create a resource card](../task/rmw-create-rsrc-card.md) to define your filtered view of resources.
3.  [View and assign unassigned work](../task/allocate-resources-rmw.md) to available resources.
4.  [Manage resource allocations](../task/manage-resource-allocations-rmw.md) to adjust and approve assignments.

**Parent Topic:**[Resource Management Workspace](rsrc-mgmt-wrkspc.md)

