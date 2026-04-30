---
title: TRM technical debt form
description: The Technology Reference Model \(TRM\) technical debts that are created for the products that aren’t aligned with the TRM phases and standards.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# TRM technical debt form

The Technology Reference Model \(TRM\) technical debts that are created for the products that aren’t aligned with the TRM phases and standards.

<table id="table_ak2_5fg_tyb"><thead><tr><th>

Column name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TRM product

</td><td>

Name of the TRM product. A software product that is having version-specific life cycles.

</td></tr><tr><td>

Business Application

</td><td>

Name of the business application associated with the TRM product.

</td></tr><tr><td>

Server

</td><td>

Name of the server related to the TRM product.**Note:** This field is available from Technology Portfolio Management \(TPM\) plugin version 1.7.1.

</td></tr><tr><td>

Software product model

</td><td>

Name of the software product model related to the TRM product.

</td></tr><tr><td>

Software product

</td><td>

Name of the software product related to the TRM product.

</td></tr><tr><td>

Operating system

</td><td>

The operating system on which the TRM product can be deployed. This field appears on when **Software** is selected in the **Type** field.

</td></tr><tr><td>

TRM phase

</td><td>

Phase of the TRM product. The following TRM phases are available from the base system:-   Approved: The technology is approved for use.
-   Approved with Constraints: The technology can be used within the specified constraints specified in the comments.
-   Divest: A decision was taken to divest from the use of the technology.
-   Evaluation: This technology is being evaluated and can’t be used to production purposes.
-   Unapproved: The technology isn’t permitted to be used.

**Note:** You can modify these phases from the **EA Workspace** &gt; **Setup** &gt; **TRM Phases**

</td></tr><tr><td>

TRM level

</td><td>

The level \(Product or Product Lifecycle\) at which the technical debt is created.

</td></tr><tr><td>

Version

</td><td>

Version of the software product. Usually, the name of the Software product model contains this version.

</td></tr><tr><td>

Reason

</td><td>

The reason to explain why the technical debt was created.

</td></tr><tr><td>

Last run

</td><td>

Shows the timestamp when the custom scheduled job **Populate TRM technical debts in the EA Workspace** is run to update the table with technical debt.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[View TRM technical debts](../../task/eaw-task/view-trm-tech-debt.md)

[Manage TRM technical debt](../../concept/eaw-concept/eaw-manage-trm-technical-debt.md)

