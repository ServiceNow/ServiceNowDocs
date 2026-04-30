---
title: Enterprise model categories and corresponding classes
description: Enterprise model categories and their corresponding Configuration Management Database \(CMDB\) configuration item \(CI\), asset, and model classes.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Enterprise model categories and corresponding classes

Enterprise model categories and their corresponding Configuration Management Database \(CMDB\) configuration item \(CI\), asset, and model classes.

## Medical model categories

|Model Category|CMDB CI Class|Asset Class|Model Class|
|--------------|-------------|-----------|-----------|
|Medical General|N/A|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Healthcare Device|cmdb\_ci\_hc\_device|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Medical Device|cmdb\_ci\_med\_device|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Patient Monitoring|cmdb\_ci\_med\_patient\_monitoring|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Patient Implants|cmdb\_ci\_med\_patient\_implant|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Surgical Instruments|cmdb\_ci\_med\_surgical\_instrument|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Clinical Devices|cmdb\_ci\_med\_clinical\_device|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Lab Equipment|cmdb\_ci\_med\_lab\_equipment|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Diagnostic Imaging|cmdb\_ci\_med\_diagnostic\_imaging|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Therapeutic Devices|cmdb\_ci\_med\_therapeutic\_device|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|
|Dental Equipment|cmdb\_ci\_med\_dental|sn\_ent\_medical\_asset|sn\_ent\_medical\_device\_model|

## Facility model categories

|Model Category|CMDB CI Class|Asset Class|Model Class|
|--------------|-------------|-----------|-----------|
|Facility General|cmdb\_ci\_facility\_hardware|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Electrical|cmdb\_ci\_power\_eq|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Automatic Transfer Switch|cmdb\_ci\_ats\_power\_eq|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Power Generator|cmdb\_ci\_generator\_power\_eq|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|UPS|cmdb\_ci\_ups\_power\_eq|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|HVAC|cmdb\_ci\_hvac|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Fuel Tank|cmdb\_ci\_fuel\_tank|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Structure|cmdb\_ci\_building\_facility|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Plumbing|N/A|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Security|cmdb\_ci\_security|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Cameras|cmdb\_ci\_ip\_camera|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|AV Displays|cmdb\_ci\_display|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|AV Equipment|cmdb\_ci\_multimedia|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Appliances|N/A|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|
|Furniture and Fixtures|N/A|sn\_ent\_facility\_asset|sn\_ent\_facility\_model|

## Transportation model categories

|Model Category|CMDB CI Class|Asset Class|Model Class|
|--------------|-------------|-----------|-----------|
|Transportation General|cmdb\_ci\_transport|sn\_ent\_transportation\_asset|sn\_ent\_transportation\_model​|
|Aircraft|cmdb\_ci\_aircraft|sn\_ent\_transportation\_asset|sn\_ent\_transportation\_model​|
|Ship|cmdb\_ci\_ship|sn\_ent\_transportation\_asset|sn\_ent\_transportation\_model​|
|Train|cmdb\_ci\_train|sn\_ent\_transportation\_asset|sn\_ent\_transportation\_model​|
|Vehicle|cmdb\_ci\_vehicle|sn\_ent\_transportation\_asset|sn\_ent\_transportation\_model​|

## Industrial model categories

|Model Category|CMDB CI Class|Asset Class|Model Class|
|--------------|-------------|-----------|-----------|
|Industrial General|cmdb\_ci\_ot|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control|cmdb\_ci\_ot\_control|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control CNC|cmdb\_ci\_ot\_cnc|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control DCS|cmdb\_ci\_ot\_dcs|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control DPU|cmdb\_ci\_ot\_dpu|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control IED|cmdb\_ci\_ot\_ied|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control 3D Printer|cmdb\_ci\_ot\_industrial\_3d\_printer|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control OPC Server|cmdb\_ci\_ot\_opc\_server|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control Module|cmdb\_ci\_ot\_control\_module|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control PLC|cmdb\_ci\_ot\_plc|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control RTU|cmdb\_ci\_ot\_rtu|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Control SCADA|cmdb\_ci\_ot\_scada\_server|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Field Device|cmdb\_ci\_ot\_field\_device|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Field Actuator|cmdb\_ci\_ot\_industrial\_actuator|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Field Drive|cmdb\_ci\_ot\_industrial\_drive|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Field Robot|cmdb\_ci\_ot\_industrial\_robot|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Field Sensor|cmdb\_ci\_ot\_industrial\_sensor|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Quality Inspection Control System|cmdb\_ci\_ot\_qics|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Supervisory|cmdb\_ci\_ot\_supervisory|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Supervisory EWS|cmdb\_ci\_ot\_ews|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Supervisory Historian|cmdb\_ci\_ot\_historian|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Supervisory HMI|cmdb\_ci\_ot\_hmi|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Supervisory OPC|cmdb\_ci\_ot\_opc\_client|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Supervisory SCADA|cmdb\_ci\_ot\_scada\_client|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|OT Supervisory System|cmdb\_ci\_ot\_supervisory|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|
|Operational Equipment|cmdb\_ci\_oe|sn\_ent\_industrial\_asset|sn\_ent\_industrial\_model​|

## Retail model categories

|Model Category|CMDB CI Class|Asset Class|Model Class|
|--------------|-------------|-----------|-----------|
|Retail General|N/A|sn\_ent\_retail\_asset|sn\_ent\_retail\_model|
|Payment Device|cmdb\_ci\_payment|sn\_ent\_retail\_asset|sn\_ent\_retail\_model|
|POS Device|cmdb\_ci\_pos|sn\_ent\_retail\_asset|sn\_ent\_retail\_model|

## Construction model categories

|Model Category|CMDB CI Class|Asset Class|Model Class|
|--------------|-------------|-----------|-----------|
|Construction General|N/A|sn\_ent\_construction\_asset​|sn\_ent\_construction\_model​|
|Construction Equipment|N/A|sn\_ent\_construction\_asset​|sn\_ent\_construction\_model​|
|Tools|N/A|sn\_ent\_construction\_asset​|sn\_ent\_construction\_model​|
|Test Tools|N/A|sn\_ent\_construction\_asset​|sn\_ent\_construction\_model​|

## Tactical equipment model categories

|Model Category|CMDB CI Class|Asset Class|Model Class|
|--------------|-------------|-----------|-----------|
|Tactical General|N/A|sn\_ent\_tactical\_asset​|sn\_ent\_tactical\_model​|
|Tactical Gear|N/A|sn\_ent\_tactical\_asset​|sn\_ent\_tactical\_model​|
|Weapons|N/A|sn\_ent\_tactical\_asset​|sn\_ent\_tactical\_model​|
|Forensic Supplies|N/A|sn\_ent\_tactical\_asset​|sn\_ent\_tactical\_model​|
|Ammunition|N/A|sn\_ent\_tactical\_asset​|sn\_ent\_tactical\_model​|

## Wearable model categories

|Model Category|CMDB CI Class|Asset Class|Model Class|
|--------------|-------------|-----------|-----------|
|Wearables General|N/A|sn\_ent\_wearable\_asset​|sn\_ent\_wearable\_model​|
|PPE|N/A|sn\_ent\_wearable\_asset​|sn\_ent\_wearable\_model​|
|Uniforms|N/A|sn\_ent\_wearable\_asset​|sn\_ent\_wearable\_model​|

**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

[Enterprise Asset Management roles](eam-roles.md)

[Mandatory fields in the bulk import spreadsheets](mandatory-bulk-fields.md)

[Normalization status for enterprise models](norm-status-eam.md)

[Model fields for Enterprise Asset Management](eam-model-fields.md)

[Contract fields for Enterprise Asset Management](contract-fields-eam.md)

[Maintenance plan fields for Enterprise Asset Management](maintenance-plan-fields-eam.md)

[Maintenance schedule fields for Enterprise Asset Management](maintenance-schedule-fields-eam.md)

[Work plan fields for Enterprise Asset Management](wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Installed with OT Asset Management](installed-with-otam.md)

[Asset put away task fields](put-away-task-form-eam.md)

