---
title: Service Model Foundation Granular admin roles
description: Granular admin roles enable organizations to assign specific administrative permissions based on functional responsibilities, replacing broad admin access with targeted role assignments.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Roles, Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Service Model Foundation Granular admin roles

Granular admin roles enable organizations to assign specific administrative permissions based on functional responsibilities, replacing broad admin access with targeted role assignments.

The following table describes the granular admin roles that the administrator can assign to the internal users.

<table id="granular_admin_roles"><thead><tr><th>

Role name

</th><th>

Description

</th><th>

Inherited by

</th><th>

Inherits

</th></tr></thead><tbody><tr><td>

sn\_bus\_loc.business\_org\_admin

</td><td>

Provides CRUD access to all Service Model Foundation tables

</td><td>

No

</td><td>

-   sn\_service\_org.service\_org\_admin
-   sn\_bus\_loc.ibl\_writer
-   sn\_bus\_loc.ebl\_viewer
-   sn\_bus\_loc.ibl\_viewer
-   sn\_bus\_loc.writer

</td></tr><tr><td>

sn\_service\_org.service\_org\_admin

</td><td>

Provides all CRUD access to service organization entities, which come under Service Model Foundation flows

</td><td>

sn\_bus\_loc.business\_org\_admin

</td><td>

-   sn\_service\_org.viewer
-   sn\_service\_org.writer
-   sn\_service\_org.service\_org\_delete
-   sn\_service\_org.service\_org\_external\_staff\_create
-   sn\_service\_org.service\_org\_external\_staff\_read
-   sn\_service\_org.service\_org\_external\_staff\_write
-   sn\_service\_org.service\_org\_external\_staff\_delete
-   sn\_service\_org.service\_org\_assignment\_group\_create
-   sn\_service\_org.service\_org\_assignment\_group\_read
-   sn\_service\_org.service\_org\_assignment\_group\_write
-   sn\_service\_org.service\_org\_assignment\_group\_delete
-   sn\_service\_org.service\_org\_criteria\_create
-   sn\_service\_org.service\_org\_criteria\_read
-   sn\_service\_org.service\_org\_criteria\_write
-   sn\_service\_org.service\_org\_criteria\_delete
-   sn\_service\_org.service\_org\_customer\_criteria\_create
-   sn\_service\_org.service\_org\_customer\_criteria\_read
-   sn\_service\_org.service\_org\_customer\_criteria\_write
-   sn\_service\_org.service\_org\_customer\_criteria\_delete
-   sn\_service\_org.service\_criteria\_write
-   sn\_service\_org.service\_criteria\_delete
-   sn\_service\_org.service\_criteria\_read
-   sn\_service\_org.service\_criteria\_create

</td></tr><tr><td>

sn\_csm\_ocs.csm\_ocs\_admin

</td><td>

Provide full CRUD access to Outsourced Customer Service flow

</td><td>

No

</td><td>

sn\_service\_org.service\_external\_staff.create sn\_service\_org.service\_external\_staff.read sn\_service\_org.service\_external\_staff.write sn\_service\_org.service\_external\_staff.delete sn\_contractor.outsourced\_service\_provider\_create sn\_contractor.outsourced\_service\_provider\_read sn\_contractor.outsourced\_service\_provider\_write sn\_contractor.outsourced\_service\_provider\_delete sn\_contractor.outsourced\_service\_provider\_criteria\_create sn\_contractor.outsourced\_service\_provider\_criteria\_read sn\_contractor.outsourced\_service\_provider\_criteria\_write sn\_contractor.outsourced\_service\_provider\_criteria\_delete sn\_csm\_ocs.sn\_csm\_ocs\_case\_transfer\_request\_create sn\_csm\_ocs.sn\_csm\_ocs\_case\_transfer\_request\_read sn\_csm\_ocs.sn\_csm\_ocs\_case\_transfer\_request\_write sn\_csm\_ocs.sn\_csm\_ocs\_case\_transfer\_request\_delete

</td></tr></tbody>
</table>## Other granular admin roles for Service Model Foundation configuration

The following are the roles required to perform Service Model Foundation \(SMF\) configuration tasks:

|Role name|Description|Plugin\(s\) required|
|---------|-----------|--------------------|
|sn\_queryrules.admin|Provides admin access to all query rules.|com.snc.query\_rules|
|user\_admin|Administers users, groups, locations, and companies.|None|
|service\_definition\_admin|Provides full CRUD access to the service definition and related tables|None|
|sn\_crm\_account\_relationship\_data\_manager|Extends the sn\_crm\_account\_data\_manager role by granting additional admin access to account relationships.|cs\_base|
|sn\_crm\_consumer\_relationship\_data\_manager|Extends the sn\_crm\_consumer\_data\_manager role by granting additional admin access to consumer relationships.|cs\_base|
|sn\_crm\_household\_relationship\_data\_manager|Extends the sn\_crm\_household\_data\_manager role by granting additional admin access to household relationships.It also contains sn\_crm\_consumer\_relationship\_data\_manager role.|com.snc.cs\_base/if/com.snc.household/|

