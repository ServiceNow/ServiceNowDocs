---
title: Password Reset Windows Application installation requirements
description: Activate the Password Reset Windows App \(Password Reset Orchestration\) \(com.glideapp.password\_reset\_desktop\) plugin and activate the Microsoft AD for Password Reset store app to use the Password Reset Windows Application.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset Windows Application installation requirements

Activate the Password Reset Windows App \(Password Reset Orchestration\) \(com.glideapp.password\_reset\_desktop\) plugin and activate the Microsoft AD for Password Reset store app to use the Password Reset Windows Application.

<table id="table_sjp_y3t_2r"><thead><tr><th>

Requirement

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Required ServiceNow release

</td><td>

Password Reset Windows Application version 5.1.4 is supported on the Yokohama, Xanadu, and Washington DC releases.

</td></tr><tr><td>

Required hardware

</td><td>

-   1 GHz or faster processor
-   512 MB of RAM
-   10 MB of available hard disk space \(x86\)
-   10 MB of available hard disk space \(x64\)

</td></tr><tr><td>

Required software

</td><td>

-   Version of Password Reset Windows Application: 5.1.4
-   Microsoft .NET Framework: 4.7.1 and newer
-   Microsoft Visual C++: Redistributable Visual Studio 2017

</td></tr><tr><td>

Supported operating systems

</td><td>

-   Windows 8.1
-   Windows 10 Enterprise
-   Windows 10 Pro
-   Windows 11

</td></tr><tr><td>

Supported processor architecture

</td><td>

-   X86
-   X64

</td></tr><tr><td>

Supported network architecture

</td><td>

-   Password Reset Windows Application clients must have direct access to both the internet and the ServiceNow instance where the Password Reset Windows Application is configured
-   For Password Reset Windows Application versions that use an SHA certificate, the corporate network must not block the SHA certificate.
-   To reset an AD password, the client must be on the corporate network.

</td></tr></tbody>
</table>**Parent Topic:**[Installing and configuring Password Reset Windows Application](../concept/install-configure-password-reset-windows-app.md)

