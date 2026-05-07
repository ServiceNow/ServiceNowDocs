---
title: View TRM technical debts
description: You can view the Technology Reference Model \(TRM\) technical debts that are created for the products that aren’t aligned with the TRM phases and standards.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with Technology Reference Model \(TRM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# View TRM technical debts

You can view the Technology Reference Model \(TRM\) technical debts that are created for the products that aren’t aligned with the TRM phases and standards.

## Before you begin

Role required: sn\_apm.apm\_analyst

## About this task

A scheduled job **Populate TRM technical debts in the EA Workspace** runs and creates an entry in the TRM Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table for EA Workspace. The table shows a reference to the software in any business application that is not aligned with the TRM software phases. The table shows a reference to the software in any business application that either isn’t defined in TRM or has TRM product lifecycles that restrict the usage of the software. To know how the technical debts are calculated, see [TRM Technical Debt calculation in Enterprise Architecture Workspace](../../concept/eaw-concept/eaw-trm-technical-debt-calc.md).

**Note:** The **Populate TRM technical debts in the EA Workspace** scheduled job is available only when the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Technology Portfolio page by selecting the Technology Portfolio icon ![Technology portfolio icon](../../image/eaw-image/technology-portfolio-icon.png).

3.  Select **Technical Debt**.

4.  View the TRM technical debts.

    For field information, see [TRM technical debt form](../../reference/eaw-reference/eaw-trm-technical-debt-form.md).


## Result

Review the list of TRM products and associated business applications details. You can also view the reason for the technical debt.

**Parent Topic:**[Working with Technology Reference Model \(TRM\) in EA Workspace](../../concept/eaw-concept/eaw-work-with-trm.md)

**Related topics**  


[View all TRM phases](eaw-view-all-trm-phases.md)

[Add a TRM product in Enterprise Architecture Workspace](eaw-create-trm-prod-lifecycle.md)

[View all TRM categories](view-all-trm-categories.md)

[View all TRM products](eaw-view-all-trm-products.md)

[Run a scheduled job to update TRM technical debt data in EA Workspace](eaw-run-job-trm-tech-debts.md)

[Request a TRM product](eaw-request-a-trm-products.md)

[View all TRM products grouped by product category](eaw-view-all-trm-products-grouped-by-product-category.md)

[Request a TRM product lifecycle](eaw-request-a-trm-product-lifecycle.md)

[Associate an Architectural Artifact to a TRM product](eaw-assoicate-artifact-trm-prod.md)

[Add a TRM product lifecycle](eaw-create-trm-prod-lifecycle-req.md)

[Manage the Technology Reference Model in Enterprise Architecture Workspace](../../concept/eaw-concept/eaw-managing-the-technology-portfolio.md)

[View or update your TRM requests](eaw-view-update-trm-requests.md)

