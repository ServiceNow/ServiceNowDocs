---
title: Configure Contract Management Pro MCP Server
description: Install the Contract Management Pro MCP Server application to add the contract analysis playbook tool and the Contract Analysis Playbooks menu to Contract Management Pro. The application is active by default and automatically installs its dependencies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-install-mcp-app.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
keywords: [Contract Management Pro MCP Server, Install application, MCP server, Contract negotiation, Dependencies]
breadcrumb: [Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure Contract Management Pro MCP Server

Install the Contract Management Pro MCP Server application to add the contract analysis playbook tool and the Contract Analysis Playbooks menu to Contract Management Pro. The application is active by default and automatically installs its dependencies.

## Before you begin

Review the Contract Management Pro MCP Server \(sn\_cm\_mcp\_server\) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Verify the plugin Contracts Core \(sn\_cm\_core\) is installed and active on your instance.

Role required: admin

## About this task

The Contract Management Pro MCP Server application hosts the contract analysis playbook tool and adds the **Contract Analysis Playbooks** menu to Contract Management Pro.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Contract Management Pro MCP Server \(sn\_cm\_mcp\_server\) application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    The available versions are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


## Result

The Contract Management Pro MCP Server application is installed. The contract analysis playbook tool and the **Contract Analysis Playbook** menu are available to users who have the required role.

## What to do next

After you install the application, set up the MCP server and its OAuth 2.0 authentication. For more information, see [Set up the Contract Management Pro MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-conf-mcp-server.md).

