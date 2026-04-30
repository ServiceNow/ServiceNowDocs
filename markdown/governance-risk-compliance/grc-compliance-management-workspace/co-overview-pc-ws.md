---
title: Manage a control objective from the overview page
description: The Overview page of the control objective record gives you the overall details of its compliance status.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a control objective using the Compliance Workspace, Manage control objectives and policies using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Manage a control objective from the overview page

The Overview page of the control objective record gives you the overall details of its compliance status.

## Overview page of a Control objective record

The control assurance section helps you to know if different attestations are in place, which demonstrates that the control has been implemented correctly. The indicators, in addition to control attestations, help to assess the controls or to monitor their compliance continuously. The ongoing and overdue status of tests conducted on controls is the key determinant by which the organization determines that its policies and authority documents are being followed.

![Overview tab of new control objective record page.](../image/record-page-mig-co.png "Overview page of a control objective record")

For more contextual information about the control objective, select the sidebar icon \(![Sidebar icon.](../image/pc-ws-sidebar-icon.png)\). For a given control objective record, you can view the hierarchy of mappings back to the authority documents and policies that show why you do the actions indicated in the control objective.

A control objective record has many related lists that come from different applications such as Advanced Risk, GRC Metric, PaCE, and others, which are listed next to the Overview. You can map or associate any of these available related list item with the control objective. For example, if you would like to add an entity type to the control objective, you can navigate to the Entity types related list, select the **Add** button, and map the required entity type.

## Control objective requirements

A control objective requirement is a granular layer under a control objective that specifies a distinct compliance condition or expectation. Each control objective can have multiple statements, and each statement becomes a control objective requirement.

When control objectives are imported, if any control objective requirements are available in the source, they will also be imported with the control objective. Control objective requirements can also be manually added or selected from existing requirements when configuring a control objective.

When controls are generated under an entity, the control objective requirements help create corresponding control requirements.

