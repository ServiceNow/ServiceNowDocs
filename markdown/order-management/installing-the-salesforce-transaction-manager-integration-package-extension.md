---
title: Installing the Salesforce Transaction Manager Integration Package extension
description: To use Transaction Manager with Salesforce, you must first follow these steps to install and configure the Salesforce Transaction Manager Integration Package Extension.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Installing the Salesforce Transaction Manager Integration Package extension

To use Transaction Manager with Salesforce, you must first follow these steps to install and configure the Salesforce Transaction Manager Integration Package Extension.

## Prerequisites

This guide assumes that your CPQ environment is integrated with a Salesforce org, and that Transaction Manager is enabled. If your Salesforce org has no CPQ packages installed, install version 2.7 or later of the CPQ Managed Package. For instructions, see [Installation and setup guide for environments linked to Salesforce orgs](installation-and-setup-guide-for-environments-linked-to-salesforce-org.md).

**Note:** CPQ Transaction Manager has no dependencies on Salesforce CPQ. You can ignore any steps or references specific to Salesforce CPQ.

Submit a support ticket requesting Transaction Manager be turned on in your CPQ environment.

## About the CPQ Transaction Manager extension

The CPQ Transaction Manager Extension is a package of components that Salesforce administrators install on their Salesforce environment to facilitate the integration between Salesforce and CPQ Transaction Manager.

Contact ServiceNow customer support for information on the latest version and how to access the managed package for installation.

Admins can install the package for admins only, for all users, or for specific profiles. The package includes permission sets for Transaction Manager that can be assigned to individuals or replicated on profiles. To view the permissions sets, in Setup, go to **Users**, and then see the **Logik.ai Full Access** option in **Permission Sets**.

After it is installed, you can view the version of the package in the **Installed Packages** section of Salesforce Setup.

![Salesforce Setup → Installed Packages](../images/cpq-txn-mgr-logik-txn-mgr-extension.png)

## Salesforce: Enable custom address fields

The Salesforce environment must have Custom Address Fields enabled. If this feature is not enabled, see this article for more information: [Enable Custom Address Fields](https://help.salesforce.com/s/articleView?id=sf.fields_caf_enable.htm&type=5)

## Salesforce: Allow security exceptions for CPQ

Add trusted URLs:

1.  From Salesforce Setup Home, go to **Settings** &gt; **Security** &gt; **Trusted URLs**. Create a new trusted URL.
2.  Provide an API name.
3.  Enter the URL of the CPQ environment, as shown below.

    ![Enable Custom Address Fields](../images/cpq-salesforce-logik-env-url.jpeg)

4.  Under CSP Directives, make sure that at least **frame-src \(iframe content\)** is enabled, and click **Save**.

    ![Enable Custom Address Fields](../images/cpq-salesforce-trusted-urls.jpeg)


Configure remote site settings:

1.  From Salesforce Setup Home, go to **Settings** &gt; **Security** &gt; **Remote Site Settings**. Create a new remote site.
2.  Provide a name.
3.  Enter the URL of the CPQ environment as shown in image below, and click **Save**.

    ![Remote settings](../images/cpq-salesforce-remote-site-name.jpeg)


Optionally, allow microphone access for Cosmo Converse \(currently in beta\). Cosmo Converse allows the user to communicate via voice with Transaction Manager. By default, this feature is not enabled. To use Cosmo Converse, submit a support ticket that describes your use case. To prepare for Cosmo Converse, update Salesforce settings to allow microphone access.

1.  From Setup Home, go to **Settings** &gt; **Security** &gt; **Session Settings**.
2.  Under **Browser Feature Permissions**, make sure that the check box for **Include Permissions-Policy HTTP header** is disabled.
3.  If necessary, click **Save**.

![Session settings](../images/cpq-salesforce-session-settings.jpeg)

## CPQ: Set up the runtime client token

The CPQ runtime client token facilitates authentication for communications from Salesforce to CPQ. For steps to create a runtime client token in CPQ, see [Set up a runtime client](../task/cpq-set-up-a-runtime-client.md). For this Transaction Manager use case, please be sure to enable permissions on this runtime client for TRANSACTION, and add a valid User ID that is recognized by the corresponding Salesforce environment.

Note that in CPQ Admin, the runtime client token must be updated to include TRANSACTION in its permissions and itself as an origin. \(For example, the runtime client token for `https://test-txn.test02.logik.io` must have an origin of `https://test-txn.test02.logik.io`.\) Also, when a runtime client token includes TRANSACTION, a user must be included. Make sure that the user has permission to perform the Create Transaction event.

![Edit runtime client](../images/cpq-salesforce-edit-runtime-client.png)

When you have set up the runtime client token, copy it to your local clipboard for use in the next procedure.

## Install the CPQ Transaction Runtime Token in Salesforce

1.  From the Salesforce App Launcher, search for and open **Logik.io Admin Custom Settings**.
2.  Press the **Set** button next to the **Runtime Client Token** field to enable it.
3.  Paste the token from CPQ into the editable field, and click **Save**.

**Note:** The runtime client token isn’t displayed on the Admin Custom Settings page after it’s been saved.

## Salesforce: Update the Opportunity layout to Open Transaction Manager

1.  In Salesforce, click the gear icon in the top right corner.
2.  Navigate to **Setup** &gt; **Object Manager** &gt; **Opportunity** &gt; **Page Layouts**.
3.  Select the page layout to edit. \(If you have multiple layouts, choose the one associated with the relevant record type or user profiles.\)

    ![Page layouts screen](../images/cpq-salesforce-opp-layout-1.jpg)

4.  Scroll down in the layout editor until you see the **Related Lists** section.

    ![Page layouts screen](../images/cpq-salesforce-opp-layout-2.jpg)

5.  Drag the Transactions object from the list of available related lists on the top palette to the desired position in the **Related Lists** section.

    ![Transactions screen](../images/cpq-salesforce-transactions-obj.gif)

6.  Click the wrench icon for the Transaction object to open the properties for the related list.

    ![Related List Properties](../images/cpq-salesforce-transactions-obj-wrench.png)

7.  In the **Selected Fields** section, select the **Edit Transaction** field from the **Available Fields** column. Click **Add** to move it to the **Selected Fields** column. Rearrange the fields as needed, and click **OK** to save the changes. After making the changes, click **Save** in the top left corner.

    ![Transactions screen](../images/cpq-salesforce-related-lists-properties.png)

8.  Test the updated layout.

    -   As an end user \(on the buyside of Salesforce\), navigate to an Opportunity record.

    -   Ensure that the transaction related list appears on the page and that the **Edit Transaction** link is visible and functional.


## Troubleshooting: If the Transaction button is missing

If the transaction button is missing from the buyside opportunity detail page, follow these steps.

1.  In the top right corner of the page, click the gear icon, and then click **Edit Page**. This opens the Lightning App Builder for the Opportunity record page.

    ![Edit page option](../images/cpq-txn-mgr-troubleshooting-1.jpg)

2.  Select the Related Lists component of the page. In the **Assign Page Layouts** section, find the name of the page layout currently assigned. \(In the image, the correct layout is indicated with the word "\(previewed\)."\)

    ![menu](../images/cpq-txn-mgr-troubleshooting-2.jpg)

3.  Click the previewed layout and repeat steps 4 through 7 in the "Salesforce: Update the Opportunity layout to Open Transaction Manager" section \(above\). Next, on the buyside, navigate to an opportunity record. Check the **Related Lists** section to confirm that the transaction object appears. Click the arrow, and create a new transaction to validate that the **Edit Transaction \(EditLink\_\_c\)** field is available.

    ![Troubleshooting](../images/cpq-txn-mgr-troubleshooting-3.jpg)

    ![troubleshooting](../images/cpq-txn-mgr-troubleshooting-4.jpg)


## Salesforce: Set up custom field mappings

When a new CPQ transaction record is initiated in CPQ, it can be helpful to transfer essential data from the Salesforce transaction record. This section sets up field mappings that copy \(or "twin"\) information from a field in Salesforce to a field in CPQ, or visa versa, during the transaction creation flow. As an example, it is common for the administrator to twin the value held in **LGK\_\_OpportunityId\_\_c** to the corresponding CPQ transaction field, **txn.opportunity.id**.

1.  In Salesforce, go to Setup.
2.  In the Quick Find bar, search for `Custom Metadata Types`.
3.  In the search results, under Custom Code, click **Custom Metadata**.

    ![Home page](../images/cpq-salesforce-custom-meta-types.jpg)

4.  To access the existing field mappings, locate **Logik.io Transaction Field Mapping** in the list of custom metadata types, and click the **Manage Records** link next to it.

    ![Metadata types](../images/cpq-salesforce-custom-meta-types-all.png)

5.  Click **New**, fill out the required details, and then click **Save**.

    Source fields:

    -   Environment: Choose the source of the field value:
        -   Select **Salesforce** for fields originating in Salesforce.

        -   Select **Logik** for fields originating in CPQ.

    -   Object: Enter `Transaction`.
    -   Field: Specify the field name.
        -   For Salesforce fields, include the `__c` suffix \(for example, `CustomField__c`\). Review the exact field names from **Salesforce** &gt; **Setup** &gt; **Object Manager** &gt; **Transaction** &gt; **Fields** and relationships.

            ![Field relationship](../images/cpq-salesforce-fields-relationships.jpeg)

        -   For CPQ fields, include prefixes such as `txn.` or `txn.line.` to denote the field \(for example, `txn.TotalAmount`\). Be sure to use the exact field variable names from **Admin** &gt; **Transaction** &gt; **Associated Fields**.

            ![Transactions](../images/cpq-txn-mgr-assoc-fields.jpeg)

    Target fields:

    -   Environment: Indicate where the field value should be updated \(Salesforce or CPQ\).
    -   Field: Enter the field name of the target in the same format \(for example, Salesforce fields with `__c` or CPQ fields with `txn.` prefixes\).

        ![Metadata screen](../images/cpq-salesforce-custom-meta-types-mapping.jpeg)


**Note:**

-   A field mapping record is included as a reference. This cannot be deleted, but its source and target details can be edited. Verify that your custom added field record matches it.
-   If you are uninstalling the managed package, any created records for new custom fields must be deleted first.

## Salesforce: Activate Transaction Line to Opportunity Line syncing and asset flows

**Note:** By default, the following flows are active:

-   Logik.ai Copy Transaction
-   Logik.ai Create Transaction \(Record Trigger\)
-   Logik.ai Create Transaction \(Screen\)

1.  From Salesforce Setup Home, search for "Flows". Click **Process Automation** &gt; **Flows**.

2.  Search for the following. You will perform step 3 for each:

    -   Logik.io Opportunity Line Sync \(Upsert\)
    -   Logik.io Opportunity Line Sync \(Delete\)
    -   Logik.io Primary Transaction Change
3.  For each of the three flows identified in step 2, activate one of the following options:
    -   Option 1: Using the drop-down menu:
        -   Click the arrow to the right of the flow name.

            ![Details list](../images/cpq-txn-mgr-asset-flows-1.jpg)

        -   Select **View Details and Versions**.
        -   Click **Activate** for the most recent version of the flow.

            ![Flow versions](../images/cpq-txn-mgr-asset-flows-2.jpg)

    -   Option 2: Open the flow:
        -   Click the flow name to open it in the Flow Builder.

            ![Flowbuilder](../images/cpq-txn-mgr-asset-flows-3.jpg)

        -   Click **Activate** at the top right of the Flow Builder.

            ![workflow](../images/cpq-txn-mgr-asset-flows-4.jpg)


Make sure all the flows are in active status.

**Note:** Opportunity line syncing is applied only to the transaction assigned to the Primary Transaction opportunity field.

## End-user flow: Launching a CPQ transaction from Salesforce

-   Create a transaction record in Salesforce

    There are several ways for the end user to initiate a CPQ transaction in Salesforce. The most common flow starts on the Opportunity record.

    1.  From an Opportunity record, click the arrow in the transaction's related list, and then click **New**.

        ![Sales console](../images/cpq-salesforce-create-transaction-record-1.png)

    2.  A new transaction opens with the **Opportunity** field populated. Fill in **Account**, **Primary Contact**, and any optional fields. Click **Save**.

        ![New transaction](../images/cpq-salesforce-create-transaction-record-2.png)

    3.  A record-triggered flow in the managed package creates a new transaction in CPQ. The UUID of the new CPQ transaction record updates in Salesforce \(**LGK\_\_TransactionUUID\_\_c**\). If the transaction ID does not appear immediately, refreshing the browser usually corrects the anomaly.

        ![Transaction details](../images/cpq-salesforce-create-transaction-record-3.png)

        If the **Transaction Id** field remains unpopulated after a browser refresh, see the Troubleshooting section below.

-   Edit a transaction

    From a Salesforce transaction \(or a transaction related list\), Transaction Manager can be launched using either the **Edit Transaction** button on the transaction detail page or the link available via the **Edit Transaction** field. This loads a CPQ transaction based on the **Transaction Id** field in the Salesforce record.

    Transaction Manager loads in an iFrame, replacing the current subtab in Salesforce.

    **Note:** Salesforce's classic UI is not supported.

-   Copy Transaction

    By clicking the **Clone** button on the Salesforce transaction record, users can call a CPQ Copy event to recreate the transaction and lines in Transaction Manager. This action is based on the transaction ID on the header record in Salesforce and results in a cloned transaction record.

    **Note:** Cloning a transaction from Salesforce does not automatically make copies of the affiliated line records to the new transactions. To clone the lines to the new transaction, launch the new \(cloned\) transaction record in Transaction Manager, and initiate a Salesforce sync.


## Troubleshooting: CPQ fails to launch with a “Transaction with id ‘null’ could not be found” error

![Error message](../images/cpq-txn-mgr-null-id-error.jpeg)

This error occurs when the creation of a new CPQ transaction record is initiated via API call from Salesforce and fails. This failure usually occurs due to one of two reasons:

-   The Transaction runtime token is incorrectly set up or has expired. Review the steps in the "CPQ: Set Up the runtime client token" section above.
-   The user creating the CPQ transaction record from the Salesforce UI does not have permission to do so.

To troubleshoot permissions errors, follow these steps.

1.  In Transaction Administration, click **Personas**.
2.  In the list of personas, observe which persona is labeled DEFAULT. The screenshot below shows that "Sales Rep" is the default persona. By default, all new users are assigned this persona.

    ![Related List Properties](../images/cpq-txn-mgr-personas.png)

3.  Open each persona record. Find your user name. The user you are debugging should only be visible in one persona. Once you find the appropriate persona, note the view that manages this persona’s access. In the example, the user is among the listed user names in the Sales Rep persona. This persona’s access is managed by the "sales" view.

    ![Personas screen](../images/cpq-txn-mgr-persona-managed-by.png)

4.  Open the view that manages the persona’s access. In our example, the view is named "sales". To open the view, in CPQ Transaction Admin Home, go to Views, and then click the managing view.

    ![Transaction details](../images/cpq-txn-mgr-personas-view.png)

5.  On the view detail page, click **Access**, click **Events**, and search for `createTransaction`. In the initial stage, the create transaction event \(varname: createTransaction\) must be set to **Active**.

    ![Sales screen](../images/cpq-txn-mgr-personas-events.png)


To sum up: for any given user, the administrator must manage the items in the following table.

<table id="table_o1w_3kp_ghc"><thead><tr><th>

Issue

</th><th>

Correctio

</th></tr></thead><tbody><tr><td>

User persona assignment

</td><td>

Navigate to **Personas** in CPQ Transaction Admin, and select a persona record.

 -   To add a user to a persona, click **+ Associate Users**.
-   To remove a user from a persona, select a user name, and then click **Remove Selected**.

</td></tr><tr><td>

Persona view assignment

</td><td>

In CPQ Transaction Admin, go to **Views**, select a view record, and then click **Associated Personas**.

</td></tr><tr><td>

View: access to each event, per stage

</td><td>

For information about how to perform fine-grained access administration \(recommended\), see the Events CSV File section in [Transaction Manager: Views](transaction-manager-views.md).

 To administer access in a less precise way, go to Events in CPQ Transaction Admin, click the **Create Transaction** event, click **Edit Event Access**, and set the event access to Active. By default, the event is active across all stages and views.

</td></tr></tbody>
</table>