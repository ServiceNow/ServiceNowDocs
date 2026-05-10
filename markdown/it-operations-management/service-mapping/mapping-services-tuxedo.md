---
title: Mapping application services containing Oracle Tuxedo platform
description: Service Mapping can discover application services containing Oracle Tuxedo platform and its components.Map an application service containing an Oracle Tuxedo platform and verify that Service Mapping discovered all Tuxedo components correctly.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Map a single application service using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Mapping application services containing Oracle Tuxedo platform

Service Mapping can discover application services containing Oracle Tuxedo platform and its components.

## Discovered components

<table id="table_b3m_1dn_2gb"><thead><tr><th>

Name

</th><th>

Platform

</th><th>

Version

</th><th>

Protocol

</th><th>

Discovery type

</th><th>

Pattern \(or probe if indicated\)

</th></tr></thead><tbody><tr id="TuxedoSupportedComponents"><td>

Oracle Tuxedo

</td><td>

Windows

 UNIX

</td><td>

10.x, 11.x, 12.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Tuxedo

</td></tr><tr id="TuxedoPortalSupportedComponents"><td>

Oracle Tuxedo Portal

</td><td>

Windows

 UNIX

</td><td>

10.x, 11.x, 12.x

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

Tuxedo Portal pattern

</td></tr></tbody>
</table>**Parent Topic:**[Map a single application service using classic Service Mapping](../task/t_DefineNewBusinessService.md)

## Map application services containing Oracle Tuxedo platform

Map an application service containing an Oracle Tuxedo platform and verify that Service Mapping discovered all Tuxedo components correctly.

### Before you begin

-   On the ServiceNow AI Platform, configure [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md).
-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/enable-winRM-MID-servers.md).
-   \(If hosted on Unix\) Provide a user with the elevated rights for running commands described in [Service Mapping commands requiring a privileged user](../reference/r_CommandsnCredentials.md).

Role required: service\_mapping\_admin

### Procedure

1.  Create a service instance.

    1.  Navigate to **All** &gt; **Service Mapping** &gt; **Service Instances**.

    2.  Select **New**.

        The **Discoverable by Service Mapping** option is selected by default.

    3.  In the **Name** field, enter a descriptive name for the service instance.

2.  Define the entry point for this application service:

    1.  Select the **Other Application** tile.

    2.  Select `TCP Endpoint` from the list.

    3.  Define the entry point as follows:

        -   A host of the server that hosts the Tuxedo process.
        -   A port on this server that the Tuxedo process opens.
    4.  Click **Add**.

    5.  Click **Save**.

3.  Click **Additional Info** on the left and clear the **Traffic based discovery** check box.

4.  Click **Update**.

5.  Verify that the mapping result is satisfactory:

    1.  Click **View Map** and wait until the mapping is complete.

        It may take a few minutes.

    2.  Review the application service map.


If the mapping result is not as you expected, perform basic troubleshooting.

|Symptom|Cause|Solution|
|-------|-----|--------|
|Service Mapping fails to discover the Tuxedo CI. The discovery log displays the message that states that the credentials are insufficient for running the command including "permissions.tmadadmin -v".|The provided user does not have elevated permissions for running this command.|Make sure that you provided a user with permissions to run [commands requiring elevated rights](../reference/r_CommandsnCredentials.md).|
|Service Mapping fails to discover the Tuxedo CI. The discovery log displays the message that states that the user cannot run the tux.env script.|The provided user does not have the permissions to run the tux.env script.|Make sure that you provided a user with permissions to run the tux.env script.|

