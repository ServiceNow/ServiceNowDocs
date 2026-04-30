---
title: License distribution in RPA Hub
description: As an administrator, you can create a robot license distribution record to define the consumption and distribution of licenses in your organization. You can create only one robot license distribution record per domain in a domain separated instance. Once you create this record, you can edit it, but you can't delete it.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# License distribution in RPA Hub

As an administrator, you can create a robot license distribution record to define the consumption and distribution of licenses in your organization. You can create only one robot license distribution record per domain in a domain separated instance. Once you create this record, you can edit it, but you can't delete it.

If the instance you are using is not domain separated, then you can create only one robot license distribution record in global domain.

For more information about creating a robot license distribution record, see [Create a robot license distribution record in RPA Hub](../task/create-lua-record.md).

For more information about executing RPA scripts, see [Execute RPA scripts to re-evaluate license distribution](../task/execute-rpa-script.md).

For unattended robots, licenses are available for the robot that is created in the current domain only. Release managers or administrators create unattended robots and associate them with Windows or virtual machines. An unattended robot is mapped to only one Windows or virtual machine.

For attended robots, licenses are available for the domain that is associated to the robot. Release managers or administrators create attended robots and associate them with users. If the auto assignment of Attended Robot property \(sn\_rpa\_fdn.allow\_rda\_robot\_auto\_assignment\) is enabled, the robot records are automatically created on a first-come, first-served basis. An attended robot is mapped to only one user.

To unassign a user, you must retire the associated attended robot. For more information, see [Unassign an attended user or group from an attended bot process in RPA Hub](../task/unassign-rda-users.md). To remove a user from a group, contact your organization.

To retire a robot if the robot machine is not working appropriately, retire the associated unattended robot. For more information, see [Retire an RPA Hub robot](../task/retire-robot.md).

You can update a robot license distribution record. For more information, see [Update a robot license distribution record in RPA Hub](../task/update-license-record-rpa.md).

