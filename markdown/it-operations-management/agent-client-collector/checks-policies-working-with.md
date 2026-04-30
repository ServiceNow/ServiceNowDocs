---
title: Collecting data from your system devices
description: Run a check command on your server or database to gather data from those devices. Depending on the check that is invoked, collected data may be monitoring data, visibility data, log data, or user metrics.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Collecting data from your system devices

Run a check command on your server or database to gather data from those devices. Depending on the check that is invoked, collected data may be monitoring data, visibility data, log data, or user metrics.

## Policies

A policy consists of the Configuration Items \(CIs\) monitored by the Agent Client Collector, and the checks that run on those CIs. Policies define which checks to run, as well as when and on which CIs to run them.

## Checks

A policy runs a set of checks. Each check is defined with the following attributes:

-   Command to run
-   Check type
-   Command timeout
-   Plugins to be used \(`tar.gz` files that are securely and automatically downloaded to the agent\)

## Determining when checks run

Policy checks run based on one of the following scheduling models:

-   Interval-based scheduling: The minimum number of seconds between each check run. For example:

    -   An interval value is at least once per hour \(at least once every 3,600 seconds\).
    -   The agent was down during the scheduled interval when the check was to run.
    When the agent is back up, it runs the check within one hour.

    If a check interval is less than one hour, the check is executed based on the indicated amount of time since the check's most recent run. For example, for a check scheduled to run once every eight hours:

    -   The check runs at 00:00 \(midnight\)
    -   The check runs again at 08:00 \(8 AM\)
    However, if the agent is down at 8:00 and is back up at 09:03, the check runs within an hour; that is, between 09:03 and 10:03. If the check runs at 09:57, the next run is at 17:57 \(5:57 PM\). In these cases, the check picks the running time at random to ensure running of once every eight hours.

    A check completes its run when the results are sent to the MID Server \(in a MID deployment\) or ITOM Cloud Services \(ICS\) Pod \(in a MID-less deployment\).

-   Cron-based scheduling: Runs at fixed times or intervals \(for example, every day at 6:00 PM or every two hours\).

## Determining where checks run

Policies monitor the configuration items \(CIs\) that are mapped to the agent hosts. To determine the specific CI types to be monitored, you can create filters. For details on configuring policy filters, see [Create a service filter for a policy](../task/create-service-filter-policy.md).

## Updating policy mappings

When activating a policy, Agent Client Collector Framework maps monitored CIs to a policy. This policy mapping repeats every seven days after the initial mapping. Every 15 minutes \(by default\), the Agent Client Collector monitors the CMDB for any changes matching the filter conditions, and updates the mapping accordingly. To modify the frequency by which mapping between the CMDB and CI is updated, modify the sn\_agent\_sync\_filters\_interval\_min property on the System Properties page \(**All** &gt; **System Properties** &gt; **All Properties**\).

