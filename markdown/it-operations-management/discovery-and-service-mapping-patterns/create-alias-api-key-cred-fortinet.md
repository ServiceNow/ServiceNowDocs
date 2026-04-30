---
title: Create an alias for the API key credential for Fortinet firewall REST-based discovery
description: Create an alias and add it to an API key credential to discover Fortinet firewalls and FortiGate Virtual Domains \(VDOMs\) through REST-based discovery.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Fortinet firewall and FortiGate VDOM REST-based, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create an alias for the API key credential for Fortinet firewall REST-based discovery

Create an alias and add it to an API key credential to discover Fortinet firewalls and FortiGate Virtual Domains \(VDOMs\) through REST-based discovery.

## Before you begin

Create an API Token in Fortinet. For more information, see the [Create API Token](../reference/fortinet-fw-vdoms-rest-discovery.md#create-fortinet-api-token) prerequisite in [Fortinet firewall and FortiGate VDOM REST-based discovery](../reference/fortinet-fw-vdoms-rest-discovery.md).

Role required: discovery\_admin

## Procedure

1.  Create an alias.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Select **New**.

    3.  Enter a unique name for the alias and select **Credential** for the alias type in the **Type** field.

    4.  Select **Submit**.

2.  Configure an API key credential for the new alias.

    1.  Navigate to **Discovery** &gt; **Credentials**.

    2.  Select **New**.

    3.  Select **API Key Credentials**.

    4.  Unlock the **Credential alias** field and select the alias you created.

    5.  Configure the rest of the **API Key Credentials** form fields.

    6.  Select **Submit**.

        For more information about API Key Credentials form fields, see [API key credentials](https://www.servicenow.com/docs/access?context=API-key-credential-form&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).


## What to do next

Create a serverless schedule for Fortinet Firewall REST-based discovery. For more information, see [Create a serverless schedule for Fortinet firewall REST-based discovery](create-serverless-schedule-fortinet.md).

**Related topics**  


[Fortinet firewall and FortiGate VDOM REST-based discovery](../reference/fortinet-fw-vdoms-rest-discovery.md)

