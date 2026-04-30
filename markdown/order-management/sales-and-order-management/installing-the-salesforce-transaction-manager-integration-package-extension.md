---
title: Installing the Salesforce Transaction Manager Integration Package extension
description: To use Transaction Manager, you must first follow these steps to install and configure the Salesforce Transaction Manager Integration Package Extension.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-10"
reading_time_minutes: 12
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Installing the Salesforce Transaction Manager Integration Package extension

To use Transaction Manager, you must first follow these steps to install and configure the Salesforce Transaction Manager Integration Package Extension.

## Prerequisites

This guide assumes that your ServiceNow CPQ environment is integrated with a Salesforce org, and that Transaction Manager is enabled. If your Salesforce org has no ServiceNow CPQ packages installed, see [Installation and setup guide for environments linked to Salesforce orgs](installation-and-setup-guide-for-environments-linked-to-salesforce-org.md) and install Managed Package version 2.7 or later.

**Note:** ServiceNow CPQ Transaction Manager has no dependencies on Salesforce CPQ. You can ignore any steps or references specific to Salesforce CPQ.

Submit a Support ticket requesting Transaction Manager be turned on in your ServiceNow CPQ environment.

## About the ServiceNow CPQ Transaction Manager extension

The Transaction Manager Extension is a package of components that Salesforce administrators install on their Salesforce environment to facilitate the integration between Salesforce and Transaction Manager.

Contact customer support for information on how to access the managed package.

After it is installed, you can view the version of the package in Salesforce Setup → Installed Packages.

![Salesforce Setup → Installed Packages](../images/cpq-txn-mgr-logik-txn-mgr-extension.png)

## Salesforce: Enable custom address fields

The Salesforce environment must have Custom Address Fields enabled. If this feature is not enabled, see this article for more information: [Enable Custom Address Fields](https://help.salesforce.com/s/articleView?id=sf.fields_caf_enable.htm&type=5)

## Salesforce: Allow security exceptions for ServiceNow CPQ

Add trusted URLs:

1.  From Salesforce Setup Home, go to Settings → Security → Trusted URLs. Create a "New Trusted URL".
2.  Provide an API name.
3.  Enter the URL of the ServiceNow CPQ environment, as shown below.

    ![Enable Custom Address Fields](../images/cpq-salesforce-logik-env-url.jpeg)

4.  Under CSP Directives, make sure at least "frame-src \(iframe content\)" is enabled, and click **Save**.

    ![Enable Custom Address Fields](../images/cpq-salesforce-trusted-urls.jpeg)


Configure remote site settings:

1.  From Salesforce Setup Home, go to Settings → Security → Remote Site Settings. Create a "New Remote Site".
2.  Provide a name.
3.  Remote Site URL: enter the URL of the ServiceNow CPQ environment as shown in image below, and click **Save**.

    ![Remote settings](../images/cpq-salesforce-remote-site-name.jpeg)


Optionally, allow microphone access for Cosmo Converse \(currently in beta\). Cosmo Converse allows the user to communicate via voice with Transaction Manager. This feature is not enabled by default. To use Cosmo Converse, please submit a support ticket that describes your use case. To prepare for Cosmo Converse, update Salesforce settings to allow microphone access.

1.  From Setup Home, go to Settings → Security → Session Settings.
2.  Under Browser Feature Permissions, make sure the checkbox for the setting "Include Permissions-Policy HTTP header" is disabled.
3.  If needed, Save.

![Session settings](../images/cpq-salesforce-session-settings.jpeg)

## ServiceNow CPQ: Set up the Runtime Client Token

The ServiceNow CPQ Runtime Client Token facilitates authentication for communications from Salesforce to ServiceNow CPQ. For steps to create a Runtime Client Token in ServiceNow CPQ, see [Set up a runtime client](../task/cpq-set-up-a-runtime-client.md). For this Transaction Manager use case, please be sure to enable permissions on this Runtime Client for ‘Transaction’ and add a valid User ID recognized by the correlative Salesforce environment.

Note that in ServiceNow CPQ Admin, the Runtime Client Token will need to be updated to include "TRANSACTION" in its permissions and itself as an origin. \(For example, the Runtime Client Token for https://test-txn.test02.logik.io must have an origin of `https://test-txn.test02.logik.io`.\) Also, when a Runtime Client Token includes TRANSACTION, a user must be included. Make sure the user has permission to perform the Create Transaction event.

![Edit runtime client](../images/cpq-salesforce-edit-runtime-client.png)

When you have set up the runtime client token, copy it to your local clipboard for use in the next procedure.

## Install the ServiceNow CPQ Transaction Runtime Token in Salesforce

1.  From the Salesforce App Launcher, search for and open **Logik.io Admin Custom Settings**.
2.  Press the "Set" button next to the "Runtime Client Token" field to enable it.
3.  Paste the token from ServiceNow CPQ into the editable field, and click **Save**.

![Basic settings](../images/cpq-salesforce-admin-pkg-settings.png)

**Note:** The Runtime Client Token isn’t displayed on the Admin Custom Settings page after it’s been saved.

## Salesforce: Update the Opportunity layout to Open Transaction Manager

1.  In Salesforce, click the gear icon in the top-right corner.
2.  Navigate to Setup → Object Manager → Opportunity → Page Layouts.
3.  Select the page layout to edit. \(If you have multiple layouts, choose the one associated with the relevant record type or user profiles.\)

    ![Page layouts screen](../images/cpq-salesforce-opp-layout-1.jpg)

4.  Scroll down in the layout editor until you see the Related Lists section.

    ![Page layouts screen](../images/cpq-salesforce-opp-layout-2.jpg)

5.  Drag the Transactions object from the list of available Related Lists on the top palette to the desired position in the Related Lists section.

    ![Transactions screen](../images/cpq-salesforce-transactions-obj.gif)

6.  Click the wrench icon \(Related List Properties\) for the Transaction object.

    ![Related List Properties](../images/cpq-salesforce-transactions-obj-wrench.png)

7.  In the Selected Fields section, select the Edit Transaction field from the Available Fields column. Click **Add** to move it to the Selected Fields column. Rearrange the fields as needed, and click **OK** to save the changes. After making the changes, click **Save** in the top-left corner.

    ![Transactions screen](../images/cpq-salesforce-related-lists-properties.png)

8.  Test the updated layout.

    -   As an end-user \(on the buyside of Salesforce\), navigate to an Opportunity record.

    -   Ensure the Transaction Related List appears on the page and that the Edit Transaction link is visible and functional.


## Troubleshooting: If the Transaction button is missing

If the transaction button is missing from the buyside opportunity detail page, follow these steps.

1.  In the top-right corner of the page, click the gear icon and then click **Edit Page**. This will open the Lightning App Builder for the Opportunity Record Page.

    ![Edit page option](../images/cpq-txn-mgr-troubleshooting-1.jpg)

2.  Select the Related Lists component of the page. Under the section labeled Assign Page Layouts, find the name of the page layout currently assigned \(e.g., in image, the correct layout can be seen with a ‘previewed’ keyword in parenthesis\).

    ![menu](../images/cpq-txn-mgr-troubleshooting-2.jpg)

3.  Click the previewed layout and repeat the steps that you did in step 4 through 7 \(from the Update Opportunity Layout to Open Transaction Manager section, above\). After this, on the buyside, navigate to an opportunity record; check the Related Lists section to confirm that the Transaction object now appears. Click the arrow and create a new Transaction to validate that the Edit Transaction \(EditLink\_\_c\) field is available.

    ![Troubleshooting](../images/cpq-txn-mgr-troubleshooting-3.jpg)

    ![troubleshooting](../images/cpq-txn-mgr-troubleshooting-4.jpg)


## Salesforce: Set up custom field mappings

When a new ServiceNow CPQ Transaction record is initiated in ServiceNow CPQ, it can be helpful to transfer essential data from the Salesforce Transaction record. This section sets up field mappings that will copy \(or ‘twin’\) information from a field in Salesforce to a field in ServiceNow CPQ, or visa versa, during the Create Transaction flow. As an example, it is common for the administrator to ‘twin' the value held in `LGK__OpportunityId__c` to the corresponding ServiceNow CPQ transaction field, txn.opportunity.id.

1.  In Salesforce, go to Setup.
2.  In the Quick Find bar, search for Custom Metadata Types.
3.  In the search results, under Custom Code, click **Custom Metadata**.

    ![Home page](../images/cpq-salesforce-custom-meta-types.jpg)

4.  To access the existing field mappings, locate Logik.io Transaction Field Mapping in the list of Custom Metadata Types and click the **Manage Records** link next to it.

    ![Metadata types](../images/cpq-salesforce-custom-meta-types-all.png)

5.  Click New; fill out the required details and click **Save**.

    Source fields:

    -   Environment: Choose the source of the field value:
        -   Select Salesforce for fields originating in Salesforce.

        -   Select **Logik** for fields originating in ServiceNow CPQ.

    -   Object: Enter "Transaction" \(the only valid value currently\).
    -   Field: Specify the field name.
        -   For Salesforce fields, include the `__c` suffix \(e.g., `CustomField__c`\). Review the exact field names from Salesforce → Setup → Object Manager → Transaction → Fields and relationships.

            ![Field relationship](../images/cpq-salesforce-fields-relationships.jpeg)

        -   For ServiceNow CPQ fields, include prefixes such as `txn.` or `txn.line.` to denote the field \(e.g., `txn.TotalAmount`\). Be sure to use the exact field variable names from ServiceNow CPQ Admin → Transaction → Associated Fields.

            ![Transactions](../images/cpq-txn-mgr-assoc-fields.jpeg)

    Target fields:

    -   Environment: Indicate where the field value will be updated \(Salesforce or ServiceNow CPQ\)
    -   Field: Enter the field name of the target in the same format \(e.g., Salesforce fields with `__c` or ServiceNow CPQ fields with `txn.` prefixes\).

        ![Metadata screen](../images/cpq-salesforce-custom-meta-types-mapping.jpeg)


**Note:**

-   A field mapping record is included as a reference. This cannot be deleted, but its Source and Target details can be edited. Verify that your custom added field record matches with it.
-   If you are uninstalling the managed package, any created records for new custom fields will need to be deleted first.

## Salesforce: Activate Transaction Line → Opportunity Line syncing and asset flows

1.  From Salesforce Setup Home, search ‘Flows’. Click Process Automation → Flows.

2.  Search for the following – you will perform step 3 for each:

    -   Logik.io Opportunity Line Sync \(Upsert\)
    -   Logik.io Opportunity Line Sync \(Delete\)
    -   Logik.io Primary Transaction Change
    -   Logik.io Asset to Transaction
    -   Logik.io Transaction to Asset
3.  For each of the five flows identified in step 2, activate one-by-one via either of the following options:
    -   Option 1: Using the Dropdown Menu:
        -   Click the dropdown arrow to the right of the flow name.

            ![Details list](../images/cpq-txn-mgr-asset-flows-1.jpg)

        -   Select **View Details and Versions**.
        -   Click **Activate** for the most recent version of the flow.

            ![Flow versions](../images/cpq-txn-mgr-asset-flows-2.jpg)

    -   Option 2: Open the Flow:
        -   Click the flow name to open it in the Flow Builder.

            ![Flowbuilder](../images/cpq-txn-mgr-asset-flows-3.jpg)

        -   Click **Activate** at the top-right of the Flow Builder.

            ![workflow](../images/cpq-txn-mgr-asset-flows-4.jpg)


Make sure all the flows are in active status.

**Note:**

-   Opportunity Line Syncing will only be applied to the Transaction assigned to the “Primary Transaction” Opportunity field.
-   The **Update Assets** button will only appear on the Transaction detail layout if the Transaction to Asset flow is activated.

## Salesforce: Define the Product Identifier in the Asset to Transaction flow

In the existing “Logik.io Create Transaction” flow, there is a new parameter for creating Transaction Lines when initiating an asset amendment. This parameter is defined on the Apex Action, labeled “Product Identifier”. By default, the value is `ProductCode`, but it should be defined based on your ServiceNow CPQ environment setting for Product Id. Acceptable values are `ProductCode`, `PartnerId`, and `ExternalId`.

![Create transaction screen](../images/cpq-txn-mgr-prod-id-1.png)

![config settings](../images/cpq-txn-mgr-prod-id-2.jpg)

## Salesforce: Add the Amend button to the asset list

1.  In Setup, type Object Manager in the Quick Find bar and click it.
2.  Open the Account object, and select **Page Layouts**. Then, click the layout you want to edit.
3.  In the layout editor, scroll to the Related Lists section. If the Assets related list is not already added, drag it from the component palette to the related list section.
4.  Click the wrench icon \(Related List Properties\) for the Assets related list. Scroll to the bottom of the properties dialog, and expand the Buttons section.
5.  In the Buttons section, move the **Amend** button from Available Buttons to Selected Buttons, and click **OK**.
6.  In the layout editor, click **Save** to apply your changes.

![Related list properties](../images/cpq-txn-mgr-amend-button.png)

## End-user flow: Launching a ServiceNow CPQ transaction from Salesforce

-   Create a Transaction Record in Salesforce

    There are several ways for the end-user to initiate a ServiceNow CPQ transaction in Salesforce. The most common flow starts on the Opportunity record.

    1.  From an Opportunity record, click the arrow in the Transactions related list. Select ‘New’.

        ![Sales console](../images/cpq-salesforce-create-transaction-record-1.png)

    2.  User is presented with a New Transaction. Opportunity will be populated. Fill in Account, Primary Contact, and any optional fields. Save.

        ![New transaction](../images/cpq-salesforce-create-transaction-record-2.png)

    3.  A Record-Triggered flow in the managed package will create a new transaction in ServiceNow CPQ. The UUID of the new ServiceNow CPQ Transaction record will update in Salesforce \(`LGK__TransactionUUID__c`\). If the Transaction Id does not appear immediately, a browser refresh usually corrects the anomaly.

        ![Transaction details](../images/cpq-salesforce-create-transaction-record-3.png)

        If the Transaction Id remains unpopulated after a browser refresh, see the following Troubleshooting section.

-   Edit Transaction

    From a Salesforce Transaction \(or a Transaction Related List\), Transaction Manager can be launched from either the "Edit Transaction" button \(only available on the Transaction Detail Page\), or the link available from the "Edit Transaction" field. This will load a ServiceNow CPQ transaction based on the "Transaction Id" field on the Salesforce record.

    Transaction Manager will load in an iframe, replacing the current subtab in Salesforce.

    **Note:** Salesforce Classic UI is not supported.

-   Copy Transaction

    Using the “Clone” button on the Salesforce transaction record, users can call ServiceNow CPQ Copy event to recreate the Transaction and Lines in Transaction Manager. This is based on the Transaction Id on the header record in Salesforce, and will result in a cloned transaction record.

    **Note:** Cloning a Transaction from Salesforce does not automatically make copies of the affiliated line records to the new Transactions. To clone the lines to the new Transaction, launch the new \(cloned\) Transaction record in Transaction Manager; initiate a Salesforce sync.


## Troubleshooting: ServiceNow CPQ fails to launch with “Transaction with id ‘null’ could not be found” error

![Error message](../images/cpq-txn-mgr-null-id-error.jpeg)

This error occurs when the creation of a new ServiceNow CPQ Transaction record is initiated via API call from Salesforce and fails. This failure usually occurs due to two reasons:

-   The Transaction Runtime token is incorrectly set up or has expired. Review the steps in the "ServiceNow CPQ: Set Up the Runtime Client Token" section above.
-   The user initiating the new ServiceNow CPQ Transaction record creation from the Salesforce UI does not have permission to do so.

To troubleshoot permissions errors, follow these steps.

1.  In Transaction Administration, click **Personas**.
2.  In the list of Personas, observe which Persona is labeled ‘DEFAULT’. The screenshot below shows that ‘Sales Rep’ is the default Persona. This means that by default, all new users are assigned this Persona.

    ![Related List Properties](../images/cpq-txn-mgr-personas.png)

3.  Open each Persona record. Find your username; the user you are debugging should only be visible in one Persona. Once you find the appropriate Persona, take note of the View that manages this Persona’s access. In our example, my user is among the listed usernames in the Sales Rep Persona. This Persona’s access is managed by the ‘sales’ View.

    ![Personas screen](../images/cpq-txn-mgr-persona-managed-by.png)

4.  Open the View that manages this Persona’s access. In our example, the View is named ‘sales’. Navigation: ServiceNow CPQ Transaction Admin Home → Views → Click ‘sales’.

    ![Transaction details](../images/cpq-txn-mgr-personas-view.png)

5.  On the ‘sales’ View detail page, click **Access**, click **Events**, and search for “createTransaction”. In the initial Stage, the Create Transaction \[varname: createTransaction\] Event must be set to ‘Active’.

    ![Sales screen](../images/cpq-txn-mgr-personas-events.png)


In sum, for any given user, the administrator must manage the items in the following table.

<table id="table_o1w_3kp_ghc"><thead><tr><th>

Issue

</th><th>

Correctio

</th></tr></thead><tbody><tr><td>

User → Persona assignment

</td><td>

Navigate to ServiceNow CPQ Transaction Admin → Personas, and select a Persona record.

 -   Select a Username + ‘Remove Selected’ to remove a user from a Persona.
-   Select “+ Associate Users” to add a user to a Persona.

</td></tr><tr><td>

Persona → View assignment

</td><td>

Navigate to ServiceNow CPQ Transaction Admin → Views, select a View record, and click the Associated Personas button.

</td></tr><tr><td>

View: access to each Event, per Stage

</td><td>

-   Fine-grained access administration \(recommended\): review [Transaction Manager: Views](transaction-manager-views.md), especially the Events CSV File section.
-   Broad-brush access administration: Navigate to ServiceNow CPQ Transaction Admin → Events, select ‘Create Transaction’ Event, click ‘Edit Event Access’, and set ‘Active’. This will set this event to be active across all Stages and Views, by default. The administrator will need to fine-tune access accordingly.


</td></tr></tbody>
</table>