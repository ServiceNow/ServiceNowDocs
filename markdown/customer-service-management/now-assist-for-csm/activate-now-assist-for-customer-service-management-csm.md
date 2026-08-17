---
title: Install ServiceNow Otto for Customer Service Management \(CSM\)
description: Install required plugins and enable ServiceNow Otto for Customer Service Management \(CSM\) to configure and use generative AI skills in Configurable Workspace and Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/activate-now-assist-for-customer-service-management-csm.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Otto for CSM, Customer Service Management]
---

# Install ServiceNow Otto for Customer Service Management \(CSM\)

Install required plugins and enable ServiceNow Otto for Customer Service Management \(CSM\) to configure and use generative AI skills in Configurable Workspace and Core UI.

## Before you begin

Role required: Admin

## About this task

To get started with AI generated skills, you must install at least one AI generated application on your instance. The AI Admin Hub can guide your implementation, starting with installation.

For information about the plugin dependencies and plugin activation order, see [Supporting information for ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-supporting-info.md).

For information about CSM Configurable Workspace, see [Set up CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-config-workspace-set-up.md). For information about AI agents, see [Install AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-ai-agents-plugins.md).

To access AI agents in the ServiceNow Otto panel, you must [turn on the panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md) and confirm that the case summarization is active on the instance.

To install the ServiceNow Otto for CSM plugin \(sn\_csm\_gen\_ai\), follow the procedure below.

## Procedure

1.  Navigate to **Admin &gt; AI Admin Hub &gt; Settings**.

2.  On the **Settings** page, select**Plugins**.

3.  Select **Get plugins** on the card for the plugin that you want to install.

4.  In the confirmation window, select Install Plugin to open the ServiceNow Store page for the plugin in a new browser tab.

5.  Install the plugin from the ServiceNow Store page.

6.  Return to the admin console.

7.  In the dialog box, select **Refresh**.

8.  Either close the dialog box to review all of your plugins or select **View all &lt;Plugin&gt; Assists and Skills** to review the features of your new plugin.

    For more detailed information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).


