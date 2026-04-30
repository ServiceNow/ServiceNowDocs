---
title: Create a Salesforce CRM integration
description: Integrate your ServiceNow instance with the Salesforce customer relationship management \(CRM\) services to track your software subscriptions and to reclaim unused licenses by using the guided walk-through playbook.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Playbook for SaaS integrations, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a Salesforce CRM integration

Integrate your ServiceNow instance with the Salesforce customer relationship management \(CRM\) services to track your software subscriptions and to reclaim unused licenses by using the guided walk-through playbook.

## Before you begin

Role required: Salesforce admin, sam\_admin

-   Create the Salesforce CRM integration only in the Global scope.

## About this task

**Note:** The **Client Credentials** grant type is supported in Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) 16.1.0, Salesforce CRM application 2.0.2, and Salesforce CRM Spoke 2.4.0 version onwards.

## Procedure

1.  From your ServiceNow instance, navigate to **Software Asset Workspace** &gt; **Software asset analytics**.

2.  Select **Create direct integration**.

3.  In the list of supported integrations, select **Salesforce CRM**.

4.  Register the Salesforce application through the Salesforce admin portal.

    For more information, see [Register a Salesforce application](../concept/integrate-with-salesforce-crm.md#).

    1.  Select **Register a Salesforce application** in the side pane.

    2.  Complete the tasks in the Salesforce application.

        Select each check box as you complete each step.

    3.  Select **Mark Complete**.

5.  Create an integration profile to track software subscriptions and optimize licensing.

    1.  Select **Profile details** in the left pane.

    2.  On the form, fill in the fields,

        |Field|Description|
        |-----|-----------|
        |Display name|Name of the integration profile to identify uniquely the organization for which you’re creating the profile.|
        |Status|Status of the integration profile. If you have not published the integration profile, this field is automatically set to **Draft**. If you have already published the integration profile, this field is automatically set to **Published**.|
        |Profile type|Type of integration profile. This value is automatically set to Salesforce CRM.|
        |Download subscription subflow|The value must be set to **Salesforce CRM Download Subscriptions**.|
        |Reclaim subscription subflow|The value must be set to **Salesforce CRM Reclaim Subscription**.|

    3.  Save your data.

        -   To save your data without continuing the integration, select **Save**.
        -   To save your data and continue the integration, select **Mark Complete**.
6.  Create a connection and credential in the ServiceNow Classic interface.

    1.  Select **Connection and credential** in the left pane.

    2.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field.

    3.  Select **Continue**.

    4.  Select the **Create New Connection &amp; Credential** link.

    5.  On the form, fill in the fields.

<table id="table_nng_qhr_xnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the connection to identify uniquely the Salesforce organization for which you’re creating this connection and credential.

</td></tr><tr><td>

Connection URL \(Instance URL\)

</td><td>

URL that displays after logging in to Salesforce, which is the custom domain URL of Salesforce.

</td></tr><tr><td class="sub-head" colspan="2">

Credential information

</td></tr><tr><td>

Grant type

</td><td>

The grant type for your application according to your authentication needs. Possible values are: -   **Authorization Code**
-   **Client Credentials**


</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID \(consumer key\) assigned to your Salesforce application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret \(consumer secret\) assigned to your Salesforce application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This is generally the URL of the ServiceNow instance that you specified while registering a Salesforce application in [Step 4](playbook-salesforce-crm.md#step4).

</td></tr></tbody>
</table>    6.  Select **Create and Get OAuth Token**.

    7.  In the OAuth2 authentication dialog box, log in to the same Salesforce admin account that you used to create your Salesforce application.

        If you have selected **Client Credentials** as the grant type, the OAuth2 dialog box doesn't appear.

        Your ServiceNow instance creates an OAuth token for Salesforce.

    8.  Select **Mark Complete**.

    The integration profile uses the Salesforce CRM Download Subscriptions and Salesforce CRM Reclaim Subscription subflows to retrieve user data from your Salesforce CRM services.

7.  Create a child alias and an extra integration profile.

    The child alias uniquely identifies the connection and credentials for this additional integration profile.

    The first Salesforce CRM integration profile that you create uses the default \(parent\) connection and credential alias for Salesforce. Each additional Salesforce CRM integration profile that you create requires a unique child alias that helps differentiate the connection and credentials between each integration profile.

    **Note:** The application scope must be set to **Salesforce Spoke**.

    1.  Select **Connect to additional Salesforce org \(Optional\)** in the left pane.

    2.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png)next to the **Connection &amp; Credential** field.

        The display redirects to the ServiceNow Classic interface where you can configure the child alias.

    3.  In the **Child Aliases** tab, select **New**.

    4.  Enter a name for the child alias in the Connection and Credential Aliases form.

    5.  Select **Submit**.

        After the form reloads, you can see the newly created child alias in the **Child Aliases** list.

    6.  Select the **Create New Connection &amp; Credential** related link to create multiple connections.

        Follow the same steps as for creating the parent connection.

    7.  Select **Mark Complete** after you have completed the steps and select all the check boxes in the Playbook view.

8.  Review the required fields before publishing the integration profile.

    1.  Select **Review and Publish** in the left pane.

    2.  Review the details of the integration profile.

    3.  In the Connection &amp; Credential field, select the preview icon ![](../image/preview-icon.png) to locate and select the child alias that you created in [Step 7](playbook-salesforce-crm.md#step-7).

        Selecting the child alias associates the additional integration profile with the child alias. Your ServiceNow instance uses this alias to identify the connection and credentials for this integration profile.

    4.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

        **Note:** For more information, see [Minimal user permissions](../concept/integrate-with-workfront.md#) table.

        1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Salesforce CRM Download Subscriptions**.

            **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

        2.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Salesforce CRM Reclaim Subscription**.

            **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

    5.  Select **Save**.

    6.  Select **Validate Connection**.

9.  Select **Publish** to publish the integration profile.

10. Verify whether the status of all scheduled job results is complete.


## Result

After the integration is published successfully, you’re redirected to the record page. You can view the details of the integration profile, associated software models, triggered scheduled jobs, scheduled job results, and unrecognized subscription identifier.

**Parent Topic:**[Playbook for SaaS integrations](../concept/playbook-saas-integrations.md)

