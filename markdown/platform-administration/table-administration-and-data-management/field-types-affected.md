---
title: Field types affected by export controls
description: Different field types are affected differently by export controls.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data export reference, Exporting data, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Field types affected by export controls

Different field types are affected differently by export controls.

The following table describes how different field types are affected by export controls.

|Field type|Display value|Raw value|
|----------|-------------|---------|
|Date/Time|CSV: User timezone date/time with user format.|CSV: UTC timezone date/time with system format.|
|Excel/XLSX: User timezone date/time with user format if **glide.excel.use\_user\_date\_format** set, otherwise system format.|Excel/XLSX: UTC timezone date/time with user format if **glide.excel.use\_user\_date\_format** set, otherwise system format.|
|Date|Date with user format.|Date with system format.|
|Excel/XLSX: Date with user format if **glide.excel.use\_user\_date\_format** set, otherwise system format.|Excel/XLSX: Date with user format if **glide.excel.use\_user\_date\_format** set, otherwise system format.|
|Time|CSV: Time with user format.|CSV: UTC time, assuming 1970-01-01 as the date with system format.|
|Excel/XLSX: User timezone time with user format if **glide.excel.use\_user\_date\_format** set, otherwise system format.|Excel/XLSX: UTC time, assuming 1970-01-01 as the date with user format if **glide.excel.use\_user\_date\_format** set, otherwise system format.|
|References|Display value of the referenced record.|Sys\_id of the referenced record.|
|Choice|Label of the selected choice.|Value of the selected choice.|
|Currency|Value with the currency symbol.|USD value without the currency symbol.|
|Price \(calculated\)|Value with the currency symbol.|USD value without the currency symbol.|
|Price \(fixed\)|Value with the currency symbol.|USD value without the currency symbol.|

**Parent Topic:**[Data export reference](data-export-reference.md)

