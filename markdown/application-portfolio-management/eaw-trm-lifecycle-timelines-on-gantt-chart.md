---
title: TRM lifecycle timelines on Gantt chart
description: For Technology Reference Model \(TRM\), the application services \(hardware models and software products\) are displayed in a hierarchical structure, similar to the TPM view. The corresponding lifecycle timelines of the application services are displayed as bars on the Gantt chart. It also displays the data for lifecycles with wild card versions. The TRM wildcard version ends with a ‘\*’.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Gantt view of TPM and TRM lifecycle timelines, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# TRM lifecycle timelines on Gantt chart

For Technology Reference Model \(TRM\), the application services \(hardware models and software products\) are displayed in a hierarchical structure, similar to the TPM view. The corresponding lifecycle timelines of the application services are displayed as bars on the Gantt chart. It also displays the data for lifecycles with wild card versions. The TRM wildcard version ends with a ‘\*’.

![TRM view of the Gantt chart.](../../image/eaw-image/TRM-gantt-chart.png "TRM Gantt chart view")

In TRM view, the lifecycles aren’t aggregated to application services or business applications.

It displays the following TRM related information:

-   **TRM Phase**
-   **Start date**
-   **End date**

You can point to an individual bar in the Gantt chart to view the phase information.

The Application services column is populated from the TPM Discovered Technology table \(sn\_apm\_tpm\_discovered\_technology\).

## TRM phase status

The TRM view also displays the status of the TRM phases of the software products or hardware models. The TRM phase column is populated from the TRM Product Lifecycle table \(sn\_apm\_trm\_standards\_product\_lifecycle\).

If no TRM product lifecycle data is available for an application service, then the TRM phase for that service is displayed as **Not assessed**.

Also, if a TRM product phase doesn’t have the **Production approved** check box \(**Enterprise Architecture Workspace** &gt; **Setup** &gt; **TRM Phases**\) selected, then the TRM phase column displays the status of the application service having that TRM phase as **Unapproved**. For details on how to approve a TRM phase, see [Add or edit a TRM phase](../../task/define-trm-phases.md).

Only when the TRM phase is marked as production approved and the phase start date has already passed, the TRM phase for the application service is displayed in the TRM phase column. For example, the TRM phase **Divest** is marked as production approved and has a start date of 01-12-2023. The current date is 10-12-2023. In such a scenario, all application services associated with the TRM phase have their phase status as **Divest** in the TRM phase column.

If you have TRM products that aren't aligned with TRM phases and standards, then a TRM technical debt is created in the TRM Technical Debt \(sn\_apm\_trm\_standards\_technical\_debt\) table. TRM technical debts are created at two levels. The following table contains information on TRM technical debts and their associated levels.

|TRM product|TRM phase|TRM level|Reason|Explanation|
|-----------|---------|---------|------|-----------|
|Not applicable|Not applicable|Product|The software isn’t defined in TRM.|TRM product isn’t available.|
|TRM Product Name|TRM Product Phase|Product|The software isn’t approved for production.|TRM product isn’t production approved.|
|TRM Product Name|Not applicable|Product lifecycle|The software version isn’t defined in the TRM product lifecycle.|No TRM lifecycle is available for the TRM product.|
|TRM Product Name|Not applicable|Product lifecycle|The software version isn’t defined in the TRM product lifecycle.|TRM lifecycle with full version information isn’t available.|
|TRM Product Name|Not applicable|Product lifecycle|The software version isn’t defined in the TRM product lifecycle.|TRM lifecycle with version information isn’t available.|
|TRM Product Name|Not applicable|Product lifecycle|The software version isn’t defined in the TRM product lifecycle.|TRM lifecycle with version information isn’t available.|
|TRM Product Name|Lifecycle phase|Product lifecycle|The software version isn’t approved for production.|TRM lifecycle with full version information isn’t production approved.|
|TRM Product Name|Not applicable|Product lifecycle|The software version isn’t approved for production.|TRM lifecycle with full version isn’t available for current date.|
|TRM Product Name|Lifecycle phase|Product lifecycle|The software version isn’t approved for production.|TRM lifecycle with version and edition information isn’t production approved.|

For details on TRM technical debts, see [Manage Technology Reference Model \(TRM\) technical debt](../../task/trm-technical-debt-calc.md).

You can schedule the **Populate TRM technical debts in the EA Workspace** job to update the TRM technical debt data in the EA Workspace. For more information, see [Run a scheduled job to update TRM technical debt data in EA Workspace](../../task/eaw-task/eaw-run-job-trm-tech-debts.md).

## Lifecycle end-date calculation logic

Entering an end date isn’t required while creating a TRM product lifecycle.

For each TRM lifecycle phase, the end date of one phase is the start date of the next phase. For example, application service A has two TRM phases that are **Divest** and **Approved with Constraints**. The start date for the **Divest** phase is 01-12-2023 and the start date for the **Approved with Constraints** phase is 30-12-2023. No phase end date has been mentioned for the **Divest** phase. In such a scenario, the end date of the **Divest** phase is considered as 30-12-2023. An error message is displayed if the product lifecycle dates overlap.

For the last phase, the end date is calculated by adding the time value as defined in the system property **sn\_apm.endRangeofTPMLifecycle** with the current date. For example, today is 01-12-2023 and the end date value as defined in the system property **sn\_apm.endRangeofTPMLifecycle** is three years from the current date. Then, the end date of the phase will be 01-12-2026.

## Application service timelines

The TRM product lifecycle timeline bars are displayed on the Gantt chart. However, for the lifecycle timeline bars to be displayed, some criteria must be fulfilled.

-   Software products: For software products, the TRM product **Name** and **Product full version** values for that particular software product as defined in the TPM Technology Lifecycle table \(sn\_apm\_tpm\_technology\_lifecycle\) should match the **TRM Product** and **Version** values that are entered while creating the TRM lifecycle for that product.

    Or the TRM product **Name**, **Version**, and **Edition** values for that particular software product as defined in the TPM Technology Lifecycle table \(sn\_apm\_tpm\_technology\_lifecycle\) should match the **TRM Product**,**Version**, and **Edition** values that are entered while creating the TRM lifecycle for that product.

-   Hardware models: For hardware models, the TRM product hardware model value for that application service should match the hardware model value that is entered while creating the TRM lifecycle for that application service.

For details on how to create a TRM product, see [Add a TRM product in Enterprise Architecture Workspace](../../task/eaw-task/eaw-create-trm-prod-lifecycle.md).

For details on how to create a TRM product lifecycle request, see [Add a TRM product lifecycle](../../task/eaw-task/eaw-create-trm-prod-lifecycle-req.md).

For details on how to approve or reject a TRM product or lifecycle request, see [Approve or reject a TRM product or product lifecycle request](../../task/approve-reject-trm-request.md).

## Color coding

The colors of the TRM lifecycle timeline bars are based on their TRM phase status. To see the colors associated with each TRM phase status, select the **Legend** button \(![Legend button.](../../image/eaw-image/legend-icon.png)\).

You can also change the TRM phase colors according to your requirement. For details on how to modify existing TRM phase colors, see [Add or edit a TRM phase](../../task/define-trm-phases.md).

**Parent Topic:**[Gantt view of TPM and TRM lifecycle timelines](eaw-gantt-view-of-tpm-and-trm-lifecycle-timelines.md)

