---
title: Supported platforms for Agent Client Collector auto-upgrade
description: Operating systems and package types supported for Agent Client Collector auto-upgrade, and the minimum agent version required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/acc-agent-upgrade-platforms.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-05-28"
reading_time_minutes: 2
keywords: [ACC upgrade supported platforms, ACC upgrade operating systems, MSI RPM DEB PKG upgrade]
breadcrumb: [ACC-F reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Supported platforms for Agent Client Collector auto-upgrade

Operating systems and package types supported for Agent Client Collector auto-upgrade, and the minimum agent version required.

The minimum agent version for upgrade eligibility is 2.7.0 on all platforms. Agents on unsupported platforms are skipped with error code ACC-5005.

<table id="table_upgrade_platforms"><thead><tr><th>

Operating system

</th><th>

Package type

</th><th>

Requirements

</th></tr></thead><tbody><tr><td>

Windows

</td><td>

MSI

</td><td>

Agent must run as the SYSTEM account.

</td></tr><tr><td>

Linux — Red Hat, CentOS, Oracle, Rocky, Alma, CentOS Stream

</td><td>

RPM

</td><td>

Agent must run as root or have full sudo access.For information on configuring sudo access, see [Install Agent Client Collector on a Linux system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/install-acc-linux.md).

</td></tr><tr><td>

Linux — Ubuntu, Debian, GNU/Linux

</td><td>

DEB

</td><td>

Agent must run as root or have full sudo access.For information on configuring sudo access, see [Install Agent Client Collector on a Linux system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/install-acc-linux.md).

</td></tr><tr><td>

macOS — Intel \(x64\)

</td><td>

PKG

</td><td>

Agent must run as root or have full sudo access.For information on configuring sudo access, see [Manually install Agent Client Collector on macOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-install-macOS-manual.md).

</td></tr><tr><td>

macOS — Apple Silicon \(ARM64\)

</td><td>

PKG

</td><td>

Architecture is detected automatically. Agent must run as root or have full sudo access.For information on configuring sudo access, see [Manually install Agent Client Collector on macOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-install-macOS-manual.md).

</td></tr></tbody>
</table>## Non-supported platforms

Auto-upgrade is not supported on Linux SuSE, Solaris, or AIX. Agents on these platforms are skipped during upgrade runs and generate error code ACC-5005. To upgrade agents on unsupported platforms, manually install the new version on the agent host.

## Required agent permissions

Agents must run with elevated privileges on the host to perform a self-upgrade:

-   Windows: SYSTEM account
-   Linux: root user or sudoers file configuration with full sudo access
-   macOS: root user or sudoers file configuration with full sudo access

**Parent Topic:**[Agent Client Collector Framework reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/agent-client-collector-reference.md)

