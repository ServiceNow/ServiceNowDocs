---
title: Clear Agent Client Collector assets
description: Clear the asset and configuration file cache folder and control plugin downloads. Clearing the cache folder removes unwanted plugins that have synced to the agent.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Clear Agent Client Collector assets

Clear the asset and configuration file cache folder and control plugin downloads. Clearing the cache folder removes unwanted plugins that have synced to the agent.

## Before you begin

Ensure that the following are installed on your system:

-   Agent Client Collector Framework \(ACC-F\), starting with version 3.5.5
-   MID Server
-   CMDB
-   Agent Client Collector agent, starting with version 3.5.5
-   ACC Global Utilities

Ensure that the **disable\_assets** system property in the `acc.yml` configuration file is set to **false**.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select an agent.

3.  In the **Related Links** section, select **Clear Assets**.

4.  In the confirmation dialog box, select **Clear Agent Assets**.

5.  Select **Collect host data** to redownload your plugins from the instance.

    Plugins download automatically when used by their respective checks/policies.


