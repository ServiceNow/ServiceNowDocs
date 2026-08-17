---
title: Components installed with RIDAC
description: A complete reference of RIDAC record fields, including data type, requirements, default values, and behavior notes for Strategic Planning Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/components-installed-with-ridac-spw.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-07-16"
reading_time_minutes: 1
keywords: [RADAC fields, field reference, RADAC table, data type]
breadcrumb: [Reference, RIDAC, Strategic Planning, Strategic Portfolio Management]
---

# Components installed with RIDAC

A complete reference of RIDAC record fields, including data type, requirements, default values, and behavior notes for Strategic Planning Workspace.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/find-components.md).

**Note:** This topic covers reference information specific to RIDAC, including user roles, tables, and system properties. For common reference information about tables, roles, and system properties installed with Strategic Planning, see [Strategic Planning Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/alignment-planner-workspace-reference.md).

## Roles installed with RIDAC in Strategic Planning Workspace

<table id="table_zkd_jny_bkc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

RIDAC reader\[sn\_align\_ws.ridac\_read\_only\]

</td><td>

Can view RIDAC \(Risk, Issue, Decision, Action, Change request\) items on planning items, EAP iterations, and goals.

</td><td>

None

</td></tr><tr><td>

RIDAC user\[sn\_align\_ws.ridac\_user\]

</td><td>

Can create, update, and delete RIDAC \(Risk, Issue, Decision, Action, Change request\) items on planning items, EAP iterations, and goals.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed with RIDAC in Strategic Planning Workspace

|Scheduled job|Description|
|-------------|-----------|
|Update planning item on RIDAC tables|Populates the planning item field on RIDAC records that were created before the Strategic Planning was installed. This job ensures legacy RIDAC records appear correctly in related lists and reports.|

