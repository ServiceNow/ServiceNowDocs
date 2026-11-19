---
title: Set up the Workday Financials spoke
description: Integrate the ServiceNow instance Workday instance by using the WS-Security Username Profile to authenticate ServiceNow requests.Provide the base URL of your Workday Financials instance in the Connection Details \[connection\_details\] table. Spoke actions based on the SOAP API, use these details for the action execution.Create a WS-Security Username Profile to provide your Workday credentials to authenticate requests from ServiceNow.Configure the SOAP security profile by adding the security user name profile you had created to authenticate requests from ServiceNow.Register Workday Financial spoke as the API client in your Workday account and generate client ID, client secret.Register API client in your Workday account and generate a token URL for Workday Financials spoke.Configure the system properties to enable OAuth for SOAP APIs based actions for Workday Financials spoke.Create a Basic Auth credential record to use the RaaS-report based actions. The Workday Financials spoke connection and credential alias uses these credentials to authorize actions.Create and configure a Workday Financials spoke connection to authenticate ServiceNow requests.Create and configure the To Do report to retrieve worker's finance related inbox items suc as, to-dos, action items, approval, and so on.Create and configure the Ledger Account report to retrieve the ledger account details.Create and configure the Payment Status report to retrieve the supplier payment information within the specified date range.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/setup-workday-fin-spoke.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Workday Financials Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Workday Financials spoke

Integrate the ServiceNow instance Workday instance by using the WS-Security Username Profile to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Workday Financials spoke.
-   Role required: admin

## Provide the Workday Financials base URL

Provide the base URL of your Workday Financials instance in the Connection Details \[connection\_details\] table. Spoke actions based on the SOAP API, use these details for the action execution.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Filter and search for the Connection Details table.

3.  Click the **Show List** related list.

4.  Click **New**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Base URL|Base URL of the Workday instance or tenant name.|
    |Version|Version of the API. For example, enter `v33.2`.|

6.  Click **Save**.


## Create a WS-Security Username Profile for the Workday Financials spoke

Create a WS-Security Username Profile to provide your Workday credentials to authenticate requests from ServiceNow.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **SOAP Integrations** &gt; **WS-Security Username Profiles**.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify this credential. For example, enter `WorkdayFinancials User`.|
    |Application|Application in which the record is applicable. Select **Workday Financials Spoke**.|
    |Username|Workday user who has integration rights using Workday Web Services.|
    |Password|Password of the Workday user.|

4.  Click **Save**.


## Configure the SOAP security policy for the Workday Financials spoke

Configure the SOAP security profile by adding the security user name profile you had created to authenticate requests from ServiceNow.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **SOAP Integrations** &gt; **SOAP Security Policies**.

2.  Open the record, **WorkdayFinancials**.

3.  For **WS-Security Username Profile**, select the security username profile you had created for the Workday Financials spoke.

    See [Create a WS-Security Username Profile for the Workday Financials spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-workday-fin-spoke.md) for more information.

4.  Do not provide value in **WS-Security X.509 Profile**.

5.  Right-click the form header and click **Save**.


## Generate client ID and client secret for Workday Financials spoke

Register Workday Financial spoke as the API client in your Workday account and generate client ID, client secret.

### Before you begin

Role required: admin

### Procedure

1.  Log into your Workday tenant.

2.  Navigate to Search and enter `Register API Client for Integrations` task. \[Omitted image "wkdy-fin-reg-api-client-integ.png"\] Alt text: Search for Register API client for integrations in Workday account

3.  On the Register API Client for Integrations form, fill in the details.

    |Field|Description|
    |-----|-----------|
    |Client Name|Client name of the app. For example, enter `Workday Financials spoke`.|
    |Non-expiring Refresh Tokens|Option to enable refresh tokens that do not expire.|
    |Scope \(Functional Areas\)|Select the required functional areas.|
    |Include Workday Owned Scope|Option to select Workday owned scope.|

    \[Omitted image "wkday-reg-api-client-screen.png"\] Alt text: Fields in Register API Client for integrations screen

4.  Click **OK**.

    Client ID and Client Secret are generated after the registration is successful.\[Omitted image "wkday-fin-client-id-sec-generated.png"\] Alt text: Client ID and client secret generated after API client registration

5.  Click the ellipsis button after the specified client name.\[Omitted image "wkday-mng-refresh-token-nav.png"\] Alt text: Navigating Manage Refresh Tokens for Integrations option

6.  Select **API Client** &gt;**Manage Refresh Tokens for Integrations**.

7.  Select your Workday Account and click **OK**.

    Delete or Regenerate Refresh Token screen displays.

8.  Select **Generate New Refresh Token** option and click **OK**.\[Omitted image "wkday-fin-refresh-tkn.png"\] Alt text: Refresh token generated in Workday account


### Result

A new refresh token is generated. Copy and store the refresh token for configuring system property.

## Generate token URL for Workday Financials spoke

Register API client in your Workday account and generate a token URL for Workday Financials spoke.

### Before you begin

Role required: admin

### Procedure

1.  Log into your Workday tenant.

2.  Navigate to Search and enter `Register API Client` task.

3.  On the Register API Client, fill in the details.

    |Field|Description|
    |-----|-----------|
    |Client Name|Client name of the app. For example, `Workday Financials spoke`.|
    |Client Grant Type|Select Authorisation Code Grant.|
    |Access Token Type|Access Token Type: Select Bearer|
    |Redirection URI|Enter your ServiceNow URL in this format: `https://<instance>.service-now.com/oauth_redirect.do`.|
    |Non-Expiring Refresh tokens|Option to enable refresh tokens which do not expire.|
    |Scope \(Functional Areas\)|Select the required functional areas.|
    |Include Workday Owned Scope|Option to select scope that are owned by Workday.|

4.  Click **OK**.


### Result

Copy and store the generated Token Endpoint value for configuring system property.

## Configure system properties for Workday Financials spoke

Configure the system properties to enable OAuth for SOAP APIs based actions for Workday Financials spoke.

### Before you begin

-   [Generate client ID and client secret for Workday Financials spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-workday-fin-spoke.md)
-   [Generate token URL for Workday Financials spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-workday-fin-spoke.md)
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the **Application** column, search for `Workday Financials Spoke`.

3.  Open the **sn\_workdayfin\_spke.glide.hub.clientid** system property.

4.  Enter the Client ID generated from the Workday account in the **Value** field and click **Update**.

5.  Open the **sn\_workdayfin\_spke.glide.hub.clientsecret** system property.

6.  Enter the Client secret generated from the Workday account in the **Value** field and click **Update**.

7.  Open the **sn\_workdayfin.glide.hub.refreshtoken** system property.

8.  Enter the refresh token generated from the Workday account in the **Value** field and click **Update**.

9.  Open the **sn\_workdayfin\_spke.glide.hub.tokenurl** system property.

10. Enter the token URL generated from the Workday account in the **Value** field and click **Update**.


### Result

The required system properties are configured for the Workday Financials spoke.

## Create a credential record

Create a Basic Auth credential record to use the RaaS-report based actions. The Workday Financials spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **Basic Auth Credentials**.

4.  On the form, fill these values.

    | | |
    |---|---|
    |Name|Name to identify the credential record. For example, `Workday Financials Cred`.|
    |User name|User name of the Workday user with access to the RaaS reports.|
    |Password|Password of the Workday user with access to the RaaS reports.|

5.  Right-click the form header and select **Save**.


## Configure a connection record

Create and configure a Workday Financials spoke connection to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record, for example, **WorkdayFinancials**.

3.  From the **Connections** tab, select **New**.

4.  On the form, fill these values.

<table id="table_v2z_zzw_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the connection record. For example, `Workday Financials Conn`.

</td></tr><tr><td>

Credential

</td><td>

Required credential record of the Basic Auth type. Select the credential record you had created for the Workday Financials spoke. For example, `Workday Financials Cred`.For more information, see [Create a credential record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-workday-fin-spoke.md).

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to your Workday instance.

</td></tr></tbody>
</table>5.  For **tenant\_name** in the **Attributes** tab, enter the value of your Workday tenant name.

6.  Right-click the form header and select **Save**.


## Configure the To Do report

Create and configure the To Do report to retrieve worker's finance related inbox items suc as, to-dos, action items, approval, and so on.

### Before you begin

Role required: User with access to create report and the Business process event steps report data source.

Create all the required calculated fields.

1.  Calculated field 1:
    1.  Create increment and decrement type calculated field named **CF\_Last\_functionally\_updated\_-1**.

        \[Omitted image "wd-fin-to-do-1.PNG"\] Alt text: Calculated field named CF\_Last\_functionally\_updated\_-1.

    2.  Create Lookup Value As Of Date type calculated field named **cf\_assigned\_to\_worker\_previous** and use **CF\_Last\_functionally\_updated\_-1** in this field.

        \[Omitted image "wd-fin-to-do-2.PNG"\] Alt text: Calculated field named cf\_assigned\_to\_worker\_previous.

2.  Calculated field 2:
    1.  Create text constant type calculated field named **Cf\_text\_0**.

        \[Omitted image "wd-fin-to-do-3.PNG"\] Alt text: Calculated field named Cf\_text\_0.

    2.  Create text constant type calculated field named **CF\_Text\_as\_1**.

        \[Omitted image "wd-fin-to-do-4.PNG"\] Alt text: Calculated field named CF\_Text\_as\_1.

    3.  Create true/false condition type calculated field named **cf\_competed\_by\_is\_not\_equal\_old\_assignee**.

        \[Omitted image "wd-fin-to-do-5.PNG"\] Alt text: Calculated field named cf\_competed\_by\_is\_not\_equal\_old\_assignee.

    4.  Create evaluate expression calculated field named **CF\_EE\_Completed\_by\_admin\_exist\_as\_old\_Assignee\_or\_not**.

        \[Omitted image "wd-fin-to-do-6.PNG"\] Alt text: Calculated field named CF\_EE\_Completed\_by\_admin\_exist\_as\_old\_Assignee\_or\_not.

3.  Calculated field 3:
    1.  Create text constant type calculated field named **CF\_Text**.

        \[Omitted image "wd-fin-to-do-7.PNG"\] Alt text: Calculated field named CF\_Text.

    2.  Create Lookup related value type calculated field named **CF\_Action\_Event**.

        \[Omitted image "wd-fin-to-do-8.PNG"\] Alt text: Calculated field named CF\_Action\_Event.

    3.  Create Concatenate text type calculated field named **CF\_inbox\_SUbject**.

        \[Omitted image "wd-fin-to-do-9.PNG"\] Alt text: Calculated field named CF\_inbox\_SUbject.

4.  Calculated field 4:
    1.  Create text constant type calculated field named **CF\_url**.

        \[Omitted image "wd-fin-to-do-10.PNG"\] Alt text: Calculated field named CF\_url.

    2.  Create Lookup related value type calculated field named **CF\_business\_pro\_transaction**.

        \[Omitted image "wd-fin-to-do-11.PNG"\] Alt text: Calculated field named CF\_business\_pro\_transaction. \[Omitted image ""\] Alt text:

    3.  Create Lookup related value type calculated field named **CF\_BP\_Wid**.

        \[Omitted image "wd-fin-to-do-12.PNG"\] Alt text: Calculated field named CF\_BP\_Wid.

    4.  Create Concatenate text type calculated field named **CF\_Inbox\_url**.

        \[Omitted image "wd-fin-to-do-13.PNG"\] Alt text: Calculated field named CF\_Inbox\_url.

5.  Calculated field 5:
    1.  Create Lookup related value type calculated field named **cf\_step\_id**.

        \[Omitted image "wd-fin-to-do-14.PNG"\] Alt text: Calculated field named cf\_step\_id.

    2.  Create Lookup related value type calculated field named **CF\_subject\_id**.

        \[Omitted image "wd-fin-to-do-15.PNG"\] Alt text: Calculated field named CF\_subject\_id.

    3.  Create Lookup related value type calculated field named **CF\_subject\_and\_step\_id**.

        \[Omitted image "wd-fin-to-do-16.PNG"\] Alt text: Calculated field named CF\_subject\_and\_step\_id.

6.  Calculated field 6: Create Lookup related value type calculated field named **CF\_sent\_back**.

    \[Omitted image "wd-fin-to-do-17.png"\] Alt text: Calculated field named CF\_sent\_back.

7.  Calculated field 7:
    1.  Create Lookup related value type calculated field named **CF\_Business Process Definition on Action Event**.

        \[Omitted image "wd-fin-to-do-18.PNG"\] Alt text: Calculated field named CF\_Business Process Definition on Action Event.

    2.  Create Lookup related value type calculated field named **Cf\_parent\_business\_process\_definition** and use **CF\_Business Process Definition on Action Event** in it.

        \[Omitted image "wd-fin-to-do-19.PNG"\] Alt text: Calculated field named Cf\_parent\_business\_process\_definition.

8.  Calculated field 8:
    1.  Create increment and decrement type calculated field named **CF\_Last\_updated\_on-1**.

        \[Omitted image "wd-fin-to-do-20.PNG"\] Alt text: Calculated field named CF\_Last\_updated\_on-1.

    2.  Create Lookup Value as of date type calculated field named **cf\_status\_as\_of\_moment** and use **CF\_Last\_updated\_on-1** in this field.

        \[Omitted image "wd-fin-to-do-21.PNG"\] Alt text: Calculated field named cf\_status\_as\_of\_moment. \[Omitted image ""\] Alt text:

9.  Calculated field 9: Create Lookup Value as of date type calculated field named **CF\_Action\_Event**.

    \[Omitted image "wd-fin-to-do-22.PNG"\] Alt text: Calculated field named CF\_Action\_Event.

10. Calculated field 10: Create Lookup Value as of date type calculated field named **CF\_worker** and use **CF\_Action\_Event** as lookup field.

    \[Omitted image "wd-fin-to-do-23.PNG"\] Alt text: Calculated field named CF\_worker.

11. Calculated field 11: Create True/False condition type calculated field named **CF\_Awaiting\_person\_is\_ISU**.

    \[Omitted image "wd-fin-to-do-24.PNG"\] Alt text: Calculated field named CF\_Awaiting\_person\_is\_ISU.


### About this task

-   For identification purpose, all calculated field names starts with `CF`.
-   Create all calculated fields required for this report before developing the report to ensure that they are available while creating the report.
-   While creating the report, you can select a different report name. However, ensure that the report field names or column heading override for the respective field \(if given in the report document\) should be same as it is in report document.

    **Important:** Report field label must be same as in report document. Else, the action fails.

-   **Group Column Heading** for each business object in the **Group Column Heading** section should be blank.
-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be shared or owned by ISU user which will be used for accessing these action on the ServiceNow platform.
-   In the **Advanced** section, select the **Enable as webservice** option.

### Procedure

1.  Access the **Create Custom Report** task.

2.  Provide the report name.

    For example, **SNIH\_Inbox\_Items- finance items**.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select Data Source as **Business Process Event steps**.

6.  Ensure that the temporary report option is cleared and click **Ok**.

    \[Omitted image "wd-fin-to-do-25.PNG"\] Alt text: Create the report.

7.  Select the report business object and report fields.

    \[Omitted image "wd-fin-to-do-26.PNG"\] Alt text: Select the required fields.

    \[Omitted image "wd-fin-to-do-27.PNG"\] Alt text: Select the required fields.

8.  In Group column heading section, select all business objects.

    Group Column heading for each business object should be blank.

    \[Omitted image "wd-fin-to-do-28.PNG"\] Alt text: Select the business objects.

9.  In the **Filter** section, select the value as shown and ensure that you add parenthesis.

    \[Omitted image "wd-fin-to-do-29.PNG"\] Alt text: In the Filter section, select the required values.

    \[Omitted image "wd-fin-to-do-30.PNG"\] Alt text: In the Filter section, select the required values.

    \[Omitted image "wd-fin-to-do-31.PNG"\] Alt text: In the Filter section, select the required values.

    \[Omitted image "wd-fin-to-do-32.PNG"\] Alt text: In the Filter section, select the required values.

10. In prompt section, clear the **Populate Undefined Prompt Defaults** check box.

    \[Omitted image "wd-fin-to-do-33.PNG"\] Alt text: Clear the Populate Undefined Prompt Defaults check box.

11. Select the value of prompts in the **Prompt Defaults** section.

    Ensure that the **Label For Prompt XML Alias** of all prompt fields must be same as shown.

    \[Omitted image "wd-fin-to-do-34.PNG"\] Alt text: Select the value of prompts in the Prompt Defaults section. \[Omitted image "wd-fin-to-do-35.PNG"\] Alt text: Select the value of prompts in the Prompt Defaults section. \[Omitted image "wd-fin-to-do-36.PNG"\] Alt text: Select the value of prompts in the Prompt Defaults section. \[Omitted image "wd-fin-to-do-37.PNG"\] Alt text: Select the value of prompts in the Prompt Defaults section. \[Omitted image "wd-fin-to-do-38.PNG"\] Alt text: Select the value of prompts in the Prompt Defaults section.

    **Note:** In Business Process Types, few finance business process type in default value column are included here. You can add more finance business process types as per your requirement.

12. In the Advanced section, select **Enable as webservice** option and click **OK**.

13. After report configuration is done, click the three dots icon and navigate **Web Service** &gt; **View URLs**.

    \[Omitted image "wd-fin-to-do-39.png"\] Alt text: Click View URLs.

14. Select the required date time range in below parameters and click **OK**.

    \[Omitted image "wd-fin-to-do-40.PNG"\] Alt text: Select the required date time range.

15. In View URLs Web Service page, click the marked icon under **CSV** section.

    \[Omitted image "wd-fin-to-do-41.png"\] Alt text: Click the marked icon in the CSV section.

    The report is displayed in a new browser tab. You can see the RaaS URL of the report in browser tab and can obtain these details from this link.

    -   **https://wd2-impl-services1.workday.com** is the base URL of customer’s workday tenant.
    -   **Tenant\_Name** is the customer’s workday tenant.
    -   **Report\_Owner\_user\_name** is the user name of the report’s owner.
    -   **SNIH\_Inbox\_Items-\_finance\_items** is the report name.
    \[Omitted image "wd-fin-to-do-42.PNG"\] Alt text: RaaS URL of the report.


## Configure the Ledger Account report

Create and configure the Ledger Account report to retrieve the ledger account details.

### Before you begin

Role required: User with access to create report and the Ledger Account report data source.

### About this task

-   For identification purpose, all calculated field names starts with `CF`.
-   Create all calculated fields required for this report before developing the report to ensure that they are available while creating the report.
-   While creating the report, you can select a different report name. However, ensure that the report field names or column heading override for the respective field \(if given in the report document\) should be same as it is in report document.

    **Important:** Report field label must be same as in report document. Else, the action fails.

-   **Group Column Heading** for each business object in the **Group Column Heading** section should be blank.
-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be shared or owned by ISU user which will be used for accessing these action on the ServiceNow platform.
-   In the **Advanced** section, select the **Enable as webservice** option.

### Procedure

1.  Access the **Create Custom Report** task.

2.  Provide the report name.

    For example **RPT\_ledger\_account**.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** check box.

5.  Select **Data Source** as **Ledger Accounts**.

6.  Clear the **Temporary Report** check box and click **OK**.

    \[Omitted image "wd-fin-led-acct-1.PNG"\] Alt text: Create the RPT\_ledger\_account report.

7.  Select the report business object and report fields.

    \[Omitted image "wd-fin-led-acct-2.PNG"\] Alt text: Select the report fields.

8.  In **Filter** section, select the value as shown and ensure that you add parenthesis.

    \[Omitted image "wd-fin-led-acct-3.PNG"\] Alt text: Select the required values in the Filter section.

9.  In prompt section, clear the **Populate Undefined Prompt Defaults** check box.

    \[Omitted image "wd-fin-led-acct-4.PNG"\] Alt text: Clear the Populate Undefined Prompt Defaults check box.

10. Select the value of prompts in the Prompt default section.

    Ensure that the **Label For Prompt XML Alias** of all prompt fields must be same as shown.

    \[Omitted image "wd-fin-led-acct-5.PNG"\] Alt text: Verify the Label For Prompt XML Alias values.

11. In the Advanced section, select **Enable as webservice** option and click **OK**.

12. After report configuration is done, click the three dots icon and navigate **Web Service** &gt; **View URLs**.

    \[Omitted image "wd-fin-led-acct-6.png"\] Alt text: Click View URLs.

13. Select the required date time range in below parameters and click **OK**.

    \[Omitted image "wd-fin-led-acct-7.PNG"\] Alt text: Select the required date time range.

14. In View URLs Web Service page, click the marked icon under the **CSV** section.

    \[Omitted image "wd-fin-led-acct-8.png"\] Alt text: Click the marked icon under the CSV section.

    The report is displayed in a new browser tab. You can see the RaaS URL of the report in browser tab and can obtain these details from this link.

    -   **https://wd2-impl-services1.workday.com** is the base URL of customer’s workday tenant.
    -   **Tenant\_Name** is the customer’s workday tenant.
    -   **Report\_Owner\_user\_name** is the user name of the report’s owner.
    -   **RPT\_ledger\_account** is the report name.
    \[Omitted image "wd-fin-led-acct-9.PNG"\] Alt text: RaaS URL of the report.


## Configure the Payment Status report

Create and configure the Payment Status report to retrieve the supplier payment information within the specified date range.

### Before you begin

Role required: User with access to create report and the Supplier Payments report data source.

### About this task

-   For identification purpose, all calculated field names starts with `CF`.
-   Create all calculated fields required for this report before developing the report to ensure that they are available while creating the report.
-   While creating the report, you can select a different report name. However, ensure that the report field names or column heading override for the respective field \(if given in the report document\) should be same as it is in report document.

    **Important:** Report field label must be same as in report document. Else, the action fails.

-   **Group Column Heading** for each business object in the **Group Column Heading** section should be blank.
-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be shared or owned by ISU user which will be used for accessing these action on the ServiceNow platform.
-   In the **Advanced** section, select the **Enable as webservice** option.

### Procedure

1.  Access the **Create Custom Report** task.

2.  Provide the report name.

    For example **CR Payment status report**.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** check box.

5.  Select **Data Source** as **Supplier Payments**.

6.  Clear the **Temporary Report** check box and click **OK**.

    \[Omitted image "wd-fin-pat-st-1.PNG"\] Alt text: Create the CR Payment status report report.

7.  Select the report business object and report fields.

    \[Omitted image "wd-fin-pat-st-2.PNG"\] Alt text: Select the required fields.

    \[Omitted image "wd-fin-pat-st-3.PNG"\] Alt text: Select the required fields.

8.  In Group column heading section, select all business objects.

    Group Column heading for each business object should be blank.

    \[Omitted image "wd-fin-pat-st-4.PNG"\] Alt text: \[Omitted image ""\] Alt text:

9.  In **Filter** section, select the value as shown and ensure that you add parenthesis.

    \[Omitted image "wd-fin-pat-st-5.PNG"\] Alt text: Select the required values in the Filter section.

10. In prompt section, clear the **Populate Undefined Prompt Defaults** check box.

    \[Omitted image "wd-fin-pat-st-6.PNG"\] Alt text: Clear the Populate Undefined Prompt Defaults check box.

11. Select the value of prompts in the Prompt default section.

    Ensure that the **Label For Prompt XML Alias** of all prompt fields must be same as shown.

    \[Omitted image "wd-fin-pat-st-7.PNG"\] Alt text: Value of prompts in the Prompt default section.

12. In the Advanced section, select **Enable as webservice** option and click **OK**.

13. After report configuration is done, click the three dots icon and navigate **Web Service** &gt; **View URLs**.

    \[Omitted image "wd-fin-pat-st-8.png"\] Alt text: ClickView URLs.

14. Select the required date time range in below parameters and click **OK**.

    \[Omitted image "wd-fin-pat-st-9.PNG"\] Alt text: Select the required date time range. \[Omitted image ""\] Alt text:

15. In View URLs Web Service page, click the marked icon under **CSV** section.

    \[Omitted image "wd-fin-pat-st-10.png"\] Alt text: Click the marked icon under CSV section. \[Omitted image ""\] Alt text:

    The report is displayed in a new browser tab. You can see the RaaS URL of the report in browser tab and can obtain these details from this link.

    -   **https://wd2-impl-services1.workday.com** is the base URL of customer’s workday tenant.
    -   **Tenant\_Name** is the customer’s workday tenant.
    -   **Report\_Owner\_user\_name** is the user name of the report’s owner.
    -   **CR\_Payment\_status\_report** is the report name.
    \[Omitted image "wd-fin-pat-st-11.PNG"\] Alt text: RaaS URL of the report.


