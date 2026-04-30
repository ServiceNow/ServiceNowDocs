---
title: Integrating with Docusign
description: Integrating your Software Asset Management application with the Docusign service enables you to track your software subscriptions and to reclaim unused licenses.Register a Docusign application through the Docusign admin portal.Create an integration profile to track software subscriptions and optimize licensing for the Docusign service.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-06-23"
reading_time_minutes: 7
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Docusign

Integrating your Software Asset Management application with the Docusign service enables you to track your software subscriptions and to reclaim unused licenses.

Docusign purchases made through resellers don’t reflect within the Docusign standard billing system. So no values are returned through the APIs for envelope consumption that is available to ServiceNow.

**Important:** Docusign has removed the **lastLogin** field from the Users API, so the user's last activities are no longer tracked as part of this integration. The Software Asset Management application now creates reclamation candidates based on the subscription assigned date.

For more information about the Docusign service, see [the DocuSign Developer site](https://developers.docusign.com/ios_sdk/developer.html).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Docusign application|Authentication scopes|
|-------|----------------------------------------------|---------------------|
|Download subscriptions|admin|No scopes|
|Reclaim subscription|admin|No scopes|

## Register a Docusign application

Register a Docusign application through the Docusign admin portal.

### Before you begin

Docusign Role required: admin

### Procedure

1.  Log in to your Docusign demo \(non-production\) account.

2.  Select your profile picture.

3.  Select **My Apps and Keys**.

    -   If you already have an API integration key from a previous integration ready for use in production, [skip to step 33](integrate-with-docusign.md#docusign-prod-login).
    -   If you don't have your client secret saved, you must generate a new one.
4.  On the left pane, select **INTEGRATIONS** &gt; **Apps and Keys**.

5.  In the **Apps and Integration Keys** section, select **ADD APP AND INTEGRATION KEY**.

6.  On the Add Integration Key form, provide a name in the **App Name** field and select**CREATE APP**.

7.  Select **ADD URI** under the **Redirect URIs** field in the **Additional Settings** section.

8.  Add `https://oauth.pstmn.io/v1/browser-callback`.

9.  Select **ADD URI** again and add`https://*ServiceNow instance*.service-now.com/oauth_redirect.do`.

10. Select **ADD SECRET KEY**.

    Save the Integration Key \(Client ID\) and Secret Key \(Client secret\) in a secure location to use them later in the Postman App and the Integration Key \(Client ID\) in the ServiceNow instance.

11. Select **Save**.

12. Download the latest version of [Postman App](https://www.getpostman.com/) and skip the login.

13. Select **New Collection** and provide a name to the collection.

14. Select the **Authorization** tab.

15. From the Type list menu, select **OAuth 2.0**.

16. Provide a name and complete the fields on the **Configuration Options** tab to create a token:

    |Field|Value|
    |-----|-----|
    |Callback URL|`https://oauth.pstmn.io/v1/browser-callback`|
    |Auth URL|`https://account-d.docusign.com/oauth/auth`|
    |Access Token URL|`https://account-d.docusign.com/oauth/token`|
    |Client ID|The integration key from your Docusign demo account created in [step 10](integrate-with-docusign.md#step9).|
    |Client Secret|The secret key from your Docusign demo account [step 10](integrate-with-docusign.md#step9).|

17. Select **Get New Access Token**.

    You get redirected to Docusign.

18. Select **Accept**.

19. After the access token is collected and authentication is complete, copy the Access Token to use it later.

20. Select **New Request** to create a GET request for your account id.

21. Enter the URL in the GET field as `https://account-d.docusign.com/oauth/userinfo`.

22. On the Headers tab, select **Authorization** under **KEY** and enter `Bearer *&lt;Access Token that you copied during authentication&gt;*` under **Value**.

23. Select **Send** and verify that your request is complete.

    The account id is displayed in the response body.

24. Duplicate the GET request.

    Copy the authorization key and value under **Headers**.

25. Update the URL in the GET field as `https://demo.docusign.net/restapi/v2/accounts/<account-id>/users`.

    Here,*account-id* is the ID that you saved from the previous request.

26. Select **Send** 20 times to make 20 API calls.

    You must invoke a minimum of 20 API calls to register your application through the Docusign admin portal.

27. Navigate to **Apps and Integration Keys** on the Docusign admin portal.

28. Select **Actions** &gt; **View API Dashboard** next to your application.

29. Wait a few minutes for Docusign to register all 20 API calls.

30. Navigate to **INTEGRATIONS** &gt; **Apps and Keys** and select **Submit for review**.

    After 5-20 minutes, your application review is complete. You can promote the application to your production account.

31. Select **Actions** &gt; **Start-Go- Live review** to promote the application to the production account.

32. Select an eligible production account to manage the integration key.

33. Log in to your Docusign production content account.

34. Select your profile picture.

35. Select **Go to Admin**.

36. On the left pane, select **INTEGRATIONS** &gt; **Apps and Keys**.

    Locate your API Account ID to use for the integration profile in your ServiceNow instance.

37. Next to your application, select **Actions** &gt; **Edit**.

38. Select **ADD URI** and add`https://*ServiceNow instance*.service-now.com/oauth_redirect.do`.

39. Select **ADD SECRET KEY**.

    Save the Secret Key \(Client secret\) for your production account in a secure location to use it in your ServiceNow instance.

40. Select **Save**.


## Create a Docusign integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Docusign service.

### Before you begin

To create a Docusign integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Docusign integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d270429e864">

Interface

</th><th align="left" id="d270429e867">

Action

</th></tr></thead><tbody><tr><td id="d270429e873">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **DocuSign Integration Profile**.


</td></tr><tr><td id="d270429e915">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **DocuSign** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Display name|Name of the integration profile. For example, `DocuSign Integration`|
    |Client Id|Client ID for the OAuth application created in [step 10](integrate-with-docusign.md#step9) in the SaaS admin account.|
    |Redirect url|URL of the OAuth provider that you're redirected to after authentication. This value is automatically populated.|
    |Technical account Id|API Account ID from your Docusign production account.|
    |Instance URL|URL of the login page used for accessing your Docusign production account. This field is automatically set to **https://account.docusign.com**.|
    |Client secret|Password associated with the client ID created in [step 39](integrate-with-docusign.md#step39).|
    |Profile type|Type of integration profile. This value is automatically set to **DocuSign Subscription**.|

3.  Select **Submit**.

4.  On the integration profile, select **Get OAuth Token** and follow the steps to get an OAuth token.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-docusign.md#) table.


### Result

You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

**Note:** Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../task/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

