---
title: Form configuration system properties
description: These system properties define the form refresh intervals for the playbook tasks.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional Security Analyst Workspace configuration, Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Form configuration system properties

These system properties define the form refresh intervals for the playbook tasks.

To configure these properties, navigate to **Analyst Workspace Setup \(New UI\)** &gt; **Analyst Workspace Properties**.

|Property|Default value|Description|
|--------|-------------|-----------|
|sn\_app\_secops\_ui.poller\_interval.playbook\_tasks|10000 ms|The interval time used by the playbook component to refresh its response tasks for every configured interval time.|
|sn\_app\_secops\_ui.poller\_interval\_count.playbook\_tasks|9 times|The number times playbook component polls for response tasks.|
|sn\_app\_secops\_ui.poller\_interval.related\_list|30000 ms|This interval time is used by the Explore component to refresh its Related List counts for every configured interval time.|

