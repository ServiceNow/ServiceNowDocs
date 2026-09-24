---
title: Create a hyperscaler connection for asset discovery from AWS
description: Use the AI Control Tower workspace to create a hyperscaler connection for asset discovery from AWS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/create-a-hyperscaler-connection-for-asset-discovery-for-aws.html
release: brazil
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Connect to AWS from ServiceNow, Hyperscaler connection with AWS, Using AI Control Tower to create hyperscaler connections, Using AI Control Tower \(legacy\), AI Control Tower \(legacy\), Establishing AI governance, Enable AI Experiences]
---

# Create a hyperscaler connection for asset discovery from AWS

Use the AI Control Tower workspace to create a hyperscaler connection for asset discovery from AWS.

## Before you begin

Role required: admin

Ensure the plugin AI discovery \(sn\_ai\_disc\) is installed.

-   -   With Generative AI Controller application for Now Assist.
-   With AI Control Tower application.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Configurations** &gt; **AI discovery setup**.

2.  Select **Set up now** to create a new connection or if there are existing connection aliases, select **New**.

    AI data source record page is created.

3.  Enter the Connection alias.

    For more information on creating and configuring connection alias, see [Create a connection alias for asset discovery for AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-control-tower/create-a-connection-alias-for-ai-discovery-for-aws.md)

4.  Select the Source configuration: AWS

5.  Select the type as **Discovery** to discover AI assets.

6.  Select the Run frequency as **Daily**, **Weekly**, or **Monthly**.

7.  Select the **Run hour of day**.

    The Run hour of day depends on the Run frequency.

8.  Save the record.

    To add the information about the AWS to the connection alias, you must create a HTTP\(s\) connection under the connection alias record. For more information about creating a new HTTP\(s\) connection see, [Create a HTTP\(s\) connection for asset discovery for AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-control-tower/create-a-http-s-connection-for-ai-discovery-for-aws.md)

    The connection alias has been added to the AI discovery setup page.

9.  Enter the HTTP\(s\) connection and ensure the newly created HTTP\(s\) connection appears active under Connections on the connection and credential alias page.

    The hyperscaler connection is created, and you can view the connection on AI discovery setup.If a connection is active, it will run based on the given schedule. To manually run, select the connection alias and select run to discover all the agents from AWS to AI Control Tower.

    To view all the assets discovered from AWS, see the AI asset inventory view on the AI assets page.


