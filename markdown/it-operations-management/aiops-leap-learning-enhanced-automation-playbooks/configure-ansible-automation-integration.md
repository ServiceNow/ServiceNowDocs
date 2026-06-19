---
title: Configure Ansible automation integration
description: Connect LEAP to Ansible Automation Platform so the Ansible Discovery and Execution Agents can automatically identify job templates and launch them during incident remediation.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/configure-ansible-automation-integration.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2025-01-07"
reading_time_minutes: 1
keywords: [Ansible integration, configuration, MCP server, automation]
breadcrumb: [Configuring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Configure Ansible automation integration

Connect LEAP to Ansible Automation Platform so the Ansible Discovery and Execution Agents can automatically identify job templates and launch them during incident remediation.

## Before you begin

Confirm that you have the following components installed and configured:

-   LEAP application activated
-   Ansible Automation Platform with MCP Server Console configured

    The MCP Server is the middle ware component that helps communication between LEAP and Ansible Automation Platform.

-   Network connectivity between ServiceNow and Ansible Automation Platform

Role required: **sn\_itom\_leap.leap\_admin**

## About this task

The Ansible Automation Integration requires configuration of the MCP Server Console connection and agent to enable communication between LEAP and Ansible Automation Platform.

## Procedure

1.  Navigate to **LEAP Settings** &gt; **Connectors**, and select **Connect**.

2.  Configure the Ansible MCP Server Console connection by completing these fields:

    |Field|Description|
    |-----|-----------|
    |MCP Server URL|The URL of the Ansible MCP Server Console endpoint.|
    |Authentication Method|API key authentication method.|

3.  In the Token field, enter the API token used for authentication.

4.  Assign the required roles to users who will work with Ansible integration:

    -   sn\_itom\_leap.leap\_admin = For LEAP administrators who configure step-to-job mappings
    -   sn\_itom\_leap.leap\_agent = For incident responders who execute Ansible automations
5.  Select **Save** to apply the configuration.


## Result

After you configure the Ansible Automation Integration, the Ansible discovery agent analyzes automation opportunities and identifies relevant job templates, and the Ansible execution agent launches mapped automations during incident remediation.

