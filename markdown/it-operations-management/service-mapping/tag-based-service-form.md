---
title: About the tag-based application service form
description: The tag-based application service form provides a centralized location for viewing detailed information about a selected tag-based service, including its configuration and its associated configuration items.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-10-22"
reading_time_minutes: 1
breadcrumb: [Tag mapping in the workspace, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# About the tag-based application service form

The tag-based application service form provides a centralized location for viewing detailed information about a selected tag-based service, including its configuration and its associated configuration items.

The tag-based application service form offers a comprehensive view of a tag-based application service. With actionable buttons and multiple tabs, you can manage and troubleshoot your tag-based application services and their associated configuration items \(CIs\).

## Access

To access the tag-based application service form:

1.  Navigate to **Workspaces** &gt; **Service Mapping** &gt; **.**
2.  Select the **Tag-based Service Mapping** icon ![](../../../reuse/icons/product-icons/tag-outline-24.svg) from the navigation pane.
3.  Select the **Tag-based service maps** tile.
4.  Select the desired tag-based service to view the tag-based application service form.

## Details tab

The **Details** tab displays basic information about the selected tag-based application service, including the service family and tag categories associated with the service. Use this tab to update the basic information about an application service, such as the description, the criticality, or the operational status.

## Service CIs tab

The **Service CIs** tab lists the configuration items \(CIs\) that are part of the selected tag-based application service. The **svc\_by\_tags.max\_ci\_limit** property controls number of CIs listed in this tab. Currently, the list is limited to the first 1,000 CIs that match the criteria for the tag-based service.

**Note:** This list filters out manual endpoints, ensuring that only relevant CIs are displayed.

## Tagged CIs tab

The **Tagged CIs** tab lists all CIs that meet the criteria for a tag-based application service, up to 4,000. The **sa.it\_service.list\_cis\_max\_count** property controls this limit. This list includes CIs belonging to the application service \(also listed on the **Service CIs** tab\) and up to 3,000 additional CIs. This tab is useful for building new tag-based application services or troubleshooting existing services with a preview of relevant CIs. However, no CIs beyond the 4000 limit are displayed.

**Parent Topic:**[Tag-based mapping in the Service Mapping Workspace](../reference/tag-based-mapping-dashboard.md)

