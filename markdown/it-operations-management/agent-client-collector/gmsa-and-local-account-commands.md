---
title: Account commands for LocalService, LocalSystem, and gMSA during Windows installation
description: When installing an agent on a Windows host using a LocalService, LocalSystem, or gMSA account, you must run msi commands to enable the accounts.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Account commands for LocalService, LocalSystem, and gMSA during Windows installation

When installing an agent on a Windows host using a LocalService, LocalSystem, or gMSA account, you must run msi commands to enable the accounts.

<table id="table_trf_slc_3cc"><thead><tr><th>

Account type

</th><th>

Command

</th></tr></thead><tbody><tr><td>

LocalSystem

</td><td>

```
msiexec /i C:\acc-installer.msi /qn /norestart ACC_API_KEY=<API key code> ACC_MID=<MID Server URL>/ws/events ACC_ALLOW_LIST=False LOCALUSERNAME="SYSTEM"
```

</td></tr><tr><td>

LocalService

</td><td>

```
msiexec /i C:\acc-installer.msi /qn /norestart ACC_API_KEY=<API key code> ACC_MID=<MID Server URL>/ws/events ACC_ALLOW_LIST=False LOCALUSERNAME="LOCALSERVICE"
```

</td></tr><tr><td>

gMSA

</td><td>

```
msiexec /i C:\acc-installer.msi /qn /norestart ACC_API_KEY=<API key code> ACC_MID=<MID Server URL>/ws/events ACC_ALLOW_LIST=False LOCALUSERNAME="DOMAIN\gMSA$"
```

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

