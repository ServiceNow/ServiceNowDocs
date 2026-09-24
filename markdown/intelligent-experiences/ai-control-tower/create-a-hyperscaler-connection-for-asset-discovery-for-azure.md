---
title: Create a hyperscaler connection for asset discovery for Azure Foundry
description: Use the AI Control Tower workspace to create a hyperscaler connection for asset discovery from Azure Foundry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-a-hyperscaler-connection-for-asset-discovery-for-azure.html
release: brazil
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Connect to Azure from ServiceNow, Hyperscaler connection with Azure, Using AI Control Tower to create hyperscaler connections, Using AI Control Tower \(legacy\), AI Control Tower \(legacy\), Establishing AI governance, Enable AI Experiences]
---

# Create a hyperscaler connection for asset discovery for Azure Foundry

Use the AI Control Tower workspace to create a hyperscaler connection for asset discovery from Azure Foundry.

## Before you begin

Role required: admin

Ensure the plugin AI discovery \(sn\_ai\_disc\) is installed.

-   -   With Generative AI Controller application for Now Assist.
-   With AI Control Tower application.

## Procedure

1.  Login to Azure portal and ensure to activate your roles.

2.  Navigate to **All** &gt; **AI Control Tower** &gt; **Configuration** &gt; **AI discovery setup**.

3.  Select **Set up now** to create a new connection or if there are existing connection aliases, select **New**.

    AI data source new record page appears.

4.  Enter the Connection alias.

    For more information on creating a connection alias for Azure, see [Create a connection alias for Azure Foundry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-control-tower/create-a-connection-alias-for-asset-discovery-for-azure.md)

5.  Select the Source configuration: Azure

6.  Select the type as **Discovery** to discover AI assets.

7.  Select the Run frequency as **Daily**, **Weekly**, or**Monthly**.

8.  Select the Run hour of day.

    The Run hour of day depends on the Run Frequency.

9.  Save the record.

    To add the information about the AWS to the connection alias, you must create a HTTP\(s\) connection under the connection alias record. For more information about creating a new HTTP\(s\) connection for Azure see, [Create a HTTP\(s\) connection for Azure Foundry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-control-tower/create-a-http-s-connection-for-azure.md)

    The connection alias has been added to the AI discovery setup page.

10. Enter the HTTP\(s\) connection and ensure the newly created HTTP\(s\) connection appears active under Connections section on the connection and credential alias page.

    The hyperscaler connection is created, and you can view the connection on AI discovery setup. If a connection is active, it will run based on the given schedule. To manually run, select the connection alias and select **Run** to discover all the agents from Azure Foundry to AI Control Tower.

    To view all the assets discovered from Azure Foundry, see the AI asset inventory view on the AI assets page.


