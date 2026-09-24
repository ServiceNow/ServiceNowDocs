---
title: Configure MID Server for automatic certificate renewal
description: Collect information about root certificates stored outside your server. Create a specialized Discovery schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.html
release: brazil
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configuring automated certificate renewal, Automated certificate renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Configure MID Server for automatic certificate renewal

Collect information about root certificates stored outside your server. Create a specialized Discovery schedule.

## Before you begin

Role required: pki\_admin or admin

## About this task

Configure your MID Server to renew certificates automatically by setting the configuration parameters in your MID Server.

For information about version compatibility and troubleshooting, see the [Renewal of TLS certificates using AI Agents for Discovery](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB2470998) knowledge article \[KB2470998\] in the Now Support Knowledge Base. The Certificate Inventory and Management on Yokohama Patch 8 or later supports the certificate renewal agent.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **MID Servers**.

2.  Select the MID Server that you want to configure.

3.  Select the **Configuration Parameters** tab.

4.  Add the parameters for your external vault provider.

    For each parameter, select **New**, select the **Parameter name** and **Value**, and then select **Submit**.

    |Parameter name|Value|
    |--------------|-----|
    |ext.vault.hashicorp.address|Address of your external HashiCorp vault. The default value is `http://127.0.0.1:8200`.|
    |ext.vault.hashicorp.path|File path in your HashiCorp vault.|

    |Parameter name|Value|
    |--------------|-----|
    |ext.vault.azure.keyvault.name|Name of your Azure Key Vault instance.|
    |ext.vault.azure.client.id|Application \(client\) ID of your Azure AD registered application.|
    |ext.vault.azure.tenant.id|Directory \(tenant\) ID of your Azure AD tenant.|
    |ext.vault.azure.client.secret|Client secret for your Azure AD registered application.|

    **Note:** The system caches the Azure authentication token in memory and refreshes it before expiry to maintain secure access without unnecessary token requests.

    |Parameter name|Value|
    |--------------|-----|
    |ext.vault.cyberark.pvwa.url|Base URL of your CyberArk PVWA instance.|
    |ext.vault.cyberark.pvwa.username|Username used to authenticate to CyberArk PVWA.|
    |ext.vault.cyberark.pvwa.safe\_name|Name of the CyberArk safe where private keys are stored.|
    |ext.vault.cyberark.pvwa.platform\_id|Platform ID configured in CyberArk PVWA for the stored accounts.|

5.  Add the secure credential for your external vault provider to your MID Server configuration file.

    1.  Navigate to the IP address in the **IP address** field of your MID Server record.

    2.  Navigate to the **MID Server installed folder** where you installed your MID Server.

    3.  Select the `agent/config.xml` file.

    4.  Add the parameter for your provider to your `config.xml` file.

        |Provider|Parameter|Value|
        |--------|---------|-----|
        |HashiCorp Vault|ext.vault.hashicorp.token|Your HashiCorp vault token.|
        |Azure Key Vault|ext.vault.azure.client.secret|Client secret for your Azure AD registered application.|
        |CyberArk PVWA|ext.vault.cyberark.pvwa.password|Password for your CyberArk PVWA user.|

    5.  Insert the following code, replacing the parameter name and value for your provider.

        ```
        <parameter name="Parameter" secure="true" value="<Value>"/>
        ```

        For example,

        ```
        <parameter name="ext.vault.hashicorp.token" secure="true" value="<Your token value>"/>
        ```

    6.  Restart your MID Server.


## Result

Your MID Server is configured for automatic certificate renewal.

## What to do next

To complete the process of configuring automatic certificate renewal, you must complete the required steps to [Add required applications and capabilities to MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md) and [Configure system properties for auto-renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/config-sys-props-for-auto-cert-renewal.md).

