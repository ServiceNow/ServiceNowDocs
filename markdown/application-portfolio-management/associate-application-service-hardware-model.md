---
title: Associate an application service to hardware model
description: Track your equipment assets such as computers and servers using hardware models.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Associate an application service to hardware model

Track your equipment assets such as computers and servers using hardware models.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy Technology Portfolio Management module is moved to the Enterprise Architecture Workspace. To learn more, see [Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](../concept/eaw-concept/eaw-tpm.md).

Role required: sn\_apm.apm\_user

## About this task

Hardware models are configuration items with specifications for a given device model. Specifications can be size, depth, image, model, and power of the device.

**Note:** In Enterprise Architecture, only computers and servers are tracked as hardware or hardware models. Other types of hardware such as printers, network gear, peripherals, or UPS are not tracked for an application service.

Your business applications may run on multiple application services, which in turn can be installed on different types of hardware. Therefore associating application services with hardware models helps to know the risk on the Application Service due to underlying hardware.

When you run the Fetch Product Models job, the application service is automatically associated with a hardware model. The application service and the hardware product model are mapped and a record is created in the Application Service Hardware Models \[sn\_apm\_tpm\_app\_service\_hardware\_model\] table. However, you can also manually associate an application service to all hardware models, including the hardware.

After the Load TPM Risk Parameters and compute Application Service Risks scheduled job is executed, the technology risk data of the hardware model are generated and stored in Hardware Model Risks \[sn\_apm\_tpm\_hardware\_model\_risk\] table.

**Note:** As an Enterprise Architecture user, your access to the hardware product model risk table is limited to read-only. However, if you are an Enterprise Architecture administrator you can create, modify, and delete the hardware model risks in the table. Access is also read-only to Hardware \[cmdb\_ci\_hardware\], Hardware Model \[cmdb\_hardware\_product\_model\], and Hardware Model Lifecycle \[cmdb\_hardware\_model\_lifecycle\] tables.

## Procedure

1.  Navigate to **All** &gt; **Application Portfolio Management** &gt; **Technology Portfolio Management \(TPM\)** &gt; **Application Services**.

2.  Click the service record, which is the application service, to which you want to associate a hardware model.

3.  Click the **Application Service Hardware Models** related list.

4.  Click **New**.

    The Application service hardware models database table stores the application service hardware model information. You can also navigate directly to the Application Service Hardware Models table from the application navigator.

5.  On the form, fill in the fields.

    For field information, see [Application Service Hardware Models form](../reference/application-service-hardware-models-form.md).

6.  Click **Submit**.


**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

