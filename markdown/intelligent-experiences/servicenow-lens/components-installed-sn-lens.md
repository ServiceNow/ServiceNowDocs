---
title: Components installed with ServiceNow AI Lens
description: Several types of components are installed with the activation of the ServiceNow AI Lens plugin, including user roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/servicenow-lens/components-installed-sn-lens.html
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Components installed with ServiceNow Lens, Roles installed with ServiceNow Lens, Tables installed with ServiceNow Lens, ServiceNow Lens roles, ServiceNow Lens tables]
breadcrumb: [Reference, ServiceNow AI Lens, Enable AI experiences]
---

# Components installed with ServiceNow AI Lens

Several types of components are installed with the activation of the ServiceNow AI Lens plugin, including user roles.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|Lens user \[lens\_user\]|Enables you to use ServiceNow AI Lens.|sn\_nowassist\_admin.user|
|Lens admin \[lens\_admin\]|Enables you to configure lens actions.|lens\_user|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lens Execution \(lens\_execution\)

</td><td>

Whenever a record is created or updated by using ServiceNow AI Lens, a record is created in the execution table. This record includes details such as the table from which the UI action is clicked and the editable fields on the form, which are then passed to the Lens app.**Note:** You can view only records created for or assigned to your user account.

</td></tr><tr><td>

Lens Transaction \(lens\_transaction\)

</td><td>

If a user performs the analyze action on the ServiceNow AI Lens app, the response received from the large language model \(LLM\) is stored in the transaction table.**Note:** You can view only records created for or assigned to your user account.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Lens reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/servicenow-lens-reference.md)

