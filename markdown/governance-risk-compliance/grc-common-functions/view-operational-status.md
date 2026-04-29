---
title: View your operational status
description: View the Operational Status modules for a list of the CIS Controls and technology Controls. Each control also includes the technology used to validate compliance, type of indicator template available, and the control's source table.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Technology Controls Monitoring Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# View your operational status

View the Operational Status modules for a list of the CIS Controls and technology Controls. Each control also includes the technology used to validate compliance, type of indicator template available, and the control's source table.

## Before you begin

Role required: admin or sn\_compliance.reader

## About this task

Starting with Version 12.0.2, the Operational Status modules provide a view of all of your CIS Controls and/or ISO 27002-based indicator templates mapped to specific CIS/ISO controls in one place. This information can be useful for monitoring your controls and the health of your system. The application is able to scan your instance and determine which controls you have implemented, along with the various technologies available for validating each control and protecting your data.

Beginning with the Australia release, Technology Controls Monitoring Accelerator provides pre-packaged CIS v8 controls and indicator templates.

## Procedure

1.  Navigate to **All** &gt; **Technology Controls Monitoring** &gt; **Operational Status**.

    You can view the module as shown in the example.

    ![Technology Controls Monitoring module.](../image/tech-controls-monitoring.png)

    **Note:** The CIS controls module is renamed from CIS controls @R to Cybersecurity Controls. The Indicator Templates module is renamed to CIS Indicator Templates.

2.  Select either **CIS Controls** or **Technology Controls**.

    **Note:** The screen shown below results from selecting **CIS Controls**. The default columns will be slightly different if you select **Technology Controls**. However, you can select the gear icon to add or remove columns as needed.

    ![Indicator templates operational status](../image/operational-status.png "Indicator templates operational status")

    Each control includes the following information.

<table id="table_uf1_qpy_c1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Controls

</td><td>

The controls included when you download and activate the Cybersecurity Controls Accelerator application.

</td></tr><tr><td>

Control family and description

</td><td>

The family and description of the control as defined in the CIS Controls.

</td></tr><tr><td>

Domain

</td><td>

Domains of the controls:-   Basic
-   Foundational
-   Organizational


</td></tr><tr><td>

Implementation Group \(IG\)

</td><td>

The implementation group to which the control is included: IG1, IG2, or IG3. IG1 covers most of the essential security controls to serve as a foundation. Then, as needed to improve your security posture, you can add IG2 and IG3 to provide additional levels of support. As illustrated here, IG2 includes all of the controls included in IG1, and IG3 includes all of the controls in IG1 and IG2.

![Implementation group hierarchy](../image/target-01.png)

</td></tr><tr><td>

Compliance validated by

</td><td>

The technology on your instance you can use to automate the validation of your controls.

</td></tr><tr><td>

Validating technology activated?

</td><td>

Identifies whether the specified technology is activated in your instance.

</td></tr><tr><td>

Controls implemented?

</td><td>

Identifies whether you have adopted the control objective and deployed it in your system.

</td></tr><tr><td>

Indicator template type

</td><td>

Identifies whether you have an indicator template type defined so you can begin validating and monitoring the control. The available types are Basic, Manual, and Script.

</td></tr><tr><td>

Source table

</td><td>

The source table for the data being monitored by the control.

</td></tr></tbody>
</table>
**Parent Topic:**[Technology Controls Monitoring Accelerator](../concept/tech-controls-monitoring-accel.md)

