---
title: Set up webhooks for your Workday HR spoke
description: Retrieve details the required employees in the Workday HR application to your ServiceNow instance by setting up the webhooks.Configure API client in Workday to authenticate webhook requests.Use the CreateUser Webhook to get the details of the newly onboarded employee from Workday to your ServiceNow instance.Generate user name and password in your ServiceNow instance to authenticate requests for Create User webhook and retrieve the required data from the Workday application.Retrieve the resource path from your ServiceNow instance for later use to authenticate Create User webhook requests and retrieve the required data from the Workday applicationImport CLAR file available at ServiceNow Store to set up Create User webhook and authenticate requests from ServiceNow instance.Use the Offboarding Webhook to get the details of the offboarded employee from Workday to your ServiceNow instance.Generate user name and password in your ServiceNow instance to authenticate requests for Offboarding webhook and retrieve the required data from the Workday application.Retrieve the resource path from your ServiceNow instance for later use to authenticate Offboard webhook requests and retrieve the required data from the Workday applicationImport CLAR file available at ServiceNow Store to set up Offboarding webhook and authenticate requests from ServiceNow instance.Use the LeaveofAbsence Webhook to get leave of absence details of an employee from Workday to your ServiceNow instance.Generate user name and password in your ServiceNow instance to authenticate requests for LeaveofAbsence webhook and retrieve the required data from the Workday application.Retrieve the resource path from your ServiceNow instance for later use to authenticate Offboard webhook requests and retrieve the required data from the Workday applicationImport CLAR file available at ServiceNow Store to set up LeaveofAbsence webhook and authenticate requests from ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-webhook-wd-hr-spoke.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up webhooks for your Workday HR spoke

Retrieve details the required employees in the Workday HR application to your ServiceNow instance by setting up the webhooks.

## Before you begin

Role required: admin

## Configure ServiceNow Webhook API Client for OAuth 2.0 in Workday

Configure API client in Workday to authenticate webhook requests.

### Before you begin

Role required: Workday admin role or the role with granted permission to setup OAuth 2.0 client in Workday.

### About this task

You only need to configure this step if you want to use the ServiceNow platform as a listener endpoint, and receive event notifications from Workday. If you don't need to receive any event notifications from Workday, then you can skip the configurations mentioned in this section.

**Note:** These configurations must be performed in Workday.

### Procedure

1.  In Workday, access the Edit Tenant Setup - Security task.

2.  Select the **OAuth 2.0 Clients Enabled** option from the **OAuth 2.0 Settings** section.

3.  Access the Register API Client task.

4.  Enter the **Client Name**.

5.  Select the **Client Grant Type** as Authorization Code Grant.

6.  Select **Access Token Type** as Bearer.

7.  Enter a valid Redirection URI.

    **Note:** Make sure that the OAuth 2.0 Redirection URI is a valid HTTPS URL.

8.  Select the Refresh Token Timeout in days.

9.  Select the Non-Expiring Refresh Tokens option to prevent the refresh token from timing out.

10. Select the **Grant Administrative Consent** option to grant OAuth permission to a REST API Client tenant-wide.

    When you select this option, you don't have to grant client access explicitly to Workday functional areas.

11. From the Functional Areas prompt, select the functional areas to which your OAuth 2.0 client requires access.

12. If the OAuth 2.0 client requires access to core Workday domains that aren’t in any functional areas, select the **Include Workday Owned Scope** option.


## Set up CreateUser Webhook for the Workday HR spoke

Use the CreateUser Webhook to get the details of the newly onboarded employee from Workday to your ServiceNow instance.

### Generate user name and password in your ServiceNow instance for Create User webhook

Generate user name and password in your ServiceNow instance to authenticate requests for Create User webhook and retrieve the required data from the Workday application.

#### Before you begin

Role required: ServiceNow admin

**Note:** These configurations must be performed in your ServiceNow instance.

#### Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Navigate to **All** &gt; **System Definition** &gt; **Table**.

3.  Filter and search for the Workday HR spoke webhook registry table.

    For example, **Workday Webhook Registry**.

4.  Click the **Show List** related list.

5.  Click **New**.

6.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Description|Description of the webhook registry record. Enter `Workday event and authentication for Create User`.|
    |UserName|Workday user who has integration rights using Workday Web Services.|
    |Password|Password of the Workday user.|
    |Workday Event|Event for which the webhook is set up. Enter `CreateUser`.|
    |Workday Instance|Workday host URL and tenant name. Enter the URL in this format:`https://<workday_host_url>/<workday_tenant_name>`|

7.  Right-click the form header and click **Save**.

8.  Click **Generate UserName And Password**.

    Copy and record the values of username and password. These values must be specified in the Workday instance to authenticate the webhook requests.

    **Note:** If you have more than one HIRE BP in your environment, you must configure all the HIRE BPs to enable the Create User webhook for all HIRE employee transactions.


### Retrieve the resource path from your ServiceNow instance for Create User webhook

Retrieve the resource path from your ServiceNow instance for later use to authenticate Create User webhook requests and retrieve the required data from the Workday application

#### Before you begin

Role required: ServiceNow admin.

**Note:** These configurations must be performed in your ServiceNow instance.

#### Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

3.  Open the record for the Workday HR spoke.

4.  In the **Resources** tab, click the **Callback** record.

5.  Record and save the value of **Resource path** for later use.


### Import CLAR file to your Workday instance for Create User webhook

Import CLAR file available at ServiceNow Store to set up Create User webhook and authenticate requests from ServiceNow instance.

#### Before you begin

-   Workday Studio should be installed.
-   Access to custom report creation policy.

    Create custom report in workday based on the New\_Hire\_record report structure and share the report with ISU user.

-   Access to edit business process definition.
-   Access to create and edit integration system.
-   Role required: admin

**Note:**

-   Except integration name, report field XPath \(if required\), and Workday instance header, users are cautioned against modifying the values of fields or properties in the CLAR file.
-   These configurations must be performed in Workday Studio.

#### Procedure

1.  From the [Workday HR spoke](https://store.servicenow.com/sn_appstore_store.do#!/store/application/133e9dacdb910010ea4494d9db961988) page on [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), download the `Workday-HR-Webhook-Studio-Sample` file from **Supporting Links and Docs**.

2.  Unzip the sample file to obtain the CLAR file.

3.  Import the CLAR file to Workday Studio.

4.  In the **Properties** tab of the **StartHere** component, navigate to **Services** and select the RAAS report created for this webhook.

    \[Omitted image "configure-clar-file.png"\] Alt text: Configure the StartHere component

5.  Choose the environment where your report exists such as, implementation or sandbox and configure the report as per your requirement.

6.  Provide a report name and select the required report.

    \[Omitted image "report-name-wd-hr.png"\] Alt text: Report name

7.  Provide the alias name of the report.

    \[Omitted image "alias-wd-hr.png"\] Alt text: Alias name

8.  After the report alias is added, add the selected path of report in **Extra Path** that is used to run the report based on prompt.

    \[Omitted image "extra-path-wd-hr.png"\] Alt text: Extra Path

9.  In the **Set Headers** component, provide your Workday instance for the **WorkdayInstance** header.

    \[Omitted image "conf-set-headers-wd.png"\] Alt text: Configure the Set Headers component

10. In the properties of **HttpOut**, fill in these values.

<table id="table_nmg_zdl_qmb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Endpoint

</td><td>

REST endpoint**Note:** See [Retrieve the resource path from your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-webhk-wd.md) for more information.

</td></tr><tr><td>

Http Method

</td><td>

POST

</td></tr></tbody>
</table>    \[Omitted image "httpout-properties-wd.png"\] Alt text: Configure the HttpOut properties

11. Save the changes.

12. In the project explorer, select the integration and deploy it in your Workday system.

13. Log in to your Workday instance and navigate to **Integration** &gt; **Integration System** &gt; **Configure Integration Attributes**.

    \[Omitted image "conf-int-attributes-wd.png"\] Alt text: Configure Integration Attributes

14. Provide user name and password in **Configure Integration Attributes** that you have generated in [Generate user name and password in your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-webhk-wd.md).

    \[Omitted image "username-pwd-wd-hr.png"\] Alt text: Configure integration attributes

15. Modify a business process and add this integration in your business process.

    1.  Edit definition of the business process.

        \[Omitted image "edit-def-wd-hr.png"\] Alt text: Edit definition

    2.  Select the effective date and click **Ok**.

    3.  Click the + sign and add a new business process step in BP.

    4.  Select an order, which is after the completion step of business process.

    5.  Add the business process and select **Type** as **Integration**.

        \[Omitted image "integration-type.png"\] Alt text: Select Integration type

    6.  Provide ISU username in **Run as User** and click **Ok**.

    7.  Click **Configure Integration** on the newly added business process step in Hire BP.

        \[Omitted image "conf-int-button.png"\] Alt text: Configure integration

    8.  In integration criteria, select value type as **Determine value at runtime** and select value as **Employee ID**.

        \[Omitted image "determine-value-runtime.png"\] Alt text: Determine value at runtime

        Selected **Employee ID** field in value is displayed.

        \[Omitted image "emp-id-field.png"\] Alt text: Employee ID field

    9.  Click **Ok**.

    10. Create a report for the webhook with these details:

        Report definition:

        \[Omitted image "report-def-wd-hr.png"\] Alt text: Report definition

        Column labels:

        \[Omitted image "col-labels-wd-hr.png"\] Alt text: Column labels

        Calculated field details:

        \[Omitted image "calc-fields-wd-hr.png"\] Alt text: Calculated field details

        Filter and prompt details:

        \[Omitted image "filter-prompt-wd-hr.png"\] Alt text: Filter and prompt details


## Set up Offboarding Webhook for the Workday HR spoke

Use the Offboarding Webhook to get the details of the offboarded employee from Workday to your ServiceNow instance.

### Generate user name and password in your ServiceNow instance for Offboarding webhook

Generate user name and password in your ServiceNow instance to authenticate requests for Offboarding webhook and retrieve the required data from the Workday application.

#### Before you begin

Role required: admin

**Note:** These configurations must be performed in your ServiceNow instance.

#### Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Navigate to **All** &gt; **System Definition** &gt; **Table**.

3.  Filter and search for the Workday HR spoke webhook registry table.

    For example, **Workday Webhook Registry**.

4.  Click the **Show List** related list.

5.  Click **New**.

6.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Description|Description of the webhook registry record. Enter `Workday event and authentication for Offboarding`.|
    |UserName|Workday user who has integration rights using Workday Web Services.|
    |Password|Password of the Workday user.|
    |Workday Event|Event for which the webhook is set up.|
    |Workday Instance|Workday host URL and tenant name. Enter the URL in this format:`https://<workday_host_url>/<workday_tenant_name>`|

7.  Right-click the form header and click **Save**.

8.  Click **Generate UserName And Password**.

    Copy and record the values of username and password. These values must be specified in the Workday instance to authenticate the webhook requests.

    **Note:** If you have more than one HIRE BP in your environment, you must configure all the HIRE BPs to enable the Create User webhook for all HIRE employee transactions.


### Retrieve the resource path from your ServiceNow instance for Offboarding webhook

Retrieve the resource path from your ServiceNow instance for later use to authenticate Offboard webhook requests and retrieve the required data from the Workday application

#### Before you begin

Role required: admin.

**Note:** These configurations must be performed in your ServiceNow instance.

#### Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

3.  Open the record for the Workday HR spoke.

4.  In the **Resources** tab, click the **Callback** record.

5.  Record and save the value of **Resource path** for later use.


### Import CLAR file to your Workday instance for Offboarding webhook

Import CLAR file available at ServiceNow Store to set up Offboarding webhook and authenticate requests from ServiceNow instance.

#### Before you begin

-   Workday Studio should be installed.
-   Access to custom report creation policy.

    Create custom report in workday based on the New\_terminated\_record report structure and share the report with ISU user.

-   Access to edit business process definition.
-   Access to create and edit integration system.
-   Role required: admin

**Note:**

-   Except integration name, report field XPath \(if required\), and Workday instance header, users are cautioned against modifying the values of fields or properties in the CLAR file.
-   These configurations must be performed in Workday Studio.

#### Procedure

1.  From the [Workday HR spoke](https://store.servicenow.com/sn_appstore_store.do#!/store/application/133e9dacdb910010ea4494d9db961988) page on [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), download the `Workday-HR-Offboarding-Webhook-Studio-Sample` file from **Supporting Links and Docs**.

2.  Unzip the sample file to obtain the CLAR file.

3.  Import the CLAR file to Workday Studio.

4.  In the **Properties** tab of the **StartHere** component, navigate to **Services** and select the RAAS report created for this webhook.

    \[Omitted image "raas-report-offboarding.jpg"\] Alt text: RAAS report for offboarding spoke

5.  Choose the environment where your report exists such as, implementation or sandbox and configure the report as per your requirement.

6.  Provide a report name and select the required report.

    \[Omitted image "custom-raas-report-offboarding.jpg"\] Alt text: Custom RaaS report for Offboarding webhook

7.  Provide the alias name of the report.

    \[Omitted image "alias-report-offboarding-webhook.jpg"\] Alt text: Alias report for offboarding webhook

8.  After the report alias is added, add the selected path of report in **Extra Path** that is used to run the report based on prompt.

    \[Omitted image "extra-path-offboarding-webhk.jpg"\] Alt text: extra path for offboarding webhook

9.  Select the report alias.

10. In the **Set Headers** component, provide your Workday instance for the **WorkdayInstance** header.

    \[Omitted image "workday-instance-set-headers-offboarding.jpg"\] Alt text: Set headers component offboarding webhook

11. In the properties of **HttpOut**, fill in these values.

<table id="table_ryn_5mm_wqb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Endpoint

</td><td>

REST endpoint**Note:** See [Retrieve the resource path from your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-webhk-wd.md) for more information.

</td></tr><tr><td>

Http Method

</td><td>

POST

</td></tr></tbody>
</table>    \[Omitted image "httpout-properties-offboarding.jpg"\] Alt text: httpout properities for offboarding

12. Save the changes.

13. In the project explorer, select the integration and deploy it in your Workday system.

14. Log in to your Workday instance and navigate to **Integration** &gt; **Integration System** &gt; **Configure Integration Attributes**.

    \[Omitted image "config-intgrt-attributes-offboarding.jpg"\] Alt text: configure integration attributes offboarding

15. Provide user name and password in **Configure Integration Attributes** that you have generated in [Generate user name and password in your ServiceNow instance for Offboarding webhook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-webhook-wd-hr-spoke.md).

    \[Omitted image "usernm-pwd-attri-offboarding.jpg"\] Alt text: integration attributes configuration offboarding webhook

16. Modify a business process and add this integration in your business process.

    1.  Edit the definition of the business process.

        \[Omitted image "related-action-integration-offboarding.jpg"\] Alt text:

    2.  Select the ISU user in Workday Account box.

    3.  Select the effective date and click **Ok**.

    4.  Click the + sign and add a new business process step in BP.

    5.  Select an order, which is after the completion step of business process.

    6.  Add the business process and select **Type** as **Integration**.

        \[Omitted image "type-integration-offboarding.jpg"\] Alt text:

    7.  Provide ISU username in **Run as User** and click **Ok**.

    8.  Click **Configure Integration** on the newly added business process step in Hire BP.

        \[Omitted image "config-integrt-hire-bp-offboarding.jpg"\] Alt text: configure integration offboarding webhook

    9.  In integration criteria, select value type as **Determine value at runtime** and select value as **Employee ID**.

        \[Omitted image "integrt-criteria-det-value-runtime-offboarding.jpg"\] Alt text: integration criteria value at runtime

        The selected **Employee ID** field in value is displayed.

        \[Omitted image "integ-crit-emp-field-offboarding.jpg"\] Alt text: integration criteria employee ID for offboarding webhook

    10. Click **Ok**.

    11. Open **Create Custom Report** task.

    12. Enter the report name, for example, enter `New_terminated_record`.

    13. Select **Report Type** as Advanced.

    14. Uncheck the Optimized for performance option.

    15. Select Data Source as All Workers.

        \[Omitted image "data-source-all-workers-offboarding.jpg"\] Alt text: View Custom Report for offboarding

    16. Create a report as shown below:

        \[Omitted image "sample-report-offboarding.jpg"\] Alt text: Sample report for offboarding webhook

        Group Column Headings in reports\[Omitted image "group-column-headings-offboarding.jpg"\] Alt text: Group column headings in report

        Sort section in reports \[Omitted image "sort-section-offboarding.jpg"\] Alt text:

        Filter section in reports\[Omitted image "filter-section-report-offboarding.jpg"\] Alt text: filter section in reports

    17. Select **Populate Undefined Prompt defaults** option from the **Prompts** tab.

    18. Select **Enable as web service** option from the **Advanced** tab.


## Set up LeaveofAbsence Webhook for the Workday HR spoke

Use the LeaveofAbsence Webhook to get leave of absence details of an employee from Workday to your ServiceNow instance.

### Generate user name and password in your ServiceNow instance for LeaveofAbsence webhook

Generate user name and password in your ServiceNow instance to authenticate requests for LeaveofAbsence webhook and retrieve the required data from the Workday application.

#### Before you begin

Role required: admin

**Note:** These configurations must be performed in your ServiceNow instance.

#### Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Navigate to **All** &gt; **System Definition** &gt; **Table**.

3.  Filter and search for the Workday HR spoke webhook registry table, for example, **Workday Webhook Registry**.

4.  Click the **Show List** related list.

5.  Click **New**.

6.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Description|Description of the webhook registry record. Enter `Workday event and authentication for leave of absence`.|
    |UserName|Workday user who has integration rights using Workday Web Services.|
    |Password|Password of the Workday user.|
    |Workday Event|Event for which the webhook is set up. Enter `LeaveofAbsence`.|
    |Workday Instance|Workday host URL and tenant name. Enter the URL in this format:`https://<workday_host_url>/<workday_tenant_name>`|

7.  Right-click the form header and click **Save**.

8.  Click **Generate UserName And Password**.

    Copy and record the values of username and password. These values must be specified in the Workday instance to authenticate the webhook requests.

    **Note:** If you have more than one HIRE BP in your environment, you must configure all the HIRE BPs to enable the Create User webhook for all HIRE employee transactions.


### Retrieve the resource path from your ServiceNow instance for LeaveofAbsence webhook

Retrieve the resource path from your ServiceNow instance for later use to authenticate Offboard webhook requests and retrieve the required data from the Workday application

#### Before you begin

Role required: admin.

**Note:** These configurations must be performed in your ServiceNow instance.

#### Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

3.  Open the record for the Workday HR spoke.

4.  In the **Resources** tab, click the **Callback** record.

5.  Record and save the value of **Resource path** for later use.


### Import CLAR file to your Workday instance for LeaveofAbsence webhook

Import CLAR file available at ServiceNow Store to set up LeaveofAbsence webhook and authenticate requests from ServiceNow instance.

#### Before you begin

-   Workday Studio should be installed.
-   Access to custom report creation policy.

    Create custom report in workday based on the Leave\_of\_absence\_request report structure and share the report with ISU user.

-   Access to edit business process definition.
-   Access to create and edit integration system.
-   Role required: admin

**Note:**

-   Except integration name, report field XPath \(if required\), and Workday instance header, users are cautioned against modifying the values of fields or properties in the CLAR file.
-   These configurations must be performed in Workday Studio.

#### Procedure

1.  From the [Workday HR spoke](https://store.servicenow.com/sn_appstore_store.do#!/store/application/133e9dacdb910010ea4494d9db961988) page on [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), download the `Workday-HR-Leave-of-Absence-Webhook-Studio-Sample` file from **Supporting Links and Docs**.

2.  Unzip the sample file to obtain the CLAR file.

3.  Import the CLAR file to Workday Studio.

4.  In the **Properties** tab of the **StartHere** component, navigate to **Services** and select the RAAS report created for this webhook.

    \[Omitted image "raas-report-leave-absence.jpg"\] Alt text: RaaS report for leave of absence webhook

5.  Choose the environment where your report exists such as, implementation or sandbox and configure the report as per your requirement.

6.  Provide a report name and select the required report.

    \[Omitted image "custom-raas-report-leave-absence.jpg"\] Alt text: Custom Raas Report for leave of absence webhook

7.  Provide the alias name of the report.

    \[Omitted image "alias-report-leave-absence.jpg"\] Alt text: Alias for report name

8.  After the report alias is added, add the selected path of report in **Extra Path** that is used to run the report based on prompt.

    \[Omitted image "extra-path-leave-absence.jpg"\] Alt text: Extra path for report alias

9.  Select the report alias.

10. In the **Set Headers** component, provide your Workday instance for the **WorkdayInstance** header.

    \[Omitted image "set-headers-leave-of-absence.jpg"\] Alt text: Set headers for Workday instance

11. In the properties of **HttpOut**, fill in these values.

<table id="table_pp4_ykn_wqb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Endpoint

</td><td>

REST endpoint**Note:** See [Retrieve the resource path from your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-webhk-wd.md) for more information.

</td></tr><tr><td>

Http Method

</td><td>

POST

</td></tr></tbody>
</table>    \[Omitted image "httpout-leave-absence.jpg"\] Alt text: http out properties for leave of absence webhook

12. Save the changes.

13. In the project explorer, select the integration and deploy it in your Workday system.

14. Log in to your Workday instance and navigate to **Integration** &gt; **Integration System** &gt; **Configure Integration Attributes**.

    \[Omitted image "config-integ-attributes-leave-absence.jpg"\] Alt text: Configure integration attributes for leave of absence webhook

15. Provide user name and password in **Configure Integration Attributes** that you have generated in [Generate user name and password in your ServiceNow instance for LeaveofAbsence webhook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-webhook-wd-hr-spoke.md).

    \[Omitted image "usrname-pwd-attributes-leave-absence.jpg"\] Alt text: user name and password for integration attributes configuration

16. Modify a business process and add this integration in your business process.

    1.  Edit definition of the business process.

        \[Omitted image "business-process-def-leave-absence.jpg"\] Alt text: Business process definition

    2.  Select the ISU user in Workday Account box.

    3.  Select the effective date and click **Ok**.

    4.  Click the + sign and add a new business process step in BP.

    5.  Select an order, which is after the completion step of business process.

    6.  Add the business process and select **Type** as **Integration**.

        \[Omitted image "type-integration-leave-absence.jpg"\] Alt text: Business process type integration

    7.  Provide ISU username in **Run as User** and click **Ok**.

    8.  Click **Configure Integration** on the newly added business process step in Hire BP.

        \[Omitted image "config-integrate-hire-bp-leave-absence.jpg"\] Alt text: Configure integration for business process

    9.  In integration criteria, select value type as **Determine value at runtime** and select value as **Employee ID**.

        \[Omitted image "det-value-runtime-leave-absence.jpg"\] Alt text: Integration criteria value at runtime

        Selected **Employee ID** field in value is displayed.

        \[Omitted image "integrt-criteria-emp-id-selected-leave-absence.jpg"\] Alt text: Employee ID selected for integration criteria

    10. Click **Ok**.

    11. Open **Create Custom Report** task.

    12. Enter the report name, for example, `Leave_of_absence_request`.

    13. Select **Report Type** as Advanced.

    14. Uncheck the Optimized for performance option.

    15. Select **Data Source** as **All Active and Terminated Workers**.

    16. Create a report as shown below:

        \[Omitted image "sample-report-leave-absence.jpg"\] Alt text: Sample report

        Group Column Heading section in report\[Omitted image "group-col-heading-leave-absence.jpg"\] Alt text: Group Column Headings in report

        Filter section in report\[Omitted image "filter-section-leave-absence.jpg"\] Alt text: Filter section in report

    17. Select **Populate Undefined Prompt defaults** option from the **Prompts** tab.

    18. Select **Enable as web service** option from the **Advanced** tab.


