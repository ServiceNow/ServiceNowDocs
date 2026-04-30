---
title: Inherit from a common control
description: After you have created a common control, you can identify other controls that can inherit protection and compliance from that common control.
locale: en-US
release: yokohama
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [RMF step 2 - Select controls for an authorization package, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Inherit from a common control

After you have created a common control, you can identify other controls that can inherit protection and compliance from that common control.

## Before you begin

Role required: sn\_irm\_cont\_auth.system owner, sn\_irm\_cont\_auth.info\_system\_sec\_officer, or sn\_irm\_cont\_auth.admin

## About this task

Consider this scenario. You and I are system owners. You own hundreds of servers and I own the facility in which they are installed. Based on the impact level of your authorization package, NIST recommends that you implement a given number of controls to protect your servers. However, you do not possess the means to implement two of them:

-   Fire protection
-   Visitor access control

You are aware that the facility has a fire suppression system, fire alarms, and smoke detectors. You also know that the facility has doors protected by a badge system. So you decide to inherit the protection in those controls from me, as well as the compliance. As long as I am compliant in terms of those controls, you are also compliant.

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **All Authorization Packages**.

2.  Open an authorization package in the Select state.

3.  Select a control that you want to inherit from a common control.

4.  Select **Inherit from Common Control**.

    ![Inherit from Common Control](../image/inherit-confirm.png)

5.  Select the common control you want to inherit protections from and select **Confirm**.

    The Inherited Controls related list now shows the control objective and the common control from which it is inheriting protection and compliance.

    ![Inherited Controls](../image/inherited-control.png)


