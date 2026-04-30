---
title: Agent Client Collector configuration data files
description: Your Agent Client Collector configuration data files contain the dynamic instance data that a check definition uses when you execute a check. When you create a check definition with a configuration data file, you can view the information about your instance. For example, you could view the Azure virtual machine details that are stored in the CMDB.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-09-17"
reading_time_minutes: 1
breadcrumb: [Exploring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector configuration data files

Your Agent Client Collector configuration data files contain the dynamic instance data that a check definition uses when you execute a check. When you create a check definition with a configuration data file, you can view the information about your instance. For example, you could view the Azure virtual machine details that are stored in the CMDB.

A configuration data file contains a single attachment with the instance data. When you add or delete an attachment, the data file synchronizes with all the MID Servers that are configured to communicate with the Agent Client Collector. When you delete the configuration data file or its attachment, the attachment is also deleted from the MID Server. You can access the configuration data files on the MID Server at `\static\acc_config`. Configuration data files cannot be larger than 10MB.

Individual check entries are referred to as check definitions. For example, the **os.linux.check-system-cpu** entry that monitors the CPU data on a Linux system is referred to as a check definition in the system. You can access the check definitions from **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **Check Definitions**.

When you associate the configuration data files with a check definition, the agent downloads the file when the check executes. The files are synched only with the agents that are in the same domain.

