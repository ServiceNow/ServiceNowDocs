---
title: Supported Microsoft license types
description: The Software Asset Management publisher pack for Microsoft adds license metrics that are specific to Microsoft.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 12
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Supported Microsoft license types

The Software Asset Management publisher pack for Microsoft adds license metrics that are specific to Microsoft.

The license metrics are available when Microsoft is selected as the **Metric group** for the entitlement.

## Per user licenses

A per user license is used when each user accessing the software is licensed, regardless of the number of devices they use to access the software.

To define the number of installations a user has, select the **Maximum installs per right** on the Metric Attribute related list of the associated software model. If the user exceeds the number of installations you've defined, additional rights are consumed until the user is fully licensed, or there are no more rights available.

You can manage user allocations for the per user license metric. Users are assigned a quantity of rights. Even if they don't need all of the allocations, the user will consume the number of rights you've allocated to them. If a user isn't assigned to a device, a right will be consumed for each unique device with a software installation.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, a right is consumed for each unique user that has at least one installation of the software on any device assigned to them.

When a software model has downgrade or upgrade rights to another versions of a software product, rights are assigned to users with the specified versions of software installed after the primary version of the software has been fully licensed.

## Per device licenses

A per device license is used when each device accessing the software is licensed, regardless of the number of users accessing the software.

To define the number of installations a device can have, select the **Maximum installs per right** on the Metric Attribute related list of the associated software model. If the device exceeds the number of installations you've defined, additional rights are consumed until the device is fully licensed, or there are no more rights available.

You can manage device allocations for the per device license metric. Devices are assigned a quantity of rights. Even if they don't need all of the allocations, the device will consume the number of rights you've allocated to them.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, a right is consumed for each unique device that has at least one installation of the software.

When a software model has downgrade or upgrade rights to another versions of a software product, rights are assigned to users with the specified versions of software installed after the primary version of the software has been fully licensed.

## Per core licenses

A server processor is one of the main components of a server. Each server processor contains smaller processing units called cores and the number of cores your processor has is dependent on your system hardware.

System hardware runs in an operating system environment \(OSE\) and they act as middleware between the operating system and the software applications on your system. OSEs can be either physical or virtual. Depending on the OSE you have, your processor will be physical, virtual, or a combination of both.

Regardless of whether your processor is in a physical or virtual OSE, Microsoft requires that every processor core running SQL Server, Windows Server, or any of their components must be licensed. However, the number of core licenses you need will depend on whether you are licensing a physical server or an individual virtual OSE. The number of licenses you need is based on the core factor table provided by Microsoft.

**Note:** If you are licensing a Microsoft cluster that contains both physical servers and virtual OSEs, you can use cost-based licensing optimizations to determine if it is more cost-effective to license the physical servers only, virtual OSEs only, or a combination of both. See [Cost-based licensing optimization for Microsoft](../concept/cost-based-microsoft-cluster-licensing.md) for more information on these optimizations.

Use the per core license metric for any of your physical or virtual core-based licenses. If you are licensing a virtual OSE, you must use either an active Microsoft Software Assurance \(SA\) or Microsoft software subscription license.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, a check is done to see which edition of the software is installed. If the software is an Enterprise edition, a set number of rights are consumed based on the normalized core count on a physical server that has at least one installation of the Enterprise edition software in the physical operating system environment \(OSE\) or on a virtual machine \(VM\) hosted by the physical server. Another check is run to ensure that the number of OSEs that have an Enterprise edition install don't exceed the number of core rights applied to the physical server. If the number of OSEs exceeds the number of core rights, a core right will be consumed for each additional OSE. If the edition is anything but Enterprise, a right is still consumed for every core on a physical server that has at least one install in the physical OSE. The difference is the additional check. In this case, the check ensures that these other editions of software are only installed on the physical server.

If other editions of software are found in a virtual environment and no other rights are owned, then the reconciliation result will be not compliant.

You can manage device allocations. Devices are assigned a quantity of rights. Even if they don't need all of the allocations, the device will consume the number of rights you've allocated to them. For this license metric, all device allocations should be created against the physical server. No matter what edition of the software it is, if the normalized core count is less than the specified value in the **Minimum cores per processor metric** attribute related to the software model, then the minimum number of rights will be consumed.

## Per core \(with CAL\) licenses

You can manage device allocations for this license metric. Devices are assigned a quantity of rights. Even if they don't need all of the allocations, the device will consume the number of rights you've allocated to them. For example, if a device allocation with a quantity of six is created for a server, but only four core rights are needed to fully license the server, six rights would still be consumed during reconciliation. The additional two rights would be considered allocated not in use in the reconciliation results.

For the Per core \(with CAL\) license metric, device allocations can be created against a physical server or virtual machine \(VM\). Device allocations that are created against a VM must be licensed using either an active Microsoft Software Assurance \(SA\) or Microsoft software subscription license. If the core count is less than the specified value in either the **Minimum cores per processor** or **Minimum cores per server** metric attributes of the software model, the minimum number of rights will be consumed.

**Note:** If you are licensing device allocations on a Microsoft cluster that contains both physical servers and VMs, you can use cost-based licensing optimizations to determine if it is more cost-effective to license the physical servers only, VMs only, or a combination of both. See [Cost-based licensing optimization for Microsoft](../concept/cost-based-microsoft-cluster-licensing.md) for more information on these optimizations.

This license metric should be used with device or user CAL license metrics. You need to create software entitlements using those license metrics separately.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, a right is consumed for every core on a physical server that has at least one installation of the software in the physical OSE or on a virtual machine hosted by the physical server. A check runs to verify that the number of installations within an OSE and the number of active OSEs don't exceed the specified maximums you defined in the **Metric Attributes** related list on the Software Model form.

If the specified number of installs and OSEs are exceeded, core rights that are equal to the number of cores or minimum cores on either the physical server or VM will be consumed until all installs and OSEs are licensed or there are no more available rights.

## User CAL licenses

A user CAL license is a client access license \(CAL\) that allows users to access a server to use its services, regardless of the number of devices the user uses to access the services.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, the number of rights consumed is equal to total user count in all client access records related to that software model.

## Device CAL licenses

A device CAL license is a client access license \(CAL\) that allows a set number of devices to access a server to use its services, regardless of the number of users accessing the services from the device.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, the number of rights consumed is equal to total device count in all client access records related to that software model.

## Server \(per instance\) licenses

A server \(per instance\) license is used to license a set number of software installations on either a physical server or virtual machine.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, a right is consumed for the number of installations that exist in an OSE. If the number of installations in an OSE exceeds the value specified in the maximum installs per OSE metric attribute, additional rights will be consumed until all installations on a physical server or virtual machine are licensed or there are no more rights variable.

You can manage device allocations. Devices are assigned a quantity of rights. Even if the software installations, the device will consume the number of rights you've allocated to them during reconciliation. For example, if a device allocation with a quantity of two is created for a server, but only one server \(per instance\) right is needed to fully license the server, two rights would still be consumed during reconciliation. The extra right would be marked as allocated no in use in the license metric results. Device allocations can be created against physical servers or virtual machines.

## Server \(per server\) licenses

A server \(per server\) license is used to license all software installations on a physical server and any virtual machines hosted by the physical server.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, a right is consumed for every unique physical server. This license metric differs from the per device license metric, which consumes a right for every unique physical server and virtual machine that has a software installation.

You can manage device allocations. Devices are assigned a quantity of rights. Even if the software installations, the device will consume the number of rights you've allocated to them during reconciliation. For example, if a device allocation with a quantity of two is created for a server, but only one right is needed to fully license the server, two rights would still be consumed during reconciliation. The extra right would be marked as allocated not in use in the license metric results. Device allocations should be created against the physical server.

## Per Processor licenses

A per processor licenses is used to license a number of processors on a physical server.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, a right is consumed for processors on a physical server that have at least one installation of the software in the physical OSE or on a virtual machine hosted by the physical server. The quantity of processors licensed by a single right is determined by the **Maximum processor per rights** on the Metric Attribute related list of the software model.

An additional check is done to ensure that the number of installations in an OSE and the number of OSEs on a server don't exceed the specified maximums in the **Maximum installs per OSE** and **Maximum active OSEs per server** Metric Attribute related list of the software model. If any of the metric attributes are exceeded, additional rights are consumed until all processors, installs, and OSEs are licensed, or there are no more available rights. Per processor rights cannot partially license a physical server or license software installations on two different physical servers.

You can manage device allocations. Devices are assigned a quantity of rights. Even if the software installations, the device will consume the number of rights you've allocated to them during reconciliation. All device allocations should be created against the physical server.

## User Subscription licenses

User subscription licenses a user for the number of activated software subscriptions.

During reconciliation, for a software model that has one or more software entitlements that use this license metric, a right is consumed for each unique user that has at least one software subscription record associated with the software model. Any software installations that correspond with the software model will also be licensed. However, if a user has software installations, but no subscription record, that user will not consume a right and the installations will be unlicensed.

## Software Assurance licenses

Microsoft Software Assurance \(SA\) is the maintenance program used by Microsoft to provide active maintenance to its users. For more information, see [Software license maintenance](../concept/software-license-maintenance.md).

**Parent Topic:**[Software Asset Management publisher pack for Microsoft](../concept/microsoft-publisher-pack.md)

