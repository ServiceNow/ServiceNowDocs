---
title: Visibility of change model records across sites
description: Depending on your Operational Technology \(OT\) change role and site role, you can view, create, or edit the change model record for your site or other sites.
locale: en-US
release: australia
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Change Management, Operational Technology]
---

# Visibility of change model records across sites

Depending on your Operational Technology \(OT\) change role and site role, you can view, create, or edit the change model record for your site or other sites.

## OT Change roles and visibility to change model records​

The following tables describe the roles and permissions for different OT change users to access change model records.

|Role|Permissions|
|----|-----------|
|sn\_ot\_change\_write with cmdb\_ot\_isa\_editor site role|Use a change model for their records.|
|sn\_ot\_change\_write with cmdb\_ot\_isa\_viewer site role|Use a change model for their records.|
|sn\_ot\_change\_write​ with cmdb\_ot\_isa\_viewer\_all site role|Use a change model for their records.|
|sn\_ot\_change\_write with no site role|No access to change models.|

|Role|Permissions|
|----|-----------|
|sn\_ot\_change\_read with cmdb\_ot\_isa\_editor site role|No access to change models.|
|sn\_ot\_change\_read with cmdb\_ot\_isa\_viewer site role|No access to change models.|
|sn\_ot\_change\_read with no site role|No access to change models.|
|sn\_ot\_change\_read​ with cmdb\_ot\_isa\_viewer\_all site role|No access to change models.|

<table id="table_k34_gyk_dxb"><thead><tr><th>

Role

</th><th>

Permissions

</th></tr></thead><tbody><tr><td>

sn\_ot\_change\_manager with cmdb\_ot\_isa\_editor site role

</td><td>

-   Create, edit, and delete change models for any site.
-   Assign change models to any site​.
-   Remove change models from any site.

</td></tr><tr><td>

sn\_ot\_change\_manager with cmdb\_ot\_isa\_viewer site role

</td><td>

-   Create, edit, and delete change models for any site.
-   Assign change models to any site​.
-   Remove change models from any site.

</td></tr><tr><td>

sn\_ot\_change\_manager with no site role

</td><td>

Can’t view or edit change models for any site. Can only view the base system change models that aren't associated with any site.

</td></tr></tbody>
</table>If you have the sn\_ot\_change\_admin role, you can use the change models to create a change request for any site.

**Parent Topic:**[Using Operational Technology Change Management](using-operational-technology-change-management.md)

