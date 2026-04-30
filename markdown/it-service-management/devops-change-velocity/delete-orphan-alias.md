---
title: Delete orphan connection and credential aliases
description: Delete the connection and credential aliases that do not label any connection or credential record by running a background script. This helps you in freeing up space in your system.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Delete orphan connection and credential aliases

Delete the connection and credential aliases that do not label any connection or credential record by running a background script. This helps you in freeing up space in your system.

## Before you begin

Role required: System Admin \(admin\)

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Scripts - Background**.

2.  Select the scope as **global**.

3.  Enter the following script in the **Run script \(JavaScript executed on server\)** pane.

    ```
    deleteOrphanAliases();
    function deleteOrphanAliases() {
        var orphanAliases = new GlideRecord('sys_alias');
        orphanAliases.addEncodedQuery("nameSTARTSWITHDevOps-_-");
        orphanAliases.query();
        while(orphanAliases.next()) {
            if (!checkIfAliasHasConnection(orphanAliases.getUniqueValue()))
                orphanAliases.deleteRecord();
        }
    };
    function checkIfAliasHasConnection(sysAliasId) {
        var httpToolConnGR = new GlideRecord("http_connection");
        httpToolConnGR.addEncodedQuery("connection_alias=" + sysAliasId);
        httpToolConnGR.query();
        if (httpToolConnGR.next())
            return true;
        return false;
    };
    ```

4.  Select **Run script**.


**Parent Topic:**[Managing DevOps Change Velocity](../concept/using-devops-change-velocity.md)

