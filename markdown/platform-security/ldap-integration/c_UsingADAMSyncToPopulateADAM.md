---
title: Use ADAMSync to populate ADAM
description: Administrators use MS ADAMSync to populate LDAP directories that use MS ADAM.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Use ADAMSync to populate ADAM

Administrators use MS ADAMSync to populate LDAP directories that use MS ADAM.

**Note:**

This document assumes you have at least a basic level of understanding with Microsoft Windows Server, Active Directory, and ADAM and that you already have a functional [Active Directory Application Mode \(ADAM\)](c_ActiveDirectoryApplicationMode.md) instance with a partition.

These are sample procedures. Due to the complexity and the fact that it is running in your environment, we cannot offer direct support. We recommend you work with Microsoft or a Microsoft consultant if you run into any trouble.

Once ADAM has been installed and the first partition has been created, you can populate it with objects.

The following options are available:

-   Manual object creation using GUI or scripts. This option is inefficient and slow.
-   Integrate with Active Directory using Microsoft Integration Information Server. This option ultimately provides the most flexibility and functionality but does require some advanced configurations. There is a free version of MIIS available that is compatible with Active Directory, ADAM, andMicrosoft Global Address Lists from Exchange. Unless you already have experience with MIIS we advise that you don’t attempt to implement a new environment for LDAP integration only.
-   Use ADAMSync, a synchronization tool that Microsoft provides with ADAM. This is the option that is explained here.

