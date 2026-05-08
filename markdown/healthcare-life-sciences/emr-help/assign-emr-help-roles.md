---
title: Assign roles for EMR Help users
description: Assign roles to control access to features, capabilities, and data in the EMR Help application.
locale: en-US
release: australia
product: EMR Help
classification: emr-help
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Assign roles for EMR Help users

Assign roles to control access to features, capabilities, and data in the EMR Help application.

## Before you begin

Role required: admin

## About this task

Users with the roles listed in the following table can use the EMR Help application.

<table id="table_i23_4wg_snb"><thead><tr><th>

Roles

</th><th>

Tasks

</th></tr></thead><tbody><tr><td>

sn\_ind\_rmt\_help.admin

</td><td>

Set up remote request definitions and data tables, identify scripted REST APIs for use, and configure a record producer.

</td></tr><tr><td>

sn\_ind\_rmt\_help.requester

</td><td>

Submit and monitor a ServiceNow service request from within an EMR system.

</td></tr><tr><td>

sn\_ind\_rmt\_help.viewer

</td><td>

View details of the EMR data associated with a ServiceNow service request.

 **Note:** Assign the sn\_ind\_rmt\_help.viewer role to agents who work on issues reported from the EMR system. By default, this role provides access to the EMR variables stored in EMR Request Data \[sn\_ind\_rmt\_help\_incident​\_data\] table.

</td></tr></tbody>
</table>## Procedure

-   Assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   To assign a role to a user, see Assign a role to a user.
    -   To assign a role to a group, see Assign a role to a group.

