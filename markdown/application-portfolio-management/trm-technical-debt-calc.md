---
title: Manage Technology Reference Model \(TRM\) technical debt
description: Manage the TRM technical debts that are created for the products that aren’t aligned with the TRM phases and standards.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage Technology Reference Model \(TRM\) technical debt

Manage the TRM technical debts that are created for the products that aren’t aligned with the TRM phases and standards.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy Technology Reference Model module has been deprecated from Enterprise Architecture \(formerly Application Portfolio Management\). However, if you’re an existing user of Enterprise Architecture \(formerly Application Portfolio Management\), you can still use the legacy Technology Reference Model module. If you’re a new activation user, the legacy Technology Reference Model module isn’t available.

You can leverage the same functionality by using the Enterprise Architecture Workspace. To learn more, see [Manage TRM technical debt](../concept/eaw-concept/eaw-manage-trm-technical-debt.md).

Role required: sn\_apm.apm\_analyst

## About this task

A scheduled job **Populate TRM technical debts in the EA Workspace** runs and creates an entry in the TRM Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table for EA Workspace. The table shows a reference to the software in any business application that is not aligned with the TRM software phases. The table shows a reference to the software in any business application that either is not defined in TRM or has TRM product lifecycles that restrict the usage of the software. To know how the technical debts are calculated, see [Manage Technology Reference Model \(TRM\) technical debt](trm-technical-debt-calc.md).

Technical debts are created at two levels if any of the following conditions are met. The Level 2 is checked only if the system property **sn\_apm\_trm.is\_product\_life\_cycle\_tech\_debt\_enabled** is set to True.

-   Level 1
    -   If a product is associated with a business application, but isn’t part of the TRM product list. \(OR\)
    -   If a product is associated with a business application and part of the TRM products list, but has the TRM phase's production unapproved.
-   Level 2
    -   If a product is associated with a business application, is part of the TRM products list, and has the TRM phase's production approved but doesn’t have any associated TRM Product life cycles. \(OR\)
    -   If a product is associated with a business application and part of the TRM products list, has the TRM phase with production approved, and the TRM product lifeycle exists, one of the following cases is considered:

        Case 1: If the lifecycle full version of the Application Service Software Model is not empty.

        A technical debt is created if the following condition isn’t met for a TRM Product lifecycle:

        -   TRM phase with production approved AND
        -   TRM product's TRM phase with production approved AND
        -   Version matching the lifecycle full version of the application service software model record AND
        -   Phase start date &lt;= Today's date &lt;=phase end date.
        Case 2: If the life cycle full version of the Application Service Software Model is empty.

        Technical debt is created if the following condition isn’t met for a TRM Product Lifecycle:

        -   TRM phase with production approved AND
        -   TRM product's TRM phase with production approval AND
        -   Version is/starts with \(based on version operator and isSampPluginInstalled\) version of the associated software model AND
        -   The edition is/starts with \(based on edition operator and isSampPluginInstalled\) edition of associated software model AND
        -   Phase start date &lt;= Today's date &lt;=phase end date.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Technology Reference Model \(TRM\)** &gt; **Technical Debts**.

2.  Review the list of TRM products and associated business applications details.

    You can also view the reason for the technical debt.


