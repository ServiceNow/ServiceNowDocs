---
title: MID Server File Cleaner
description: A monitor thread runs in the MID Server to clean up old files, to keep the size and quantity of files within the install folder manageable, and to prevent performance issues with the MID Servers.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server File Cleaner

A monitor thread runs in the MID Server to clean up old files, to keep the size and quantity of files within the install folder manageable, and to prevent performance issues with the MID Servers.

Files and empty folders within the following folders may be deleted by this MID File Cleaner. Files [last accessed](https://docs.oracle.com/javase/7/docs/api/java/nio/file/attribute/BasicFileAttributes.html#lastAccessTime%28%29) more than 30 days ago are deleted.

It runs on startup, and then every 24 hours after that. You can force the File Cleaner to run by restarting the MID Server service.

Folders/files cleaned:

-   \\agent\\import
-   \\agent\\export - Used by the Export Set feature.
-   \\agent\\work\\monitors\\ECCSender\\output\_error - Used since San Diego for ECC input payloads that cannot be inserted for any reason \(see [PRB1521761/KB0995569](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0995569)\).
-   \\agent\\work\\monitors\\ECCSender\\output\_oversize - Used since Eureka/Fuji for saving copies of payloads that are not sent to the instance because they are larger than the limit set by mid.eccq.max\_payload\_size, which defaults to 20000000 bytes \(see PRB598334\)
-   \\agent\\logs - Specifically JFR Dumps \(Utah release\)

## Logging

The MID Server agent log shows this monitor starting and shutting down with the MID Server.

```
2022-10-21T13:08:58.330+0200 INFO (MIDServer) [Main:265] Initializing MID Server 
2022-10-21T13:10:36.527+0200 INFO (StartupSequencer) [Monitors:307] Enabling monitor: FileCleanerMonitor
... 
2022-10-24T09:29:35.193+0200 INFO (MIDServer) [MIDServerState:160] MID Server stopping 
2022-10-24T09:29:38.591+0200 INFO (MIDServer) [Instance:928] interrupting thread FileCleanerMonitor.21600
```

To see exactly when it runs, enable debug with parameter `mid.log.level=debug`.

```
2022-11-17T02:49:13.201-0800 DEBUG (FileCleanerMonitor.21600) [AFileCleaner:103] Scanning directory to delete files: C:\...\agent\import
2022-11-17T02:49:13.201-0800 DEBUG (FileCleanerMonitor.21600) [AFileCleaner:103] Scanning directory to delete files: C:\...\agent\export
2022-11-17T02:49:13.201-0800 DEBUG (FileCleanerMonitor.21600) [AFileCleaner:103] Scanning directory to delete files: C:\...\agent\work\monitors\ECCSender\output_error
2022-11-17T02:49:13.201-0800 DEBUG (FileCleanerMonitor.21600) [AFileCleaner:103] Scanning directory to delete files: C:\...\agent\work\monitors\ECCSender\output_oversize
2022-11-17T02:49:13.201-0800 DEBUG (FileCleanerMonitor.21600) [AFileCleaner:103] Scanning directory to delete files: C:\...\agent\logs
```

There is no logging for individual file/folder deletes.

## Disabling the MID File Cleaner

Export Sets write files to the MID Server agent\\export folders. The idea is then that a custom implementation on the customer side takes those files and moves them elsewhere, so that these files only need to remain in the MID Server application's install directory for a short time.

The MID File Cleaner can be disabled completely for all folders, by adding the MID Server Configuration Parameter **mid.file\_cleaner.disabled=true**. When the parameter is not present, which is the out-of-box state, it defaults to false, and the file cleaner runs.

On the MID Server form, click New on the "Configuration Parameters" related list, select mid.file\_cleaner.disabled, and enter the value "true".

This can also be manually added to the config.xml file: `<parameter name="mid.file_cleaner.disabled" value="true"/>`. See [MID Server parameters](../reference/mid-server-parameters.md#) for more information.

**Parent Topic:**[MID Server reference](mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](../reference/r_MIDServerSystemRequirements.md)

[MID Server upgrades](c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](../reference/r_MIDServerTroubleshooting.md)

[MID Server dashboard](c_MIDServerDashboard.md)

[MID Server properties](../reference/r_MIDServerProperties.md#)

[MID Server parameters](../reference/mid-server-parameters.md#)

[MID Server Configuration Parameter settings and priority](../reference/mid-config-param-priority.md)

[MID Server protected records and reserved characters](../reference/mid-server-reserved-characters.md)

[MID Server privileged commands](c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](../reference/r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)

[MID Server heartbeat](../reference/r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](../task/t_PauseTheMIDServer.md#)

