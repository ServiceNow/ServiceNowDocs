---
title: Determining license compliance through Virtualization Adapter
description: Software Asset Management Virtualization Adapter determines the license compliance of several software products deployed on virtualization technologies by applying license compliance rules. This feature is activated and installed with the base system in Software Asset Management.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software reconciliation for compliance, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Determining license compliance through Virtualization Adapter

Software Asset Management Virtualization Adapter determines the license compliance of several software products deployed on virtualization technologies by applying license compliance rules. This feature is activated and installed with the base system in Software Asset Management.

The following are the software products for which Software Asset Management Virtualization Adapter determines the license compliance:

-   Microsoft SQL Server
-   Windows Server
-   Red Hat Enterprise Linux Server \(RHEL\)
-   Oracle Database Server, Options, and WebLogic Server

Virtualization is a process of simulating hardware functionality and creating a virtual environment in which you can run more than one virtual machine on a single server in a clustered environment. For more information on Oracle Database and WebLogic Server licensing support on VMware vSphere and Nutanix virtualization technology, see [Oracle Database and WebLogic Server licensing in soft-partitioned environments](oracle-licensing-soft-partitioned-environments.md).

The virtualization technologies supported by Software Asset Management are:

-   VMware
-   Microsoft Hyper-V
-   Red Hat Virtualization
-   Nutanix

ITOM Discovery discovers virtualization technologies based on their relationship architecture. Software Asset Management depends on the discovered relationships to determine the license compliance of the software installations.

Software Asset Management Virtualization Adapter standardizes the relationship architecture through database views and metadata views, which are used by Software Asset Management to determine license compliance.

Software Asset Management considers the architecture of the virtualization technology while applying the licensing rules. For example, Microsoft Hyper-V architecture permits Windows Server Standard edition to use one running instance of the server software in the physical OSE on the licensed server in addition to two virtual OSEs if the physical OSE is used only to host and manage the virtual OSEs. Software Asset Management Virtualization Adapter automatically applies this rule set.

**Parent Topic:**[Software reconciliation for compliance](c_SAMReconciliation.md)

