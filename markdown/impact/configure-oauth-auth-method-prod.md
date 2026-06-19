---
title: Configure the OAuth authentication method production instance
description: Export OAuth records from the development instance, import them into the production instance, correct Key Management Framework \(KMF\) credential encryption, and configure development-to-production authentication so that both instances can validate their connections to each other.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-oauth-auth-method-prod.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 8
breadcrumb: [Configure the OAuth authentication method development instance, Register your instance, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Configure the OAuth authentication method production instance

Export OAuth records from the development instance, import them into the production instance, correct Key Management Framework \(KMF\) credential encryption, and configure development-to-production authentication so that both instances can validate their connections to each other.

## About this task

After the development instance is validated, see [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-oauth-auth-method.md), the production instance must be able to communicate with development, and development must be able to communicate with production. This requires two rounds of record export and import; one in each direction with KMF credential correction performed after each import.

**Important:** When OAuth records are imported into a new instance, KMF re-encrypts password fields using the receiving instance's cryptographic key. The stored values will appear jumbled and must be manually overwritten with the correct password before the connection can be validated.

## Before you begin

-   Complete [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-oauth-auth-method.md) on the development instance and confirm that the development connection validates successfully.
-   The integration user account must already exist on the production instance with the `sn_se.scan_engine_admin` and `sn_se.internal_rest_integration` roles assigned. See [Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/task-create-integration-user.md).
-   Have the integration account password available in a text editor. You will paste it multiple times during this procedure.
-   Role required: Scan Engine Admin \(`sn_se.scan_engine_admin`\).

## Procedure

1.  Stage 1 — Export OAuth records from the development instance
2.  On the development instance, navigate to **All** &gt; **Scan Engine** &gt; **My SN Instances** and open the development instance record.

3.  Select and hold \(or right-click\) the form header of the MySN instance record and select **Export** &gt; **XML**.

4.  Save the file to a local folder \(for example, `SE_Data`\).

5.  From the MySN instance record, drill into the **OAuth User Profile** field, open the linked record, and export it as XML.

6.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and filter the list to show only records scoped to **Scan Engine**.

    \[Omitted image "scan-engine-app-registry-filterout.png"\] Alt text: Application registry filtering Scan Engine scope.

    Two records should be present: `OAuth Client Dev` and `OAuth Provider Dev`.

7.  Select both records and export them together as XML.

8.  Open the **OAuth Provider Dev** record and locate the auto-generated OAuth entity profile record linked at the bottom of the form.

    \[Omitted image "scan-engine-oauthprovider-dev-profile.png"\] Alt text: OAuth Entity profile for OAuth Provider-Dev.

9.  Open the OAuth entity profile record and export it as XML.

    You should now have four XML files in your export folder:

    -   MySN instance record
    -   OAuth user profile
    -   Two application registry records \(OAuth Client Dev and OAuth Provider Dev\)
    -   OAuth entity profile record
10. Stage 2 — Prepare Key Management Framework access on the production instance
11. Log in to the production instance.

12. In the Navigator, type `key` and open **Key Management Administration**.

13. Add your user account to the selected users list and save.

    The role `sn_kmf.admin` is automatically assigned to your account.

14. Log out and log back in, then navigate to your user record.

15. In the **Roles** related list, select **Edit** and also assign `sn_kmf.cryptographic_manager`.

16. Log out and log back in to activate both KMF roles.

17. Stage 3 — Import development records into the production instance
18. On the production instance, navigate to **All** &gt; **Scan Engine** &gt; **My SN Instances**.

19. Import the four XML files in the following order, using **Import XML** for each file:

    1.  OAuth entity profile record
    2.  Second OAuth entity profile record \(if present\)
    3.  MySN instance record
    4.  OAuth user profile \(OAuth2 configuration\) record
20. Stage 4 — Correct KMF-encrypted credentials on the production instance
21. Navigate to `sys_auth_profile_oauth2.list` and open the **Integration Account** OAuth user profile record.

22. Switch the application scope to **Scan Engine**.

23. If the **Username** and **Password** fields are not visible, configure the form to display them, or open the record using the list layout.

    When prompted whether to edit in Scan Engine or Global scope, select **Global** for the form configuration only.

24. Overwrite the **Password** field with the integration account password from your text editor and select **Save**.

    Importing the record causes KMF to re-encrypt the password field with the production instance key. Overwriting it restores the correct value.

25. Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and open **OAuth Client Dev**.

26. Unlock the **Client Secret** field, overwrite it with the integration account password, and select **Save**.

27. Return to the Application Registry list and open **OAuth Provider Dev**.

28. Unlock the **Client Secret** field, overwrite it with the integration account password, and select **Save**.

29. Stage 5 — Grant KMF module access and validate the development connection
30. In the Navigator, type `key`.

31. Navigate to **All** &gt; **Key Management Framework** &gt; **Module Access Policies** &gt; **All**.

32. Filter the **Script table** column to show **Script Includes** only and locate the record named **ScanEngine API Util**.

33. Open the record, change the access decision to **Track**, and select **Save**.

34. Navigate to **All** &gt; **Scan Engine** &gt; **My SN Instances**, remove any active filters, and open the development instance record.

35. Select **Validate Connection**.

    Connection Status updates to `Connection valid`. The production instance can now communicate with the development instance. See [Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/validate-instance-connection.md) for additional information.

36. Stage 6 — Create the OAuth client and provider for the production instance
37. Confirm the application scope is set to **Scan Engine**.

38. Navigate to **All** &gt; **Scan Engine** &gt; **My SN Instances** and confirm that a MySN instance record exists for the production instance.

    If the production instance record has not been created yet, complete [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md) before continuing as follows. The record must exist before OAuth fields can be configured.

    |Field|Value|
    |-----|-----|
    |Instance Name|The instance name as it appears in `stats.do` for the production instance.|
    |URL|The full URL of the production instance.|
    |Environment|**Production**|

39. Navigate to **All** &gt; **System OAuth** &gt; **Inbound Integrations** and select **New Integration**.

40. Select **Resource Owner Password Credential Grant** and fill out the form as follows:

    |Field|Value|
    |-----|-----|
    |Name|OAuth Client Prod|
    |Provider Name|Leave empty.|
    |Client ID|Copy the auto-generated value to your text editor for use in the next step.|
    |Client Secret|Enter the integration account password.|
    |Auth Scope|**useraccount**|
    |Advanced options: Token Format|**Opaque**|

41. Select **Save**.

42. Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and select **New**.

43. Select **Connect to an OAuth Provider \(simplified\) — Outbound** and fill out the form as follows:

    |Field|Value|
    |-----|-----|
    |Name|OAuth Provider Prod|
    |Client ID|Paste the client ID copied from OAuth Client Prod.|
    |Client Secret|Enter the integration account password.|
    |Default Grant Type|Resource Owner Password Credentials|
    |Redirect URL|Select the redirect URL for the production instance. Example: https://prod.servicenow.com/oauth\_redirect.do|
    |Token URL|Use the redirect URL with the path changed to `oauth_token.do`. Example: https://prod.servicenow.com/oauth\_token.do|

44. Select **Save**.

    An OAuth entity profile record is automatically generated and appears at the bottom of the form. Leave this record as-is.

45. Stage 7 — Link OAuth records to the production MySN instance and validate
46. Navigate to **All** &gt; **Scan Engine** &gt; **My SN Instances** and open the production instance record created in [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md).

47. Configure the record as follows:

    |Field|Value|
    |-----|-----|
    |Authentication Type|OAuth|
    |OAuth Application Registry|OAuth Provider Prod|
    |OAuth User Profile|Select the existing Integration Account profile \(the same profile used for the development connection\).|

48. Select **Save**, then click **Validate Connection**.

    **Note:** Because the KMF module access policy for ScanEngine API Util was already set to **Track** in Stage 5, the connection should validate immediately without additional KMF steps. See [Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/validate-instance-connection.md) for additional information.

    Connection Status updates to `Connection valid`.

49. Stage 8 — Export production records and import into the development instance
50. From the production instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and export the following records as XML:

    -   **OAuth Client Prod**
    -   **OAuth Provider Prod**
    -   The **OAuth entity profile** auto-generated by OAuth Provider Prod
51. Export the production MySN instance record as XML.

52. Log in to the development instance and navigate to **All** &gt; **Scan Engine** &gt; **My SN Instances**.

53. Import the four XML files using **Import XML**.

54. Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and correct the KMF-encrypted client secret on both **OAuth Client Prod** and **OAuth Provider Prod** by overwriting each with the integration account password.

    See Stage 4 for the correction procedure.

55. Navigate to **All** &gt; **Scan Engine** &gt; **My SN Instances**, remove any active filters, and open the production instance record.

56. Select **Validate Connection**.

    Connection Status updates to `Connection valid`. Both instances now have valid MySN instance records for development and production.


## Result

Both the development and production instances have validated MySN instance records in each direction. Definition synchronization, update set summary synchronization, and exception reason synchronization are now available.

## What to do next

-   [Definitions integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/definitions-integrations.md)
-   [Exception reason integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/exception-reason-integration.md)
-   [User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/user-story-integration-properties.md)
-   [Deployment and synchronization integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/deployment-sync-integrations.md)

**Parent Topic:**[Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-oauth-auth-method.md)

