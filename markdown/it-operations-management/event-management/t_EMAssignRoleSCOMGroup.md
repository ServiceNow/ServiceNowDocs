---
title: Limit collected SCOM alerts to specific SCOM groups
description: Limit the collection of SCOM alerts to only those alerts that belong to the specified SCOM group.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure alert collection from SCOM, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Limit collected SCOM alerts to specific SCOM groups

Limit the collection of SCOM alerts to only those alerts that belong to the specified SCOM group.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Use the SCOM Authoring workspace and Operations console to define a SCOM group and ensure that the group contains the required computers or instances.

    For further information about SCOM groups, see the SCOM documentation.

2.  Create a role that has a scope of the SCOM group.

3.  Add the new role to the SCOM user.

4.  Assign the role to the user defined in the credentials given to the SCOM connector instance.

5.  Remove all other roles from the user.


## Result

Only alerts from the specified SCOM group arrive at the instance.

**Parent Topic:**[Configure alert collection from SCOM](t_EMConfigureSCOMConnectorInstance.md)

