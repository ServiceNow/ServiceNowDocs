---
title: Manage TRM technical debt
description: Manage the TRM technical debts that are created for the products that aren’t approved for the usage.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage the Technology Reference Model in Enterprise Architecture Workspace, Exploring Technology Portfolio view, Explore, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage TRM technical debt

Manage the TRM technical debts that are created for the products that aren’t approved for the usage.

A scheduled job **Populate TRM technical debts in the EA Workspace** runs and creates an entry in the TRM Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table for EA Workspace. The table shows a reference to the software in any business application that is not aligned with the TRM software phases. The table shows a reference to the software in any business application that either isn’t defined in TRM or has TRM product lifecycles that restrict the usage of the software. To know how the technical debts are calculated, see [TRM Technical Debt calculation in Enterprise Architecture Workspace](eaw-trm-technical-debt-calc.md).

**Note:** The **Populate TRM technical debts in the EA Workspace** scheduled job is available only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

**Parent Topic:**[Manage the Technology Reference Model in Enterprise Architecture Workspace](eaw-managing-the-technology-portfolio.md)

**Related topics**  


[TRM Technical Debt calculation in Enterprise Architecture Workspace](eaw-trm-technical-debt-calc.md)

[View TRM technical debts](../../task/eaw-task/view-trm-tech-debt.md)

[Run a scheduled job to update TRM technical debt data in EA Workspace](../../task/eaw-task/eaw-run-job-trm-tech-debts.md)

