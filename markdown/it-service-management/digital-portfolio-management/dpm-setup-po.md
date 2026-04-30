---
title: Configure Digital Portfolio Management to integrate with Process Mining
description: Use Process Mining in Digital Portfolio Management \(DPM\) to see the status of a key performance indicators \(KPI\) on your solutions, and adjust as needed.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2024-08-22"
reading_time_minutes: 1
breadcrumb: [Configuring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Configure Digital Portfolio Management to integrate with Process Mining

Use Process Mining in Digital Portfolio Management \(DPM\) to see the status of a key performance indicators \(KPI\) on your solutions, and adjust as needed.

Process Mining enables you to analyze and address KPI outputs for your solutions in DPM.

Administrators must complete a few steps to set up Process Mining.

## Set up Process Mining in DPM

In general, to use Process Mining in DPM, you access the KPI group and select **Initiate Process Mining**. To see that option, administrators with the dpm\_admin role must do the following.

1.  Install the ITSM Process Mining Content Pack from the ServiceNow Store. The content pack provides the following project insights and system property for Process Mining in DPM:
    -   Team performance
    -   Process Mining
    -   System property **sn\_dpm.enable.po.dpm**
2.  Set the system property **sn\_dpm.enable.po.dpm** to true. By default, the system property is set to false. Admins \[sn\_dpm.dpm\_admin\] must set the system property to true.
    1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **Administration** &gt; **Settings**.
    2.  Enter **\*enable** in the **System Properties Name** search field, and then press **Enter**.
    3.  Verify that the system property **sn\_dpm.enable.po.dpm** is set to true. If not, then select it, and set the Value field to true \(you may get a text banner that provides a link to edit the record\).
    4.  Select **Update**.

The primary role to use Process Mining is Process Mining Analyst \[process\_optimization\_analyst\]. For details about properties, roles, and scheduled jobs, see [Process Mining components for Digital Portfolio Management](../reference/dpm-po-integration.md).

**Parent Topic:**[Configuring Digital Portfolio Management](dpm-configure-cfw.md)

