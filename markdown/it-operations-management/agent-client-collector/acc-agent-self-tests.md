---
title: Agent Client Collector diagnostic self tests
description: The following table describes each diagnostic self-test that runs in the Agent Self Test Run \(sn\_agent\_self\_test\_run\) table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/acc-agent-self-tests.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [agent, self-test, diagnostics, validation]
breadcrumb: [ACC-F reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector diagnostic self tests

The following table describes each diagnostic self-test that runs in the Agent Self Test Run \(`sn_agent_self_test_run`\) table.

|Self-test name|Description|
|--------------|-----------|
|Allow List Validation|Checks if the allowlist is enabled and whether the allowlist file is a valid JSON file.|
|Cache Subdirectory Creation|Verifies that a user can create subdirectories in the cache directory. Required by ACC as it creates a directory per plugin.|
|MID Authentication Configuration|Checks if the MID Server authentication is configured. At least 1 authentication method is required.|
|MID Connection|Tests the connection to the MID Server over both HTTP\(S\) and WebSockets.|
|MID Connection Configuration|Checks if the MID connection is configured. At least 1 MID Server connection is required.|
|OSQuery Test|Verifies OSquery executable availability and executes a basic system query.|
|PAC File|Validates the configured PAC file is accessible and valid.|
|Powershell Version|Validates Powershell installation and version.|
|Ruby Script Execution|Verifies that the current user is able to execute a basic Ruby script.|
|Sudo SS Command Access|Validates sudo access via `ss` command.|
|WMI Permissions|Checks WMI permissions for process queries.|

**Parent Topic:**[Agent Client Collector Framework reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/agent-client-collector-reference.md)

