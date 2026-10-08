---
title: Install the AI Service Graph Connector for Prisma AIRS
description: Configure the AI Service Graph Connector to integrate ServiceNow with Palo Alto Networks Prisma AIRS and import AI model inventory and security findings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/palo-alto-prisma-airs-ai-sgc-install-configure.html
release: zurich
topic_type: task
last_updated: "2026-10-06"
reading_time_minutes: 2
keywords: [Palo Alto Prisma AIRS, AI Service Graph Connector, configuration, installation]
breadcrumb: [AI Service Graph Connector for Palo Alto Prisma AIRS, Integrations, Unified Security Exposure Management, Security Operations]
---

# Install the AI Service Graph Connector for Prisma AIRS

Configure the AI Service Graph Connector to integrate ServiceNow with Palo Alto Networks Prisma AIRS and import AI model inventory and security findings.

## Before you begin

Obtain the following information from Palo Alto Networks before configuring the connection:

-   API Base URL \(default: `https://api.sase.paloaltonetworks.com`\)
-   OAuth Client ID — Provided by Palo Alto Networks
-   OAuth Client Secret — Provided by Palo Alto Networks
-   Tenant Service Group \(TSG\) ID — Provided by Palo Alto Networks

See the following topics for more information about SGC Central:

[Install a Service Graph Connector from ServiceNow Store in SGC Central](https://www.servicenow.com/docs/r/servicenow-platform/sgcc-install-store-connectors.html)

[Create a connection for a Service Graph Connector in SGC Central](https://www.servicenow.com/docs/r/servicenow-platform/sgcc-create-connection.html)

If you have not already downloaded the application to your instance, visit the ServiceNow® Store and locate the **AI Service Graph Connector for Palo Alto Prisma AIRS** application and download it onto your ServiceNow AI Platform® instance.

Role required: cmdb\_inst\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Prisma AIRS** &gt; **Setup**.

2.  Select **Create Connection** and choose **Prisma AIRS**.

3.  Complete the authentication fields.

    |Field|Description|
    |-----|-----------|
    | | |
    |API Base URL|For example, `https://api.sase.paloaltonetworks.com`|
    |Token URL|For example, `https://auth.apps.paloaltonetworks.com/oauth2/access_token`|
    |Client ID|OAuth Client ID provided by Palo Alto Networks|
    |Client Secret|OAuth Client Secret provided by Palo Alto Networks|
    |TSG ID|Tenant Service Group ID provided by Palo Alto Networks|

4.  Validate the credentials by selecting **Test Connection**.

    If Test Connection fails, verify that the Client ID, Client Secret, and TSG ID are correct.

5.  Save the connection by selecting **Submit**.


## What to do next

After creating the connection, configure the import schedules and connection properties.

|Property|Description|Default|
|--------|-----------|-------|
|Limit|Number of records returned per page|100|

Import schedules are inactive by default. Activate the ones you need from the Import Schedules module.

|Data|Frequency|
|----|---------|
|AI Models|Daily|
|Vulnerability Scans and Violations|On demand \(triggered manually or via API\)|
|Red Teaming Scans, Attacks, and Compliance|Daily|

Adding another connection for a different Prisma AIRS tenant automatically creates its own set of data sources and import schedules.

Navigate to **All** &gt; **Service Graph Connectors** &gt; **Prisma AIRS** to access Setup, Connections, Data Sources, and Import Schedules. The cmdb\_inst\_admin role is required to configure settings. The SGC viewer role allows view-only access.

**Parent Topic:**[Palo Alto Prisma AIRS AI Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/palo-alto-prisma-airs-ai-sgc.md)

