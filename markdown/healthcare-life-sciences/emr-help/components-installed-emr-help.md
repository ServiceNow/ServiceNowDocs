---
title: Components installed with EMR Help
description: Several types of components are installed with activation of the EMR Help application including tables, user roles, and plugins.
locale: en-US
release: australia
product: EMR Help
classification: emr-help
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Components installed with EMR Help

Several types of components are installed with activation of the EMR Help application including tables, user roles, and plugins.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_ind\_rmt\_help.admin

</td><td id="help-admin">

Set up remote request definitions and data tables, identify scripted REST APIs for use, and configure a record producer.

</td><td>

sn\_ind\_rmt\_help.requester

</td></tr><tr><td>

sn\_ind\_rmt\_help.requester

</td><td id="help-requester">

Submit and monitor a ServiceNow service request from within an EMR system.

</td><td>

sn\_ind\_rmt\_help.viewer

</td></tr><tr><td>

sn\_ind\_rmt\_help.viewer

</td><td id="help-viewer">

View details of the EMR data associated with a ServiceNow service request.

 **Note:** Assign the sn\_ind\_rmt\_help.viewer role to agents who work on issues reported from the EMR system. By default, this role provides access to the EMR variables stored in EMR Request Data \[sn\_ind\_rmt\_help\_incident​\_data\] table.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remote Request Parameter

 \[sn\_ind\_rmt\_help\_request\_param\]

</td><td>

Contains parameters for IT service requests available to the EMR system from your ServiceNow instance.

</td></tr><tr><td>

Remote Request Data

 \[sn\_ind\_rmt\_help\_request\_data\]

</td><td>

Provides basic fields for IT service requests. You can extend this table to include more data from an IT service request.

 Each remote request parameter has a corresponding column in this table.

</td></tr><tr><td>

Remote Request Definition

 \[sn\_ind\_rmt\_help\_request\_defn\]

</td><td>

Associates a task type with a request data table and also includes the request configuration mapping.

</td></tr><tr><td>

EMR Incident Data

 \[sn\_ind\_rmt\_help\_incident\_data\]

</td><td>

Contains data from the EMR system included in IT service requests. This table extends the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table for including any task-specific data from IT service requests.

</td></tr><tr><td>

Request configuration mapping

 \[sn\_ind\_rmt\_help\_defn\_param\_data\_map\]

</td><td>

Maps request parameters with the columns in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] data table or its child table.

</td></tr></tbody>
</table>## Plugins installed

<table id="table_dyd_hpw_vnb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Encryption Support plugin \(com.glide.encryption\)

</td><td>

Encrypts table columns and attachments associated with an EMR system in an IT service request.

</td></tr></tbody>
</table>## ServiceNow Store applications installed

<table id="table_e2s_lsj_wnb"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Industry Core \(com.sn\_ind\)

</td><td>

Includes common objects, code artifacts, and request definitions for industry vertical applications.

</td></tr></tbody>
</table>**Parent Topic:**[EMR Help reference](emr-reference.md)

