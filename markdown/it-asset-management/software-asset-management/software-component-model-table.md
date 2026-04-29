---
title: Software Component Model table
description: The Software Component Model \[cmdb\_software\_component\_model\] table stores component model records that serves industries and use cases across different solutions on the ServiceNow Platform.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software Component Model table

The Software Component Model \[cmdb\_software\_component\_model\] table stores component model records that serves industries and use cases across different solutions on the ServiceNow Platform.

## Overview of Software Component Model table

The Software Component Model table extends from the System Component Model \[cmdb\_sw\_component\_model\] table that resides in the Data Foundation Model \(sn\_cmdb\_foundation\) application. The Software Component Model table can consist of various entities.

A software component model record is automatically created whenever a discovery model meets either of the following conditions:

-   Is normalized with a normalized version set.
-   Is manually normalized with a normalized version set.

A script runs to generate software component models from the normalized discovery models. This script uses the system property, **com.snc.sam.software\_component.choice.version\_level**, to determine the granularity of the normalized version. You can configure this system property to set the version level options, which include the following versions:

-   MAJOR
-   FULL
-   BOTH
-   NONE

**Note:** The system property is configured to the BOTH version by default. You can modify this setting by selecting any of the other available options. When entering values, ensure they are in lowercase format. As an example, to set the system property to NONE, enter "none" in the value field.

Two records are created in the Software Model Component table when a FULL version and a MAJOR version exist for the normalized discovery model. However, only one record is created if only the MAJOR version exists.

You can also manually create a software component model record in the Software Component Model \[cmdb\_software\_component\_model\] table. If you have the Software Asset Management Foundation plugin or the Software Asset Management Professional application while creating the record, you can reference the Software Product \[samp\_sw\_product\] table. If you are not using the Software Asset Management application, you need to type in the software product name.

## Upgrade information

When you upgrade to Zurich release and later releases, the scheduled job, **SAM - Generate software component model** does a one time run to generate component model records for all existing normalized discovery models which are then stored in the Software Component Model table.

After the upgrade, every time a new discovery model is normalized, the business rule,**Create software component model** that runs on the Software discovery model \[cmdb\_sam\_sw\_discovery\_model\] table gets triggered and automatically creates new software component model records for the new normalized discovery models.

**Note:** The Software Discovery Model table is available if you have Software Asset Management Foundation plugin or the Software Asset Management Professional application running on your ServiceNow instance.

## Discovery model considerations

The following are some considerations to keep in mind for discovery models:

-   System property changes: When a system property preference changes, the existing software component models retain their original settings. Only newly created version models adopt the updated system property.
-   Model deletion or modification: If you delete or modify a software component model, the system won't recreate it from the original discovery model.
-   Manual re-normalization: When a discovery model is manually normalized with new values, the existing software component model remains as is. The system creates a new software component model only if one does not already exist.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

