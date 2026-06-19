---
title: Agent installation plan steps
description: After you complete agent onboarding, the system generates an installation plan. The following table describes each step in the plan and the commands or actions required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/agent-installation-plan-steps.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# Agent installation plan steps

After you complete agent onboarding, the system generates an installation plan. The following table describes each step in the plan and the commands or actions required.

<table id="table-acc-onboarding-install-steps"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Instance configured

</td><td>

Confirms the instance is configured and ready.Marked as Completed when the criteria monitored by the check are complete.

</td></tr><tr><td>

MID Server configured

</td><td>

Confirms the MID Server is configured and ready.Marked as Completed when the criteria monitored by the check are complete.

</td></tr><tr><td>

ICS configured

</td><td>

Confirms the ITOM Cloud Service \(ICS\) is configured and ready.Marked as Completed when the criteria monitored by the check are complete.

</td></tr><tr><td>

Network connectivity verified from endpoint to MID

</td><td>

Runs the indicated command in a terminal on the endpoint to verify network connectivity before installation.

</td></tr><tr><td>

Service Account Configuration

</td><td>

Runs the indicated commands in an elevated Command Prompt on the endpoint. For the "Deny log on locally" setting, use Local Security Policy \(`secpol.msc`\).Required for Linux and macOS, optional for Windows

</td></tr><tr><td>

Installation packages downloaded for Windows

</td><td>

Runs the indicated command in an elevated Command Prompt or PowerShell, from the directory where you downloaded the .msi file.

</td></tr><tr><td>

Review and update configuration file

</td><td>

After installation, find the agent `acc.yml` configuration file and update it with your registration \(for ICS\) or API key \(for MID Server\) and verify that the default field values match your configuration. The default field values are:```
verify-plugin-signature: true
max-running-checks: 10
disable-secrets: true
disable-api: true
stated-disable: true
```

**Note:** Only the configuration options handled by the onboarding process are used.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/agent-client-collector-reference.md)

