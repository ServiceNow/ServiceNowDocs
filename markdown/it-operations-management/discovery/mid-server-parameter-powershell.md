---
title: MID Server parameters for PowerShell
description: Parameters control the behavior of a particular MID Server and have lower precedence than MID Server properties.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [PowerShell for Discovery and Service Mapping, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# MID Server parameters for PowerShell

Parameters control the behavior of a particular MID Server and have lower precedence than MID Server properties.

The following parameters are optional.

**Note:** After changing the setting for any parameter, be sure to restart the MID Server service.

<table id="table_trv_b4r_pfb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.powershell\_api.session\_pool.max\_size

</td><td>

Specifies the maximum number of sessions allowed in the session pool.

 **Note:** Setting or changing this parameter requires restarting the MID Server.

 -   Type: Integer
-   Default value: 25

</td></tr><tr><td>

mid.powershell\_api.session\_pool.target.max\_size

</td><td>

Specifies the maximum number of sessions allowed in the pool per target host.

 **Note:** Setting or changing this parameter requires restarting the MID Server.

 -   Type: Integer
-   Default value: 3

</td></tr><tr id="MIDServerPowershell_useSSL"><td>

mid.powershell\_api.winrm.use\_ssl

</td><td>

Requires the use of SSL certificates for HTTPS connections using WinRM.-   Type: True \| False
-   Default value: false

</td></tr><tr id="MIDServerPowershell_additionalPSSessionOptions"><td>

mid.powershell\_api.winrm.additional\_pssesion\_options

</td><td>

Controls advanced options for a PSSession. For more information about advanced PSSession options, see [https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/new-pssessionoption?view=powershell-6](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/new-pssessionoption?view=powershell-6).

</td></tr><tr id="MIDServerPowershell_APIWinrmRemoteHttpsPort"><td>

mid.powershell\_api.winrm.remote\_https\_port

</td><td>

Configures the port for connecting to Windows servers using PowerShell over HTTPS. -   Type: Integer
-   Default value: 5986

</td></tr><tr id="MIDServerPowershell_APIWinrmRemotePort"><td>

mid.powershell\_api.winrm.remote\_port

</td><td>

Configures the port for connecting to Windows servers using PowerShell over HTTP. -   Type: Integer
-   Default value: 5985

</td></tr><tr id="MIDServerPowershell_skipSSLCertCheck"><td>

mid.powershell\_api.winrm.skip\_ssl\_cert\_check

</td><td>

Skips the SSL certificate check when using WinRM for HTTPS connections.-   Type: True \| False
-   Default value: false

</td></tr><tr id="MIDServerPowershell_skipSSLCertCheckOptions"><td>

mid.powershell\_api.winrm.skip\_ssl\_cert\_check\_options

</td><td>

Skips specific SSL certificate checks when using WinRM for HTTPS connections. Configure the MID Server to skip checks for certificates from a Certification Authority \(CA\), from the Common Name \(CN\) that identifies the host associated with the certificate, and for revoked certificates.

-   Type: String
-   Default value: -SkipCACheck -SkipCNCheck -SkipRevocationCheck

</td></tr><tr id="MIDServerPowershell_useCredentials"><td>

mid.powershell.use\_credentials

</td><td>

Determines the credentials to use for Discovery with PowerShell. A setting of true directs the MID Server to run probes with the Windows credentials from the credentials table. To run probes with the credentials of the user for the MID Server service, set this parameter to false.

-   Type: true \| false
-   Default value: true

</td></tr><tr id="MIDServerPowershell_UsePowerShell"><td>

mid.use\_powershell

</td><td>

Enables or disables PowerShell for Discovery. Restart the MID Server after changing the value. If PowerShell is not installed or the version installed is less than version 2.0, Discovery reverts to using WMIRunner.

-   Type: true \| false
-   Default value: true

</td></tr><tr id="MIDServerPowershell_Path"><td>

mid.powershell.path

</td><td>

Enables an administrator to point to a specific PowerShell on a MID Server in cases where more than one PowerShell is installed. Supply the path to the folder containing the PowerShell executable, for example, `C:\mypowershell` or `C:\mypowershell\`. ServiceNow automatically appends the string powershell.exe to the path. Configure this parameter when both a 32-bit and 64-bit PowerShells are active on the same MID Server, and it becomes necessary to launch the correct PowerShell for the context. 64-bit Windows employs file system redirection and the MID Server runs as a 32-bit application. If trying to specify a path in %WinDir%\\System32, Windows automatically redirects to %WinDir%\\SysWOW64. To avoid redirection, specify the path as %WinDir%\\Sysnative. For example, instead of C:\\WINDOWS\\system32\\WindowsPowerShell\\v1.0\\, specify C:\\WINDOWS\\sysnative\\WindowsPowerShell\\v1.0\\.

 **Note:** On a 64-bit version of Windows XP, a Microsoft hotfix may be required to enable this.

 To discover applications running on a 64-bit Windows machine, the MID Server must be running on a 64-bit Windows host machine.

 -   Type: string \(path\)
-   Default value: none

</td></tr><tr id="MIDServerPowershell_enforceUTF8"><td>

mid.powershell.enforce\_utf8

</td><td>

Enable this parameter to force commands on a target Windows system to return UTF-8 encoded output. Disabling it allows the target system to use its default encoding. This parameter is only valid when PowerShell is enabled.Setting this value to false may result in incorrect values in the CMDB when non-ASCII characters are returned by a probe.

 -   Type: true \| false
-   Default value: true

</td></tr><tr id="MIDServerPowershell_idleSessionTimeout"><td>

mid.powershell\_api.idle\_session\_timeout

</td><td>

Specifies the timeout value of idle PowerShell sessions in seconds.

 **Note:** Setting or changing this parameter requires restarting the MID Server.

 -   Type: Integer
-   Default value: 60

</td></tr><tr id="MIDServerPowershell_parameterPassing"><td>

mid.powershell.command.parameter\_passing

</td><td>

Enable this parameter to allow passing PowerShell parameters from the command line.-   Type: True \| False
-   Default value: false

</td></tr><tr id="MIDServerPowershell_ScriptParameterPassing"><td>

mid.powershell.command.script.parameter\_passing

</td><td>

Enable this parameter to allow passing PowerShell scripts from the command line.-   Type: True \| False
-   Default value: false

</td></tr><tr><td>

mid.windows.management\_protocol

</td><td>

Enables administrators to select the Windows management protocol used for device and process classification. Options include:

-   WMI
-   WinRM

 -   Type: String
-   Default value: WMI

</td></tr><tr><td>

mid.windows.probe\_timeout

</td><td>

Sets the timeout interval for all Windows probes on a specific MID Server. This value is overridden by the values configured for individual probes with the wmi\_timeout probe parameter.-   Type: Integer
-   Default value: 600

</td></tr></tbody>
</table>**Parent Topic:**[PowerShell for Discovery and Service Mapping](r_PowerShellForDiscovery.md)

