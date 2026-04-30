---
title: Creation of webhooks to send inbound events to DevOps Change Velocity using token
description: You must create webhooks to send inbound events to DevOps Change Velocity using token based authentication.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a tool integration from the DevOps Change Workspace, User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Creation of webhooks to send inbound events to DevOps Change Velocity using token

You must create webhooks to send inbound events to DevOps Change Velocity using token based authentication.

To send inbound events to a ServiceNow instance, you must use the following API endpoint structure:

```
<instance_url>/api/sn_devops/v2/devops/tool/{capability}?toolId=<toolId>
```

where capability can be plan, code, or orchestration.

You can copy the details like the tool Id, instance URL, and so on by selecting **Configure manually** from the tool record or in the configure step while onboarding the tool. You can then select **Copy** in the appropriate field to copy the value to your clipboard. The field label changes to **Copied**, but you can copy multiple times. The following image displays the page from where the values can be copied for the GitHub tool in DevOps Change Velocity. ![GitHub manually configure webhooks](../image/github-manual-webhooks-2.png)

For token authentication, you must pass the token as part of the authorization header or query parameters as the endpoints are secured. You can use one of the following methods:

-   Pass the token as a header by using the following format: `Header Name: Authorization Header Value: sn_devops.DevOpsToken <ToolId>:<Token>`, where &lt;ToolId&gt; is the ID of the tool, and &lt;Token&gt; is the authentication token copied from the Tool Record page.
-   Pass the token as a query parameter in the URL: `<instance_url>/api/sn_devops/v2/devops/tool/{capability}?toolId=<toolId>&ni.nolog.token=<Token>`, where &lt;ToolId&gt; is the ID of the tool, and &lt;Token&gt; is the authentication token copied from the Tool Record page.

For Basic authentication, you can use the following V1 endpoint: `https://user:password@<instance_url>/api/sn_devops/v1/devops/tool/{capability}?toolId=<toolId>`, replace user and password with your ServiceNow credentials.

If you have a custom tool or a different authentication method, you can implement your own authentication logic. For example, you can implement an authenticateToken function in your handler class. The function should verify the token and ensure proper authentication. You must have the admin role in ServiceNow to implement your own authentication logic.

**Parent Topic:**[Create a tool integration from the DevOps Change Workspace](create-a-tool-integration-from-the-devops-change-workspace.md)

