---
title: Create spoke and build actions using the spoke generation skill in Now Assist
description: Automate an integration and generate reusable actions by providing the required third-party API documentation snippet as an input.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-02-11"
reading_time_minutes: 4
breadcrumb: [Use Now Assist to create spokes and build actions, Building spokes using Spoke Generator, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create spoke and build actions using the spoke generation skill in Now Assist

Automate an integration and generate reusable actions by providing the required third-party API documentation snippet as an input.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click **Create new** &gt; **Spoke**.

3.  On the Spoke Info screen, specify if you want to create the spoke in a new scope or an existing scope.

    1.  If you choose to create the spoke in a new scope, select an image as the logo for your integration and fill in the fields.

        Here, we will go through an integration with 360Learning as an example.

        |Field|Description|
        |-----|-----------|
        |Spoke name|Name to identify the custom spoke.|
        |Description|Description about the custom spoke.|

        ![Create a spoke in a new scope.](../images/now-assist-spk-gen.png)

        **Note:**

        The value of **App scope name** is the format: `x_<company-code>_<spoke-name>_<spoke>`. By default, the &lt;company-code&gt; is, `snc`. You can configure the company code by configuring **Value** of the system property, **glide.appcreator.company.code**.![Configuring Value of glide.appcreator.company.code.](../images/spoke-gen-sys-property.png)

        This configured value is used when the value **App scope name** is generated.![Configured value of App scope name.](../images/spoke-gen-app-scope.png)

    2.  If you choose to create the spoke in an existing scope, select an image as the logo for your integration and fill in the fields.

        Here, we will go through an integration with 360Learning as an example.

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
</table>4.  Click **Continue**.

5.  On the Build Info screen, select the method using which you want to build your spoke.

6.  Select **Now Assist** and click **Continue** to generate reusable actions by providing the required third-party API documentation snippet.

    ![Create spoke using Now Assist.](../images/now-assist-spk-gen2.png)

7.  On the Generate action screen, paste the required content from the 360Learning API documentation in **Now Assist Context**.

    In this example, we will copy the documentation related to the createGroup action and paste it in **Now Assist Context**.

    **Note:** Ensure that you paste the documentation related to only one action at a time.

    ![Provide content in Now Assist Context.](../images/now-assist-spk-gen-context.png)

8.  Click **Generate Preview**.

    The action preview is generated. Details of the action properties, inputs, outputs, and steps are displayed.

    ![Preview of the provided context.](../images/now-assist-spk-gen-preview.png)

9.  If you want to modify the generated action, modify the provided content in **Now Assist Context** accordingly and click **Regenerate preview**.

    If there are any missing fields in the content provided for **Now Assist Context**, an error message is displayed.

    ![Missing fields in generated action.](../images/now-assist-spk-gen-error.png)

10. Click **Continue**.

11. On the Select connection and category screen, for **Connection and credential alias**, click **Create new**.

12. On the Create new connection and credential alias screen, fill in the fields and provide the alias information.

    |Field|Description|
    |-----|-----------|
    |Connection &amp; Credential name|Name to identify the connection and credential alias record.|
    |Configuration Template for authentication|Required authentication mechanism for this integration. Ensure that the authentication mechanism is compatible with the third-party application.|

    ![Create connection and credential alias record for the spoke.](../images/now-assist-pk-gen-conn.png)

13. Click **Create alias and continue**.

14. On the Configure connection and credential alias screen, fill in the fields to configure the alias.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Base URL to connect to the third-party instance or server.|
    |Credential Information|
    |Based on the configuration template you had selected, the relevant credential fields are displayed. Provide the required values to configure the credential record.|

    If you want configure the alias record later, click **Do it later**.

15. Click **Submit**.

    The connection alias record is created.

16. On the Select connection and category screen:

    -   For a new spoke, leave the category empty. You can update the action properties later on, if needed.

        ![Select Category for an existing spoke.](../images/now-assist-spk-gen-upt-prop.png)

    -   For an existing spoke, assign an existing category.

        If a category is unavailable, create the required action category for your integration in the Action Category \[sys\_hub\_category\] table. You must ensure that the category is created in the same **Application scope** as that of the spoke.

        ![Select the same Application scope as that of the spoke.](../images/now-assist-spk-gen-scope.png)

        ![Action category record for your integration in the Action Category [sys_hub_category] table.](../images/now-assist-spk-gen-category.png)

17. Click **Publish**.

    **Note:** If there are any missing fields, you can't publish the action. Instead you can save the action as a draft by clicking, **Save action as draft**.

    The action is created. You can create another spoke action or navigate to the Spokes page.

    If you have saved action as a draft, you can access these draft actions in the spoke details page under **Actions** &gt; **Draft**.


**Parent Topic:**[Use Now Assist to create spokes and build actions](../concept/now-assist-in-spk-gen.md)

