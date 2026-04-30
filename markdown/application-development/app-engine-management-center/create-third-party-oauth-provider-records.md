---
title: Create third-party OAuth provider records
description: Create third-party OAuth provider records to enable each of your instances to access the API endpoints you've created.
locale: en-US
release: zurich
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure OAuth credentials, Configure environment credentials, Configuration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Create third-party OAuth provider records

Create third-party OAuth provider records to enable each of your instances to access the API endpoints you've created.

## Before you begin

Complete the tasks in [Create OAuth API endpoints for external clients](create-oauth-api-endpoints-for-external-clients.md).

In the top right corner of your instance, make sure you set the application scope to **Global**.

Open all of your instances \(development, test, production, and the like\) in separate browser tabs. Begin the steps below on the production instance.

Role required: admin

## Procedure

1.  On your production instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

    You must create three records here, one for each of the three instances \(development, test, and production\). If you have any additional non-production instances \(staging, and the like\), create a record for each of those following the method shown here.

    Demonstration of how to create the first three records on your production instance

2.  Select **New**.

3.  Select **Connect to a third party OAuth Provider** to create a record for your development instance.

4.  On the form, fill in the fields.

<table id="table_dgb_1qq_fyb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter `Dev Instance Connection`.

</td></tr><tr><td>

Client ID

</td><td>

1.  On your development instance, open the Application Registry list \(**All** &gt; **System OAuth** &gt; **Application Registry**\).
2.  Open the **Pipeline Development Client** record.
3.  Copy the **Client ID**.
4.  On your production instance, paste the Client ID from your development instance into the **Client ID** field.


</td></tr><tr><td>

Client Secret

</td><td>

1.  On your development instance, open the Application Registry list \(**All** &gt; **System OAuth** &gt; **Application Registry**\).
2.  Open the **Pipeline Development Client** record.
3.  Unlock the **Client Secret** field and copy the text.
4.  On your production instance, paste the Client Secret from your development instance in the **Client Secret** field.


</td></tr><tr><td>

Default Grant type

</td><td>

Change to **Authorization code**.

</td></tr><tr><td>

Authorization URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your development instance followed by `oauth_auth.do`.
3.  Lock the field.
For example: `https://<development instance name>.service-now.com/oauth_auth.do`.

</td></tr><tr><td>

Token URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your development instance followed by `oauth_token.do`.
3.  Lock the field.
For example: `https://<development instance name>.service-now.com/oauth_token.do`.

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  Select **New**.

7.  Select **Connect to a third party OAuth Provider** to create a record for your test instance.

8.  On the form, fill in the fields.

<table id="table_tzx_fqq_fyb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter `Test Instance Connection`.

</td></tr><tr><td>

Client ID

</td><td>

1.  On your test instance, open the Application Registry list \(**All** &gt; **System OAuth** &gt; **Application Registry**\).
2.  Open the **Pipeline Test Client** record.
3.  Copy the **Client ID**.
4.  On your production instance, paste the Client ID from your test instance into the **Client ID** field.


</td></tr><tr><td>

Client Secret

</td><td>

1.  On your test instance, open the Application Registry list \(**All** &gt; **System OAuth** &gt; **Application Registry**\).
2.  Open the **Pipeline Test Client** record.
3.  Unlock the **Client Secret** field and copy the text.
4.  On your production instance, paste the Client Secret from your test instance in the **Client Secret** field.


</td></tr><tr><td>

Default Grant type

</td><td>

Change to **Authorization code**.

</td></tr><tr><td>

Authorization URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your test instance followed by `oauth_auth.do`.
3.  Lock the field.
For example: `https://<test instance name>.service-now.com/oauth_auth.do`.

</td></tr><tr><td>

Token URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your test instance followed by `oauth_token.do`.
3.  Lock the field.
For example: `https://<test instance name>.service-now.com/oauth_token.do`.

</td></tr></tbody>
</table>9.  Select **Submit**.

10. On the Application Registry list, select the **Pipeline Controller Client** record.

11. Copy the **Client ID** and paste it somewhere like a notes application.

12. Unlock the **Client Secret** field, copy the text, and paste it in a note with the Client ID.

13. Go back to the Application Registry list and select **New**.

14. Select **Connect to a third party OAuth Provider** to create a record for your production instance.

15. On the form, fill in the fields.

<table id="table_hfw_jqq_fyb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter `Prod Instance Connection`.

</td></tr><tr><td>

Client ID

</td><td>

1.  Copy the **Client ID** that you noted down.
2.  Paste the Client ID into the **Client ID** field.


</td></tr><tr><td>

Client Secret

</td><td>

1.  Copy the **Client Secret** that you noted down.
2.  Unlock the **Client Secret** field, and paste the text in the field.


</td></tr><tr><td>

Default Grant type

</td><td>

Change to **Authorization code**.

</td></tr><tr><td>

Authorization URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your production instance followed by `oauth_auth.do`.
3.  Lock the field.
For example: `https://<production instance name>.service-now.com/oauth_auth.do`.

</td></tr><tr><td>

Token URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your production instance followed by `oauth_token.do`.
3.  Lock the field.
For example: `https://<production instance name>.service-now.com/oauth_token.do`.

</td></tr></tbody>
</table>16. Select **Submit**.

    **Important:** Complete the next steps on your development instance.

17. On your development instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

    Demonstration of how to create records for your production instance on both your development and test instances

18. Select **New**.

19. Select **Connect to a third party OAuth Provider** to create a record for your production instance.

20. On the form, fill in the fields.

<table id="table_ar4_mqq_fyb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter `Prod Instance Connection`.

</td></tr><tr><td>

Client ID

</td><td>

1.  Copy the **Client ID** that you noted down.
2.  Paste the Client ID into the **Client ID** field.


</td></tr><tr><td>

Client Secret

</td><td>

1.  Copy the **Client Secret** that you noted down.
2.  Unlock the **Client Secret** field, and paste the text in the field.


</td></tr><tr><td>

Default Grant type

</td><td>

Change to **Authorization code**.

</td></tr><tr><td>

Authorization URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your production instance followed by `oauth_auth.do`.
3.  Lock the field.
For example: `https://<production instance name>.service-now.com/oauth_auth.do`.

</td></tr><tr><td>

Token URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your production instance followed by `oauth_token.do`.
3.  Lock the field.
For example: `https://<production instance name>.service-now.com/oauth_token.do`.

</td></tr></tbody>
</table>21. Select **Submit**.

    **Important:** Complete the next steps on your test instance.

22. On your test instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

23. Select **New**.

24. Select **Connect to a third party OAuth Provider** to create a record for your production instance.

25. On the form, fill in the fields.

<table id="table_irq_xqq_fyb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter `Prod Instance Connection`.

</td></tr><tr><td>

Client ID

</td><td>

1.  Copy the **Client ID** that you noted down.
2.  Paste the Client ID into the **Client ID** field.


</td></tr><tr><td>

Client Secret

</td><td>

1.  Copy the **Client Secret** that you noted down.
2.  Unlock the **Client Secret** field, and paste the text in the field.


</td></tr><tr><td>

Default Grant type

</td><td>

Change to **Authorization code**.

</td></tr><tr><td>

Authorization URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your production instance followed by `oauth_auth.do`
3.  Lock the field.
For example: `https://<production instance name>.service-now.com/oauth_auth.do`.

</td></tr><tr><td>

Token URL

</td><td>

1.  Unlock the field.
2.  Enter the URL for your production instance followed by `oauth_token.do`
3.  Lock the field.
For example: `https://<production instance name>.service-now.com/oauth_token.do`.

</td></tr></tbody>
</table>26. Select **Submit**.

27. Repeat steps 22–26 for any other non-production instances that you have \(staging, and the like\).


## What to do next

Now that you’ve completed the pre-work for using OAuth, complete all the steps in [Use OAuth to create pipeline credentials](use-oauth-to-create-pipeline-credentials.md) on the specified instances.

