---
title: Align versions of customized probes and sensors
description: If you customized a probe or sensor and upgraded to a new version of an instance, you need to realign the versions of the customized probe and sensor to the most current version.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-08"
reading_time_minutes: 3
breadcrumb: [Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# Align versions of customized probes and sensors

If you customized a probe or sensor and upgraded to a new version of an instance, you need to realign the versions of the customized probe and sensor to the most current version.

## Before you begin

Role required: admin

## About this task

Probes and sensors have a major and a minor version.

-   **Major version**

    A major version change reflects a change in the expected output of a probe, such as the addition or subtraction of a targeted attribute, a format change, such as XML versus JSON, or a probe parameter script change.

-   **Minor version**

    A minor version change reflects small fixes that do not impact the result or the processing of the data.


A sensor and its corresponding probe must have the same major version. It is recommended they also have the same minor version. This version matching ensures that the data sent back from the probe is understood and properly processed by the sensor. All members of a multi-probes bundle must have the same major and minor version.

By default, Discovery tracks major version mismatches and displays version mismatch errors in the Active Discovery Errors section in the [Discovery Log](../reference/r_DiscoveryLog.md#). You can control whether or not Discovery tracks minor versions mismatches by setting the **Warn on Minor Version Mismatch** \(`glide.discovery.warn_minor_version`\) [Discovery property](../reference/r_DiscoveryProperties.md). Minor version mismatches are tracked in the Discovery log, but are not displayed on the Discovery Dashboard.

Versions for multi-probes and multi-sensors are checked as follows:

-   The versions of the individual probes contained in the multi-probes are compared with the Responds to Probes scripts that process their data.
-   The versions of the Responds to Probes scripts and the main multi-sensors script are compared.

If a probe and its corresponding sensor do not have the same major version, a sensor does not process information during a discovery and sends error messages to the log file. Errors also show up on the Discovery Dashboard when you run a discovery job. If the major version is the same, but the minor version is not, a sensor processes information during a discovery.

To use the most up-to-date version of a probe that is available:

## Procedure

1.  Save the customizations that you made with your probe or sensor into a text file so you can re-apply them later.

2.  Navigate to **Discovery** &gt; **Dashboard**.

3.  Look for version mismatch errors in the **Active Discovery Errors** section, and note the probe or sensor that caused the error.

4.  Navigate to **Discovery Definition** &gt; **Probes** or **Discovery Definition** &gt; **Sensors** and select the probe or sensor that you want to upgrade.

5.  Add the **Major version** and **Minor version** fields to the form if you want to display the versions on the form.

6.  In a multi-sensor, you can verify the major version with the versions of the probes that use the sensor in the **Responds to Probes** related list.

    ![This example shows matching MultiProbe and MultiSensor versions.](../image/DiscoveryProbeSensorVersion.png "Matching multi-probe and multi-sensor version")

7.  Click the **Versions** related list.

8.  Look for version where the **State** is **Previous** and the **Source** is **System upgrades**.

9.  Click the date link in the **Created** column for that version to open the version record.

10. Click **Revert to this version**.

11. Navigate back to the probe or sensor form and verify that the major version is correct.

12. Reapply your customizations to the probe or the sensor.

13. Verify that your customizations are valid with the new version of the probe or sensor by running a Discovery in your test environment.


**Parent Topic:**[Discovery probes and sensors](../concept/c_DiscoveryProbesAndSensors.md)

