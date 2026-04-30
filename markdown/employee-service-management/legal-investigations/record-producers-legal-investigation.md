---
title: Record producers for legal investigations
description: A record producer helps you set up an intake form containing fields that a requester has to fill in and initiate a request.
locale: en-US
release: zurich
product: Legal Investigations
classification: legal-investigations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Record producers for legal investigations

A record producer helps you set up an intake form containing fields that a requester has to fill in and initiate a request.

When Legal Investigations is installed, record producers for ethic complaints are installed.

When an employee submits a complaint, a legal request or universal request is created based on the active record producers' mapping to different tables.

**Important:** At any given time, only one set of record producers mapped to a specific table can be active.

## Legal requests

The following record producers can be activated for creating legal requests when a complaint is submitted.

**Note:** To submit a legal request via the Anonymous Report Center portal, you require a HRSD Pro/Enterprise license in addition to the Legal Investigations subscription.

<table id="table_qll_chd_jvb"><thead><tr><th>

Record producer name

</th><th>

Mapped table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ethics Complaints

</td><td>

Ethics \[sn\_lg\_ops\_ethics\]

</td><td>

-   Submitting via Legal Service Portal or via the **Legal** menu option in the Employee Center portal.
-   Creates a legal request.

</td></tr><tr><td>

Ethics Complaints

</td><td>

Ethics \[sn\_lg\_ops\_ethics\]

</td><td>

-   Submitting via the Anonymous Report Center portal.
-   Creates a legal request.

</td></tr></tbody>
</table>## Universal requests

The following record producers can be activated for creating universal requests when a complaint is submitted.

**Note:** These record producers are inactive by default. If you want to integrate Legal Investigations with HR Service Delivery Employee Relations and transfer complaints between the Legal and HR departments, you must activate them.

<table id="table_oxq_j3k_2vb"><thead><tr><th>

Record producer name

</th><th>

Mapped table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ethics Complaints

</td><td>

Universal Request \[universal\_request\]

</td><td>

-   Submitting via the **Quick Link** option in the Employee Center portal.
-   Creates a universal request.
-   Marks the request as a sensitive case by default.

</td></tr><tr><td>

Ethics Complaints

</td><td>

Universal Request \[universal\_request\]

</td><td>

-   Submitting via the Anonymous Report Center portal.
-   Creates a universal request.
-   Marks the request as a sensitive case by default.

</td></tr></tbody>
</table>For more information, see [Managing record producers for legal services](../../legal-request-management/concept/record-producers-legal-services.md).

**Parent Topic:**[Legal Investigations reference](legal-investigations-reference.md)

