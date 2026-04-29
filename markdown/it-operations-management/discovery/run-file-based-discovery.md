---
title: Run File-based Discovery
description: Run File-based Discovery to find all of your installed software whether it is registered or not. You can enable and configure File-based Discovery at any time using the Discovery Configuration Console.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-24"
reading_time_minutes: 2
breadcrumb: [File-based Discovery, Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Run File-based Discovery

Run File-based Discovery to find all of your installed software whether it is registered or not. You can enable and configure File-based Discovery at any time using the Discovery Configuration Console.

## Before you begin

Role required: admin

## Procedure

1.  Set up the PowerShell script.

    By default, the **filebaseddiscovery.ps1** script has a ServiceNow signature. Its certificate chain resolves up to the VeriSign Universal Root Certification Authority which is trusted by Windows by default. Since PowerShell scripts are signed by ServiceNow publisher, add ServiceNow publisher to your trusted publisher repository.

    If your Execution Policy requires you to use your own certificate or if you must make any changes to the script, re-sign the script.

    1.  Navigate to the probe “Windows - File discovery.”
    2.  Open the **filebaseddiscovey.ps1** probe parameter.
    3.  Copy the contents of the **value** field into a file.
    4.  Make the necessary changes to the file and then remove the \(old\) signature block at the end of the file.
    5.  Re-sign the script: [https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-authenticodesignature?view=powershell-6](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-authenticodesignature?view=powershell-6).

        After re-signing, the file should have a new signature block at the end of it.

    6.  Copy the entire file contents and replace the old value in the **filebaseddiscovery.ps1** probe parameter from step b.

        Windows File-based Discovery should now run using the updated signed script.

    If you're using anti-virus software, make sure to include all of the ServiceNow Windows PowerShell scripts so the anti-virus software does not see it as a threat.

2.  [Activate](https://www.servicenow.com/docs/access?context=t_RequestAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US) the File-based Discovery plugin.

3.  Enable and configure File-based Discovery.

    Using the [Discovery Configuration Console](../concept/c_DiscoveryConfigurationConsole.md#), you can enable File-based Discovery as well as configure several components to find and manage all of your installed software.

    To avoid impacting performance for existing customers, File-based Discovery is turned off by default.

4.  Configure File-based Discovery scans.

    After Discovery runs and returns file information for a configuration item \(CI\), it will not execute File-based Discovery again on that target until the interval has expired. Since there is a performance cost when File-based Discovery performs scans, it is important to determine how frequently to scan. However, choosing a more frequent interval than Monthly is not recommended due to performance considerations.

    1.  Using the [Discovery Configuration Console](../concept/c_DiscoveryConfigurationConsole.md#), expand **Common** and then enter the maximum number of files that you want to discover.

        **Note:** Increasing this value can impact performance.

    2.  Select the **Frequency** that File-based Discovery runs on the CI.

        The default is set to Monthly.

    **Note:** File-based Discovery does not trigger until initial Content Data Service \(CDS\) synchronization occurs. CDS synchronization could take approximately 24 hours for the initial set of data to be synchronized from CDS. For more information see, [File Signature Normalization](https://www.servicenow.com/docs/access?context=sam-file-based-discovery&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).


## Result

Your File-based Discovery should run based on the configurations set.

**Related topics**  


[File-based Discovery references](../reference/file-based-discovery-references.md)

