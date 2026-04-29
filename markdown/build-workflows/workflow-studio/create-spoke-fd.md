---
title: Create spoke and build actions by importing an OpenAPI Specification
description: Automate an integration and generate reusable actions by importing an OpenAPI Specification.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Building spokes using Spoke Generator, Workflow Studio, Build workflows]
---

# Create spoke and build actions by importing an OpenAPI Specification

Automate an integration and generate reusable actions by importing an OpenAPI Specification.

## Before you begin

-   Install the Spoke Generator app from the ServiceNow Store.
-   Confirm that ServiceNow Integration Hub Professional Pack Installer \(com.glide.hub.integrations.professional\) is installed and the license is entitled.
-   Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click **Create new** &gt; **Spoke**.

3.  On the Spoke Info screen, specify if you want to create the spoke in a new scope or an existing scope.

    1.  If you choose to create the spoke in a new scope, select an image as the logo for your integration and fill in the fields.

        Here, we will go through an integration with Zoom as an example.

        |Field|Description|
        |-----|-----------|
        |Spoke name|Name to identify the custom spoke.|
        |Description|Description about the custom spoke.|

        ![Create spoke in new scope.](../images/spk-gen-new-scope.png)

        **Note:**

        The value of **App scope name** is the format: `x_<company-code>_<spoke-name>_<spoke>`. By default, the &lt;company-code&gt; is, `snc`. You can configure the company code by configuring **Value** of the system property, **glide.appcreator.company.code**.![Configuring Value of glide.appcreator.company.code.](../images/spoke-gen-sys-property.png)

        This configured value is used when the value **App scope name** is generated.![Configured value of App scope name.](../images/spoke-gen-app-scope.png)

    2.  If you choose to create the spoke in an existing scope, select an image as the logo for your integration and fill in the fields.

        Here, we will go through an integration with AWS as an example.

<table id="table_tz2_hs3_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application name

</td><td>

An existing application name or scope.![Select an existing application.](../images/spk-gen-existing-app-name.png)

</td></tr><tr><td>

App scope name

</td><td>

Scope name that is auto-populated based in the selected **Application name**.

</td></tr><tr><td>

Description

</td><td>

Description about the custom spoke.

</td></tr></tbody>
</table>        ![Create spoke in an existin scope.](../images/spk-gen-existing-scope.png)

4.  Click **Continue**.

    Based on the provided name and description, if there are any matching spokes on Store, the spoke details are displayed.![Matching spokes found on Store.](../images/spoke-gen-store-apps.png)

    1.  Click **View details on Store** to see the details of the matching spokes.

        Details of the matching spokes are displayed in a new browser tab.

    2.  Install the spoke from the Store.

        For more details, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

    3.  After installing the spoke, navigate to the Workflow Studio tab.

        The system displays the message `Have you installed a spoke from the Store?`.

    4.  Select one of these options and click **Continue**.

        |Option|Description|
        |------|-----------|
        |**Yes, view the installed spoke.**|Option to redirect to the **Spokes** dashboard under **Integrations**.|
        |**No, I will build custom spoke.**|Option to continue with spoke creation.|
        |**No, I want to exit spoke creation.**|Option to close the current tab.|

5.  Click **Skip** if you want to build the custom spoke.

    **Note:** These following steps are also applicable if you have selected the **No, I will build custom spoke.** option.

    The spoke is created and a confirmation message is displayed.

6.  On the Build Info screen, select the method using which you want to build your spoke.

    You can choose to build your spoke using OpenAPI specification or Postman collection.

7.  Select **OpenAPI Specification** and click **Continue** to import an OpenAPI specification.

    ![Select the method by which you want to create your spoke.](../images/spk-gen-open-api.png)

8.  For **OpenAPI source**, click **Import new**.

9.  On the Import new OpenAPI source screen, perform one of these two steps.

    1.  If you want to import using an URL, select **Import from URL** for **Import method** and specify the URL in **OpenAPI URL**.

        ![Import new OpenAPI source.](../images/create-spk-import-openapi-url.png)

    2.  If you want to import manually using JSON or YAML code, select **Import from JSON or YAML manually** for **Import method** and provide the code in **JSON or YAML**.

        ![Create spoke manually by importing JSON or YAML.](../images/create-spk-import-openapi-json.png)

10. Click **Import**.

    The OpenAPI source is imported.

11. For **Connection and credential alias**, click **Create new**.

12. On the Create new connection and credential alias screen, fill in the fields and provide the alias information.

<table id="table_awp_szx_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection &amp; Credential name

</td><td>

Name to identify the connection and credential alias record.

</td></tr><tr><td>

Configuration Template for authentication

</td><td>

Required authentication mechanism for this integration. Ensure that the authentication mechanism is compatible with the OpenAPI source.**Note:** The configuration template is auto-populated based on the OpenAPI specification you had provided. You can continue with the default option or change it as per your requirement.

</td></tr></tbody>
</table>    ![Create connection alias for the spoke.](../images/create-spk-conn-alias.png)

13. Click **Create alias and continue**.

14. On the same screen, fill in the fields to configure the alias.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Base URL to connect to the third-party instance or server. This URL is auto-populated based on the OpenAPI specification you had provided.|
    |Credential Information|
    |Based on the configuration template you had selected, the relevant credential fields are displayed. Provide the required values to configure the credential record.|

    ![Configure connection and credential records.](../images/create-spk-conn-alias-2.png)

    If you want configure the alias record later, click **Do it later**.

15. Click **Submit**.

    The connection alias record is created.

16. Click **Generate operations**.

    ![Generate operations for the spoke.](../images/create-spk-fin-buildinfo.png)

    All the operations that can be performed using the OpenAPI Specification are listed.

17. Select the required operations.

    You can search for the required actions by entering the required term in the search bar. The actions that match the specified search term are displayed.

    ![Search for the required actions.](../images/spoke-gen-search-act.png)

18. Click **Publish**.

    Alternatively, you can also select **Save actions as Draft** to save the actions as draft, modify them as per your requirement, and publish them later.![Create spoke actions.](../images/create-spk-actions.png)

19. Click **Done: Go to spoke** to go the Spokes page and view the publish status.

    -   Actions with the OpenAPI step are created. For information about the OpenAPI step, see [OpenAPI support in the REST step](https://www.servicenow.com/docs/access?context=open-api-integration&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
    -   Action inputs and outputs are mapped.
    -   Actions are published and listed in the spoke details page under **Actions** &gt; **Published**.
    You can start using these published actions to create flows and subflows as per your requirement.

    -   If you have saved actions as draft, you can access these draft actions in the spoke details page under **Actions** &gt; **Draft**.
    -   To view run-time information about the spoke activities, click **Spoke activity log** in the spoke details page. Every time a spoke activity is performed, the system generates its information as a spoke activity log. Click the required **Number** to view the activity log. Every operation in the spoke activity log has one of these status values:

        |Status|Description|
        |------|-----------|
        |**new**|An event for the operation is created and this operation will be executed soon.|
        |**error**|The operation has failed to execute.|
        |**processing**|The operation execution is in progress.|
        |**success**|The operation has been executed successfully.|

    You can create flows and subflows in the spoke details page and use them in your integration. For more information, see [Building flows](../concept/flows.md) and [Building subflows](../concept/subflows.md).

    Along with **Spoke activity log**, you can also view details of the available flows, subflows, and actions in the spoke details page.


