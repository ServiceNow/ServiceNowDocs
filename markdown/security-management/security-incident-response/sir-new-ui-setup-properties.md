---
title: Legacy: Form configuration system properties
description: These system properties define the form refresh intervals for the playbook tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/sir-new-ui-setup-properties.html
release: brazil
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Legacy: Additional Security Analyst Workspace configuration, Legacy: Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Legacy: Form configuration system properties

These system properties define the form refresh intervals for the playbook tasks.

**Important:**

The Security Incident Response UI \[sn\_app\_secops\_ui\] is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Use the [Security Incident Response Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/sir-workspace-landing-page.md) instead.

To configure these properties, navigate to **Analyst Workspace Setup \(New UI\)** &gt; **Analyst Workspace Properties**.

|Property|Default value|Description|
|--------|-------------|-----------|
|sn\_app\_secops\_ui.poller\_interval.playbook\_tasks|10000 ms|The interval time used by the playbook component to refresh its response tasks for every configured interval time.|
|sn\_app\_secops\_ui.poller\_interval\_count.playbook\_tasks|9 times|The number times playbook component polls for response tasks.|
|sn\_app\_secops\_ui.poller\_interval.related\_list|30000 ms|This interval time is used by the Explore component to refresh its Related List counts for every configured interval time.|

