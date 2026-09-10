---
title: Enable a non-persistent virtual desktop infrastructure \(NPVDI\) agent
description: Configure an agent to enable it to work in a non-persistent virtual desktop infrastructure \(NPVDI\) environment. NPVDI agents are self-sufficient and start running checks immediately.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/enable-npvdi-agent.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-08-30"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Enable a non-persistent virtual desktop infrastructure \(NPVDI\) agent

Configure an agent to enable it to work in a non-persistent virtual desktop infrastructure \(NPVDI\) environment. NPVDI agents are self-sufficient and start running checks immediately.

## Before you begin

Ensure that you have set preliminary configurations in your ServiceNow instance, as described in [Prepare for agent deployment on a non-persistent virtual desktop infrastructure machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/npvdi-agent-instance-prep.md).

Role required: agent\_client\_collector\_user

## About this task

A non-persistent VDI \(NPVDI\) machine is deployed agent installed on its golden image. When working with an NPVDI agent, data collection begins within two minutes.

NPVDI machines have their file system and storage cleaned after each use. There is no record of previous activity on an NPVDI machine; the only indicator it retains throughout its existence is its FQDN.

## Procedure

1.  Install the agent MSI on the NPVDI gold image host using the following parameters:

    ```
    msiexec /i agent.msi NP_VDI_GOLD_IMAGE=true `
      INSTANCE_URL=<instance-url> `
      INSTANCE_REST_API_USER=<basic-auth-user> `
      INSTANCE_REST_API_PASS=<basic-auth-password> `
      REGISTRATION_KEY=<light-registration-key> `
      [PAC_FILE=<pac-url-or-path>] `
      [HTTPS_PROXY=<proxy-url>]
    ```

    For details on the MSI installation parameters, see [MSI installation parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/msi-installation-parameters.md).

    The following occurs during installation.

    1.  The installer validates the parameters.
    2.  The agent downloads the NPVDI configurations \(policies, checks, assets and config files\) from the instance.
    3.  The installer registers the agent binary as a Windows group policy \(GPO\) shutdown script.
    4.  The installer marks the agent as non-persistent, making it eligible for a golden image.

