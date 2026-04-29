---
title: TRM Technical Debt calculation in Enterprise Architecture Workspace
description: A TRM technical debt indicates the unapproved usage of a software. The technical debts table \[sn\_apm\_trm\_standards\_technical\_debt\], displays the TRM products and associated business applications details, and the reason for the technical debt.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage the Technology Reference Model in Enterprise Architecture Workspace, Exploring Technology Portfolio view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# TRM Technical Debt calculation in Enterprise Architecture Workspace

A TRM technical debt indicates the unapproved usage of a software. The technical debts table \[sn\_apm\_trm\_standards\_technical\_debt\], displays the TRM products and associated business applications details, and the reason for the technical debt.

To view the TRM technical debts, you require Technology Portfolio Management \[sn\_apm\_tpm\] store application and SAM Foundation \[com.snc.sams\] plugin.

Technical debts are created at two levels if any of the following conditions are met. The Level 2 is checked only if the system property **sn\_apm\_trm.is\_product\_life\_cycle\_tech\_debt\_enabled** is set to True.

-   Level 1
    -   If a product is associated with a business application, but isn’t part of the TRM product list. \(OR\)
    -   If a product is associated with a business application and part of the TRM products list, but has the TRM phase's production unapproved.
-   Level 2
    -   If a product is associated with a business application, is part of the TRM products list, and has the TRM phase's production approved but doesn’t have any associated TRM Product life cycles. \(OR\)
    -   If a product is associated with a business application and part of the TRM products list, has the TRM phase with production approved, and the TRM product lifecycle exists, one of the following cases is considered:

        Case 1: If the lifecycle full version of the software discovery model \[cmdb\_sam\_sw\_discovery\_model\] is not empty.

        A technical debt is created if the following condition isn’t met for a TRM Product lifecycle:

        -   TRM phase with production approved AND
        -   TRM product's TRM phase with production approved AND
        -   Version matching the lifecycle full version or wild card of the software discovery model \[cmdb\_sam\_sw\_discovery\_model\] AND
        -   Phase start date &lt;= Today's date &lt;=phase end date.
        Case 2: If the life cycle full version of the software discovery model \[cmdb\_sam\_sw\_discovery\_model\] is empty.

        Technical debt is created if the following condition isn’t met for a TRM Product Lifecycle:

        -   TRM phase with production approved AND
        -   TRM product's TRM phase with production approval AND
        -   Version matching \(exact match or wildcard match\) the version of software discovery model \[cmdb\_sam\_sw\_discovery\_model\] AND
        -   The edition of TRM lifecycle matching with edition for software discovery model \[cmdb\_sam\_sw\_discovery\_model\] AND
        -   Phase start date &lt;= Today's date &lt;=phase end date.

**Parent Topic:**[Manage the Technology Reference Model in Enterprise Architecture Workspace](eaw-managing-the-technology-portfolio.md)

