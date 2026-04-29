---
title: Credentials troubleshooting
description: Review the &lt;credentials\_debug&gt; section of the ECC queue payload to troubleshoot issues with credentials.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Get started with credentials, Connections and Credentials, Access Management]
---

# Credentials troubleshooting

Review the `<credentials_debug>` section of the ECC queue payload to troubleshoot issues with credentials.

Certain probes support credential debugging. Credential debugging inserts a `<credentials_debug>` section in the payload that the MID Server returns to the instance ECC queue. You can view the `<credentials_debug>` section to see detailed information about the credential lookup.

The `<credentials_debug>` section appears in the payload if:

-   Credentials fail for [WMIRunner probe](https://www.servicenow.com/docs/access?context=r_WMIRunnerProbe&version=australia&pubname=australia-it-operations-management&ft:locale=en-US), [PowerShell probe](https://www.servicenow.com/docs/access?context=c_PowershellProbe&version=australia&pubname=australia-it-operations-management&ft:locale=en-US), [JMS](r_JMSCredentialsForm.md), or [SSHCommand probe](https://www.servicenow.com/docs/access?context=c_SSHCommandProbe&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).
-   You set the **credentials\_debug** parameter to **true** for the WMIRunner, PowerShell, or SSHCommand probes. If you set the parameter to true, the `<credentials_debug>` section appears even if the credential lookup is successful.

The `<credentials_debug>` section shows:

-   Information about the credential search, such as the credential types, tags, and affinities.
-   The IP address targeted.
-   Information about each credential \(in order\) that the MID Server used, including the type, classification, tag, name, Sys ID, and external credential ID if present.

![Sample payload showing invalid credentials](../image/CredentialDebuggingPayload.png "Sample payload showing invalid credentials")

Details appear for the PowerShell parameter:

-   If the local MID Server credentials were used after all the Windows credentials failed.
-   If the credentials were skipped because you are trying to discover the same machine that the MID Server is on.
-   If the [mid.powershell.use\_credentials](https://www.servicenow.com/docs/access?context=r_PowerShellForDiscovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) parameter is set to `true`.

Details appear for the SSHCommand:

-   If the credential search was skipped because the target IP is excluded.
-   If the target IP was added to the exclusion list.

**Note:** The MID Server saves IP addresses for failed credential searches in an exclusion list in cache memory. This exclusion list specifies which devices the MID Server should stop trying to access. IP addresses are added to the exclusion list after every credential has failed. The IP addresses are cleared from the exclusion list cache either after five minutes, if the MID Server is restarted, or if the credential records on the instance are updated.

