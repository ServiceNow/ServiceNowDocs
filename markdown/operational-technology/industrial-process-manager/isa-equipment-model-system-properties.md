---
title: ISA Equipment Model system properties
description: Enable the system properties for the ISA Equipment Model as needed.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: reference
last_updated: "2026-02-10"
reading_time_minutes: 1
breadcrumb: [Reference, Industrial Process Manager, Operational Technology]
---

# ISA Equipment Model system properties

Enable the system properties for the ISA Equipment Model as needed.

You can access the system properties for the ISA Equipment Model by navigating to **All** &gt; **Industrial Workspace Admin** &gt; **All OT Properties**. For more information about how to view and edit the OT system properties, see [View and edit OT system properties](../task/view-and-edit-ot-system-properties.md).

The following table describes the system properties for the ISA Equipment Model.

|System property|Description|Type|
|---------------|-----------|----|
|sn\_isa\_model.cmdb\_relationships\_sync\_levels|Number of levels of CMDB relationships that are synchronized.|Integer|
|sn\_isa\_model.short\_code\_validation\_max\_length|Maximum length for the short code validation.|Integer|
|sn\_isa\_model.excluded\_operational\_statuses|List of equipment model operational statuses that need to be filtered out from the equipment model page.|String|
|sn\_isa\_model.user\_search\_matching\_attribute|Column on the User Table \[sys\_user\] that matches with a user in the system. By default, the Email column on the User table is used.|String|
|sn\_isa\_model.user\_sites\_cache.expiry\_time|Expiration time in seconds. The default is set to 600 \(10 minutes\).|Integer|
|sn\_isa\_model.use\_user\_sites\_cache|Enables the session cache for ISA entity records.|Boolean|

**Parent Topic:**[Industrial Process Manager reference](manufacturing-process-mgr-reference.md)

