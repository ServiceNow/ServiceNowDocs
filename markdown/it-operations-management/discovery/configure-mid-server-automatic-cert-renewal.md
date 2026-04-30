---
title: Configure your MID Server for automatic certificate renewal
description: Collect information about root certificates stored outside your server. Create a specialized Discovery schedule.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 1
breadcrumb: [Configuring automated certificate renewal, Automated Certificate Renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Configure your MID Server for automatic certificate renewal

Collect information about root certificates stored outside your server. Create a specialized Discovery schedule.

## Before you begin

Role required: pki\_admin or admin

## About this task

Configure your MID Server to renew certificates automatically by setting the configuration parameters in your MID Server.

For information about version compatibility and troubleshooting, see the [Renewal of TLS certificates using AI Agents for Discovery](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB2470998) knowledge article \[KB2470998\] in the Now Support Knowledge Base. The Certificate Inventory and Management on Yokohama Patch 8 or later supports the certificate renewal agent.

## Procedure

1.  Navigate to **All** &gt; **Mid Servers**.

2.  Select the MID Server that you want to configure.

3.  Select the **Configuration Parameters** tab.

4.  Add a new parameter by selecting **New**.

5.  Select the **Parameter name** field.

6.  Select **ext.vault.hashicorp.address**

7.  In the **Value** field, enter your external Hashicorp vault address.

    The default value is http://127.0.0.1:8200.

8.  Select **Submit**

9.  Add a new parameter.

    1.  Select **New**.

    2.  Select the **Parameter name** field.

    3.  Select **ext.vault.hashicorp.path**

    4.  In the **Value** field, enter your file path in the Hashicorp vault.

    5.  Select **Submit**.

10. Navigate to the location of your host name of the MID Server

    1.  Navigate to the IP address in the **IP address** field of your MID Server record.

    2.  Navigate to the **MID Server installed folder** where you installed your MID Server.

    3.  Select the `agent/config.xml` file.

    4.  Add the parameter **ext.vault.hashicorp.token** in your cofig.xml file.

    5.  Insert the following code: `<parameter name="ext.valut.hashicorp.token" secure="true" value="<YOUR TOKEN VALUE>"/>`

    6.  Restart your MID Server.


## Result

Your MID Server is configured for automatic certificate renewal.

## What to do next

To complete the process of configuring yourself for automatic certificate renewal, you must complete the required steps to [Add the required applications and capabilities to your MID Server](add-req-apps-capabilities-to-mid-server.md) and [Configure System Properties for automatic certificate renewal](config-sys-props-for-auto-cert-renewal.md).

