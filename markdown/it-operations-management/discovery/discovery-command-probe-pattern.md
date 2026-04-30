---
title: Discovery commands for probes and patterns
description: Discovery commands are used for both probe and pattern-based discovery to access configuration items \(CIs\) in your environment.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-02-20"
reading_time_minutes: 2
keywords: [discovery commands, probe commands, pattern commands]
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery commands for probes and patterns

Discovery commands are used for both probe and pattern-based discovery to access configuration items \(CIs\) in your environment.

For information about Service Mapping commands, see [Prerequisites for performing top-down discovery using Service Mapping](../../service-mapping/reference/prerequisites-service-mapping.md).

For information about MID Server privileged commands, see [MID Server privileged commands](https://www.servicenow.com/docs/access?context=c_PrivilegedCommandsForMIDServer&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Probe-based discovery

Discovery runs several different types of commands during probe-based horizontal discovery. Some of these commands require elevated privileges to run.

|Command/Permission|Resource|
|------------------|--------|
|SSH commands requiring a privileged user|[SSH commands requiring a privileged user during probe-based discovery](../reference/discovery-ssh-command-require-priv.md)|
|SSH commands not requiring a privileged user|[SSH commands not requiring a privileged user during probe-based discovery](../reference/discovery-ssh-probe-commands.md)|
|Windows commands and permissions|[Windows probes and permissions](../reference/r_DiscoWinProbesAndPermissions.md)|
|Additional permissions|[Discovery probe permissions](../reference/r_AdditionalPermissions.md)|

## Pattern-based discovery

Discovery runs several different types of commands during pattern-based horizontal discovery. Some of these commands require elevated privileges to run. For pattern-based discovery, you can view all the commands used by a specific infrastructure or application pattern on the ServiceNow AI Platform and validate them before running discovery. For cloud resource patterns, you can view all the required permissions in the Cloud Discovery patterns spreadsheet.

<table id="table_tpb_k3z_k2c"><thead><tr><th>

Action

</th><th>

Resource

</th></tr></thead><tbody><tr><td>

View commands used by infrastructure and application patterns

</td><td>

-   [View Patterns commands through the Discovery Patterns module](../task/view-command-pattern-discovery.md)\*
-   [View Patterns commands through the Command List module](../task/view-pattern-command-in-command-list.md)
-   [Command List form for pattern-based discovery](../../it-operations-management/reference/commands-list-discovery.md)

</td></tr><tr><td>

Validate commands used by infrastructure and application patterns

</td><td>

-   [Validate commands used in pattern-based discovery](../../it-operations-management/task/validate-discovery-commands.md)\*
-   [View command validation task results in pattern-based discovery](../task/view-command-validation-task-results.md)
-   [Command Validation Tasks form for pattern-based discovery](../../it-operations-management/reference/command-validation-reference.md)

</td></tr><tr><td>

View permissions required by cloud resource patterns

</td><td>

[Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx)

</td></tr></tbody>
</table>\* These tasks are exclusive to the discovery\_admin role and can't be performed by users with the pde\_viewer role.

**Related topics**  


[KB1123625: Command Validation Tool](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123625)

