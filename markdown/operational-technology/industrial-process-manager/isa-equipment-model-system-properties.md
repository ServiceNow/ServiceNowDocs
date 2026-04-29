---
title: ISA Equipment Model system properties
description: Enable the system properties for the ISA Equipment Model as needed.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Industrial Process Manager, Operational Technology]
---

# ISA Equipment Model system properties

Enable the system properties for the ISA Equipment Model as needed.

You can access the system properties for the ISA Equipment Model by navigating to **All** &gt; **Industrial Workspace Admin** &gt; **All OT Properties**. For more information about how to view and edit the OT system properties, see [View and edit OT system properties](../task/view-and-edit-ot-system-properties.md).

The following table describes the system properties for the ISA Equipment Model.

<table id="table_s3z_rwt_31c"><thead><tr><th>

System property

</th><th>

Description

</th><th>

Type

</th></tr></thead><tbody><tr><td>

sn\_isa\_model.cmdb\_relationships\_sync\_levels

</td><td>

Number of levels of CMDB relationships that are synchronized.

</td><td>

Integer

</td></tr><tr><td>

sn\_isa\_model.short\_code\_validation\_max\_length

</td><td>

Maximum length for the short code validation.

</td><td>

Integer

</td></tr><tr><td>

sn\_isa\_model.excluded\_operational\_statuses

</td><td>

List of equipment model operational statuses that need to be filtered out from the equipment model page.

</td><td>

String

</td></tr><tr><td>

sn\_isa\_model.user\_search\_matching\_attribute

</td><td>

Column on the User Table \[sys\_user\] that matches with a user in the system. By default, the Email column on the User table is used.

</td><td>

String

</td></tr><tr><td>

sn\_isa\_model.user\_sites\_cache.expiry\_time

</td><td>

Expiration time in seconds. The default is set to 600 \(10 minutes\).

</td><td>

Integer

</td></tr><tr><td>

sn\_isa\_model.use\_user\_sites\_cache

</td><td>

Enables the session cache for ISA entity records.

</td><td>

Boolean

</td></tr><tr><td>

sn\_isa\_model.isa\_entity.validate\_and\_generate\_locations

</td><td>

Allows display of the **Auto generate location** UI action \(UI16 and Workspace\) and the **Location Validation Map** tab \(Workspace\) in the Equipment Model form. Validates synchronization between the ISA Equipment Model Entity Hierarchy and its referenced CMN Location Hierarchy.

Automatically creates CMN Location records for each new ISA entity within the ISA Hierarchy, connecting them to the CMN Location Hierarchy.

The default is set to false.

</td><td>

Boolean

</td></tr></tbody>
</table>**Parent Topic:**[Industrial Process Manager reference](manufacturing-process-mgr-reference.md)

