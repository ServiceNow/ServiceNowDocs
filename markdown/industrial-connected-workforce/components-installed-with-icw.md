---
title: Components installed with the Industrial Connected Workforce
description: Several types of components are installed with activation of the plugin, including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Industrial Connected Workforce Core, Industrial Connected Workforce]
---

# Components installed with the Industrial Connected Workforce

Several types of components are installed with activation of the plugin, including tables and user roles.

## Roles installed

<table id="table_xbb_vps_bdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Action Expert

 \[sn\_icw.action\_expert\]

</td><td>

Expert role for the Actions module

</td><td>

sn\_icw.action\_user

</td></tr><tr><td>

Action User

 \[sn\_icw.action\_user\]

</td><td>

User role for the Actions module

</td><td>

sn\_icw.user

</td></tr><tr><td>

ICW Admin

 \[sn\_icw.admin\]

</td><td>

Administrator role for the ICW Core application

</td><td>

-   category\_manager
-   cmdb\_ot\_isa\_editor
-   sn\_ent.classification\_manager
-   sn\_icw.user
-   view\_changer
-   schedule\_admin
-   cmdb\_ot\_isa\_admin
-   model\_manager
-   sn\_smart\_asmt.assessment\_admin

</td></tr><tr><td>

ICW Application Admin

 sn\_icw.application\_admin

</td><td>

Role for administering the ICW application

</td><td>

sn\_icw.admin

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ICW Config

 \[sn\_icw.config\]

</td><td>

Configuration role for the ICW Core application

</td><td>

-   sn\_icw.user
-   cmdb\_ot\_isa\_editor
-   schedule\_admin

</td></tr><tr><td>

Deviation Expert

 \[sn\_icw.deviation\_expert\]

</td><td>

Expert role for the Deviations module

</td><td>

sn\_icw.deviation\_user

</td></tr><tr><td>

Deviation User

 \[sn\_icw.deviation\_user\]

</td><td>

User role for the Deviations module

</td><td>

sn\_icw.user

</td></tr><tr><td>

Knowledge Author

 \[sn\_icw.knowledge\_author\]

</td><td>

Knowledge Author role for the ICW Core application

</td><td>

-   knowledge
-   sn\_icw.user

</td></tr><tr><td>

Knowledge Manager

 \[sn\_icw.knowledge\_manager\]

</td><td>

Knowledge Manager role for the ICW Core application

</td><td>

-   knowledge\_coach
-   knowledge
-   sn\_icw.user
-   knowledge\_manager
-   knowledge\_view\_as

</td></tr><tr><td>

Root Cause Analysis Expert

 \[sn\_icw.rca\_expert\]

</td><td>

Expert role for Root Cause Analysis

</td><td>

sn\_icw.rca\_user

</td></tr><tr><td>

Root Cause Analysis User

 \[sn\_icw.rca\_user\]

</td><td>

User role for root Cause Analysis

</td><td>

sn\_icw.user

</td></tr><tr><td>

ICW Report User

 \[sn\_icw.report\_user\]

</td><td>

Report user role for the ICW Core application

</td><td>

sn\_icw.user

</td></tr><tr><td>

ICW User

 \[sn\_icw.user\]

</td><td>

User role for the ICW Core application

</td><td>

-   canvas\_user
-   cmdb\_ot\_isa\_viewer
-   sn\_ent.classification\_reader
-   sn\_nb\_action.next\_best\_action\_user

</td></tr></tbody>
</table>## Tables installed

-   Industrial Action \[sn\_icw\_action\]
-   Action Priority Data lookup \[sn\_icw\_action\_dl\_priority\]
-   Industrial Deviation \[sn\_icw\_deviation\]
-   Deviation Priority Data lookup \[sn\_icw\_deviation\_dl\_priority\]
-   Failure \[sn\_icw\_failure\]
-   Industrial Calendar \[sn\_icw\_industrial\_calendar\]
-   Industrial Calendar Span \[sn\_icw\_industrial\_calendar\_span\]
-   Industrial Root Cause Analysis \[sn\_icw\_rca\]
-   Root Cause Analysis Priority Data lookup \[sn\_icw\_rca\_dl\_priority\]
-   Industrial Task \[sn\_icw\_task\]
-   Worker profile \[sn\_icw\_worker\_profile\]

**Parent Topic:**[Industrial Connected Workforce reference](icw-reference.md)

