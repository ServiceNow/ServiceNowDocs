---
title: Request access to an API in API Insights
description: Request access to an API available within your organization in the API Insights workspace.
locale: en-US
release: zurich
product: API Insights
classification: api-insights
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage API data, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Request access to an API in API Insights

Request access to an API available within your organization in the API Insights workspace.

## Before you begin

The application administrator must configure an ownership group and set up a workflow for managing access requests.

Role required: sn\_api\_insights\_ws.api\_mgmt\_architect

## About this task

Alternatively, you can request access to an API managed by your team. See [Manage your team's API data in API Insights](api-insights-team-api.md),

## Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  In the **Search APIs** text box on the Overview tab, enter your search phrase and select **Search**.

3.  On the Search results page, select the **APIs** tab.

4.  Select the check box next to the **Name** column for the API for which you want to request access.

    **Note:** You can request access for only one API at a time.

5.  Select **Request access**.

6.  In the Request access dialog box, fill in the details.

<table id="table_olc_cx2_mcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Access type

</td><td>

Method used for authenticating and authorizing users or applications when interacting with an API or service. The available options are:-   **API Key**

Provides authentication using a unique token included in the request.

-   **Application**

Grants access at the application level, authenticating the application itself.

-   **Basic Auth**

Uses a base64-encoded string of credentials sent in the request header for authentication.

-   **Developer**

Offers access for individual developers or development environments.

-   **OAuth 2.0**

Employs tokens to authorize access securely, allowing applications to act on behalf of a user.

-   **Other**

Includes custom methods of authentication and authorization.

</td></tr><tr><td>

Access duration in days

</td><td>

Length of time, measured in days, for which access to an API is granted before reauthorization is needed.

</td></tr><tr><td>

Justification for your access request

</td><td>

Reason or explanation for why access to the API is needed.

</td></tr></tbody>
</table>7.  Select **Request**.


## Result

The access request is submitted for approval based on the workflow settings configured by your application administrator.

