---
title: Components installed with AMF Core
description: The following components are installed with activation of the AMF Core plugin \(com.glide.amf\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/installed-with-amf-core.html
release: brazil
topic_type: reference
last_updated: "2026-09-21"
reading_time_minutes: 1
keywords: [AMF Core, com.glide.amf, ALM MIM Framework, roles, tables]
breadcrumb: [Install Multi-Instance Setup and AMF Core, Multi-Instance Setup, Multi-Instance Management, Get started, Administer the ServiceNow AI Platform]
---

# Components installed with AMF Core

The following components are installed with activation of the AMF Core plugin \(com.glide.amf\).

## Roles installed

<table id="table_j32_ftr_qkc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

AMF Core administrator

 \[sn\_amf.amf\_core\_admin\]

</td><td>

Defines and manages connections between controller and managed instances.

</td><td>

sn\_mif.mif\_admin

</td></tr><tr><td>

AMF Core viewer

 \[sn\_amf.amf\_core\_read\]

</td><td>

Views connections between controller and managed instances.

</td><td>

sn\_mif.mif\_read

</td></tr></tbody>
</table>## Tables installed

<table id="table_n32_ftr_qkc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AMF Instance

 \[sn\_amf\_instance\]

</td><td>

Controller and managed instances and their instance type.

</td></tr><tr><td>

AMF Instance Type

 \[sn\_amf\_instance\_type\]

</td><td>

Configured instance types: Development, Production, and Test by default.

</td></tr></tbody>
</table>