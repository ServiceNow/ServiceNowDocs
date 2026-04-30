---
title: Create OAuth API endpoints for external clients
description: Create OAuth API endpoints to enable your controller instance to have two-way communication with your non-production instances. Follow and complete each step carefully on the specified instances before moving on to create your third-party OAuth provider records.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure OAuth credentials for use in Pipelines and Deployments, Configure environment credentials, Pipelines and Deployments configuration tasks, Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Create OAuth API endpoints for external clients

Create OAuth API endpoints to enable your controller instance to have two-way communication with your non-production instances. Follow and complete each step carefully on the specified instances before moving on to create your third-party OAuth provider records.

Demonstration of how to create OAuth API endpoints for external clients

## Before you begin

In the top right corner of your instance, make sure you set the application scope to **Global**.

Open all of your instances \(development, test, production, and the like\) in separate browser tabs.

Role required: admin

## About this task

To create OAuth API endpoints for external clients and use OAuth in your pipelines, you must create several records, each on different instances in your pipeline. Begin on your production instance, which should be your controller instance.

## Procedure

1.  On your production instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  Select **Create an OAuth API endpoint for external clients**.

4.  On the form, fill in the fields.

<table id="table_wcz_drq_fyb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter `Pipeline Controller Client`.

</td></tr><tr><td>

Redirect URLs

</td><td>

1.  Unlock the field.
2.  Enter the URL for your production, development, and test instances, each with `oauth_redirect.do` after the backslash.
3.  Lock the field.
 Separate each of the three URLs with a comma and a space. For example: `https://<production instance name>.service-now.com/oauth_redirect.do, https://<development instance name>.service-now.com/oauth_redirect.do, https://<test instance name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>5.  Select **Submit**.

    **Important:** Complete the next steps on your development instance.

6.  On your development instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

7.  Select **New**.

8.  Select **Create an OAuth API endpoint for external clients**.

9.  On the form, fill in the fields.

<table id="table_phy_3rq_fyb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter `Pipeline Development Client`.

</td></tr><tr><td>

Redirect URLs

</td><td>

1.  Unlock the field.
2.  Enter the URL for your production and development instances, each with `oauth_redirect.do` after the backslash.
3.  Lock the field.
 Separate the two URLs with a comma and a space. For example: `https://<production instance name>.service-now.com/oauth_redirect.do, https://<development instance name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>10. Select **Submit**.

    **Important:** Complete the next steps on your test instance.

11. On your test instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

12. Select **New**.

13. Select **Create an OAuth API endpoint for external clients**.

14. On the form, fill in the fields.

<table id="table_f4d_nrq_fyb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter `Pipeline Test Client`.

</td></tr><tr><td>

Redirect URLs

</td><td>

1.  Unlock the field.
2.  Enter the URL for your production and test instances, each with `oauth_redirect.do` after the backslash.
3.  Lock the field.
 Separate the two URLs with a comma and a space. For example: `https://<production instance name>.service-now.com/oauth_redirect.do, https://<test instance name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>15. Select **Submit**.

16. Repeat this process from steps 11–15 for any other non-production instances \(staging, and the like\) you have.


## What to do next

Follow the steps in [Create third-party OAuth provider records](create-third-party-oauth-provider-records.md) on the specified instances.

**Parent Topic:**[Configure OAuth credentials for use in Pipelines and Deployments](configure-oauth-credentials-pipelines-deployments.md)

