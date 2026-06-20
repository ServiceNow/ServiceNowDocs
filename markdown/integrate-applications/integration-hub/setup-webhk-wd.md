---
title: Set up webhook for your Workday Financials spoke
description: Set up a webhook to get the data from the Workday Financials application to your ServiceNow instance when an event occurs.Generate user name and password in your ServiceNow instance to authenticate requests and retrieve the required data from the Workday application.Retrieve the resource path from your ServiceNow instance for later use to authenticate requests and retrieve the required data from the Workday applicationImport CLAR file available at ServiceNow Store to set up webhooks and authenticate requests from ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/setup-webhk-wd.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Workday Financials Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up webhook for your Workday Financials spoke

Set up a webhook to get the data from the Workday Financials application to your ServiceNow instance when an event occurs.

## Before you begin

-   [Set up the Workday Financials spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-workday-fin-spoke.md)
-   Role required: admin

## Generate user name and password in your ServiceNow instance

Generate user name and password in your ServiceNow instance to authenticate requests and retrieve the required data from the Workday application.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Table**.

2.  Filter and search for the Workday Financials spoke webhook registry table, for example, **Workday Financials Webhook Registry**.

3.  Click the **Show List** related list.

4.  Click **New**.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Description|Description of the webhook registry record. Enter `Workday event and authentication for Create PO`.|
    |UserName|Workday user who has integration rights using Workday Web Services.|
    |Password|Password of the Workday user.|
    |Workday Event|Event for which the webhook is set up. Enter `CreatePO`.|
    |Workday Instance|Base URL of the Workday instance or tenant name.|

6.  Right-click the form header and click **Save**.

7.  Click **Generate UserName And Password**.

    Copy and record the values of user name and password. These values must be specified in the Workday instance to authenticate the webhook requests.


## Retrieve the resource path from your ServiceNow instance

Retrieve the resource path from your ServiceNow instance for later use to authenticate requests and retrieve the required data from the Workday application

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

2.  Open the record for the Workday Financials spoke.

3.  In the **Resources** tab, click the **Callback** record.

4.  Record and save the value of **Resource path** for later use.


## Import CLAR file to your Workday instance

Import CLAR file available at ServiceNow Store to set up webhooks and authenticate requests from ServiceNow instance.

### Before you begin

-   Workday Studio should be installed.
-   Access to custom report creation policy.
    -   Create custom report in Workday based on the Purchase\_order\_report structure and share the report with ISU user.
    -   Ensure that you select all companies in company prompt in report.

        \[Omitted image "prompt-instructions-wd-fin.png"\] Alt text: Prompt instructions

-   Access to edit business process definition.
-   Access to create and edit integration system.
-   Role required: admin

**Note:** Except integration name, report field XPath \(if required\), and Workday instance header, users are cautioned against modifying the values of fields or properties in the CLAR file.

### Procedure

1.  From the [Workday Financials spoke](https://store.servicenow.com/sn_appstore_store.do#!/store/application/dddbe37edbe5c810ea4494d9db96195f) page on [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), download the `Workday-Finance-Webhook-Studio-Sample` file from **Supporting Links and Docs**.

2.  Unzip the sample file to obtain the CLAR file.

3.  Import the CLAR file to Workday Studio.

4.  In the **Properties** tab of the **StartHere** component, navigate to **Services** and select the RAAS report created for this webhook.

    \[Omitted image "conf-starthere-wd-fin.png"\] Alt text: Configure the StartHere properties

5.  Choose the environment where your report exists such as, implementation or sandbox, and configure the report as per your requirement.

6.  Provide a report name and select the required report.

    \[Omitted image "provide-purchase-order-wd-fin.png"\] Alt text: Provide purchase order name

7.  Provide the alias name of the report.

    \[Omitted image "alias-box-wd-fin.png"\] Alt text: Alias

8.  After the report alias is added, add the selected path of report in **Extra Path** that is used to run the report based on prompt.

    \[Omitted image "extra-path-wd-fin.png"\] Alt text: Extra Path

9.  In the **Set Headers** component, provide your Workday instance for the **WorkdayInstance** header.

    \[Omitted image "set-headers-wd-fin.png"\] Alt text: Set headers

10. In the properties of **HttpOut**, fill in these values.

<table id="table_nmg_zdl_qmb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Endpoint

</td><td>

REST endpoint**Note:** See [Retrieve the resource path from your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-webhk-wd.md) for more information.

</td></tr><tr><td>

Http Method

</td><td>

POST

</td></tr></tbody>
</table>    \[Omitted image "httpout-properties-wd.png"\] Alt text: Configure the HttpOut properties

11. Save the changes.

12. In the project explorer, select the integration and deploy it in your Workday system.

13. Log in to your Workday instance and navigate to **Integration** &gt; **Integration System** &gt; **Configure Integration Attributes**.

    \[Omitted image "conf-int-attributes-wd-fin.png"\] Alt text: Configure integration attributes

14. Provide user name and password in **Configure Integration Attributes** that you have generated in [Generate user name and password in your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-webhk-wd.md).

    \[Omitted image "username-password-wd.png"\] Alt text: Configure username and password

15. Modify a business process and add this integration in your business process.

    1.  Edit definition of the business process.

    2.  Search for Purchase Order business process in Workday.

        If within one customer environment there are more than one purchase order business processes, all the business processes should be configured to enable this webhook for all purchase orders

        \[Omitted image "edit-definition-fin.png"\] Alt text: Edit definition

    3.  Select the effective date and click **Ok**.

    4.  Click the + sign and add a new business process step in BP.

    5.  Select an order, which is after the completion step of business process.

    6.  Select **Type** as **Integration**.

        \[Omitted image "integration-type-fin.png"\] Alt text: Select integration type

    7.  Provide ISU username in **Run as User** and click **Ok**.

    8.  Click **Configure Integration** on the newly added business process step in hire BP.

        \[Omitted image "conf-int-button-fin.png"\] Alt text: Configure integration button

    9.  On the Configuration Integration Step page, click **Ok**.

    10. In integration criteria, select value type as **Determine value at runtime** and select value as **PO Number**.

        \[Omitted image "determine-value-runtime-wd-fin.png"\] Alt text: Determine value at runtime

        Selected **PO Number** should be as shown below.

        \[Omitted image "emp-id-fin.png"\] Alt text: Employee ID field

    11. Click **Ok**.

    12. Create a report for the webhook with these details:

        Purchase Order report definition:

        \[Omitted image "po-report-wd-fin.png"\] Alt text: Purchase Order report definition

        Column labels:

        \[Omitted image "col-names-wd-fin.png"\] Alt text: Column labels

        Filter:

        \[Omitted image "filter-wd-fin.png"\] Alt text: Filter

        Prompt default:

        \[Omitted image "prompt-defaults-wd-fin.png"\] Alt text: Prompt defaults


