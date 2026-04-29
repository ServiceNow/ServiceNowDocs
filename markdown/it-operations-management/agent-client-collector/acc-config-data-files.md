---
title: Agent Client Collector configuration data files
description: Configuration data files store dynamic instance data, such as virtual machine details, that check definitions use during execution. This ensures that checks are executed with up-to-date and accurate information about the instance being monitored.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector configuration data files

Configuration data files store dynamic instance data, such as virtual machine details, that check definitions use during execution. This ensures that checks are executed with up-to-date and accurate information about the instance being monitored.

## Configuration data files structure

-   Attachment based: A configuration data file contains a single attachment with instance data, such as Azure VM details.
-   Synchronization: When an attachment is added or deleted, the data file is synchronized across all MID Servers configured with the Agent Client Collector. If a file or its attachment is deleted, it is also removed from the MID Server.
-   Access point: The configuration data files can be accessed on the MID Server at `static/cache/config-files`.
-   Size: Configuration data files cannot be larger than 10MB.

## Check definitions used by configuration data files

-   Check definition: Individual check entries are referred to as check definitions. For instance, **os.linux.check-system-cpu** checks the CPU on Linux systems.
-   Accessing check definitions: Check definitions can be accessed from **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **Check Definitions**.

## File association

-   Download process: When a check executes, the agent downloads the configuration data file associated with that check.
-   Domain-Specific Synchronization: Files are synchronized only with agents within the same domain, ensuring secure and localized data handling.

## Working with configuration data files

Configuration data files serve as a repository for dynamic instance data that is used by check definitions when they are executed. These files ensure that checks are run with accurate, real-time information about the systems or instances being monitored. Configuration data files work as follows:

-   Store instance-specific data: Configuration data files store dynamic instance data, such as virtual machine details, server configurations, and other system-specific information. This data is used by check definitions during execution to ensure the latest information is available.
-   Create check definitions: A check definition is created with an associated configuration data file. For example, a check definition monitoring system CPU data may include configuration data detailing the system's environment, ensuring checks use accurate and relevant instance data.
-   Synchronize with MID Servers: When a configuration data file is added or updated, it synchronizes across all MID Servers communicating with the Agent Client Collector. If the file or attachment is deleted, it is also removed from the MID Servers, ensuring consistency and up-to-date data availability.
-   Execute with updated data: During execution, the Agent Client Collector agent downloads the relevant configuration data file from the MID Server. The agent uses this data to execute the check, ensuring access to the most current and accurate instance information.
-   Store and access data: Configuration data files are stored on the MID Server in the `static/cache/config-files` directory. This storage location facilitates easy access and management, ensuring the necessary data for checks is always available when needed.

**Parent Topic:**[Deploying Agent Client Collector on both servers and endpoints](acc-shared-deployment.md)

