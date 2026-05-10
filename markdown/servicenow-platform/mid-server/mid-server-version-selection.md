---
title: Pinning a MID Server to a specific version
description: You can pin all the MID Servers in your environment to a specific version by setting a system property, or you can configure specific versions for individual MID Servers.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MID Server upgrades, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Pinning a MID Server to a specific version

You can pin all the MID Servers in your environment to a specific version by setting a system property, or you can configure specific versions for individual MID Servers.

**Note:** Under most circumstances, do not pin the MID Server to a specific version. Pinning the MID server can make it out of sync with the instance, and lead to broken functionality. Instead, let the instance determine which MID Server version to use.

## Version control properties

These system properties control the version for all MID Servers:

-   **mid.buildstamp**: Identifies the MID Server version with an identifier based on the date of the build. This property uses the format of **mm-dd-yyyy-hhmm**. The MID Server checks for version information hourly. If no override version is configured, the MID Server looks at the mid.buildstamp property for the version to use. This property resets itself to the default version \(the version that matches your instance version\) when the instance is restarted or upgraded, so any user changes are lost at that time. The system appends the release name and patch information to the date and time format.

    **Warning:** This property is not visible by default and should not be configured.

-   **mid.version.override**: Sets an override condition for the current version for all MID Servers in your environment. This action pins the MID Servers to a single version and disables the automatic upgrade feature. This property is not visible in the base system and must be added to the System Property \[sys\_properties\] table when it is set. For details, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

    When the MID Servers check the version each hour, they look at the mid.version.override property first. If this property is empty, the MID Servers get their version information from the mid.buildstamp property. If an override version is configured, the MID Servers use this value and ignore the version information in the mid.buildstamp property. This override value remains when the instance is restarted and is passed to the MID Servers.

    **Important:** The value in the **mid.version.override** property is cleared during an upgrade, which forces the MID Server to reset itself to the version in the mid.buildstamp property.


## Version control configuration parameter

To pin specific MID Servers on a desired version, set the **mid.pinned.version** parameter with the name of that version in the **config.xml** file of each MID Server. Use the format **&lt;version&gt;-mm-dd-yyyy**. This setting overrides the property setting for the pinned MID Server version. The MID Server version is checked every 20 minutes or whenever the MID Server restarts, at which point the pinned version is applied. For instructions, see [Add a MID Server parameter](mid-server-parameters.md#).

**Note:** The value set in this parameter is not affected by an upgrade.

**Parent Topic:**[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

