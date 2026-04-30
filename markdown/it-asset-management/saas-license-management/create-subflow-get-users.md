---
title: Create a subflow to get users
description: Create a subflow to add a list of users to the Software Subscription table.Configure an identifier if it doesn't exist to identify an integration.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a subflow to get users

Create a subflow to add a list of users to the Software Subscription table.

## Before you begin

This subflow requires a data stream action to get users. For more information, see [Create a data stream action to get users](create-data-stream-action-slc.md).

Role required: flow\_designer or admin

## About this task

**Note:** For examples of subflows to get users, see the Jira Download Subscriptions and Webex Download Subscriptions subflows.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Select **New** and then select **Subflow**.

3.  On the form, fill in the fields.

<table id="table_dk4_brb_njb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your choice. For example, `Application` Download Subscriptions, where `Application` is the name of the SaaS application that you're integrating with.

</td></tr><tr><td>

Application

</td><td>

Software Asset Management - SaaS License Management

</td></tr><tr><td>

Accessible From

</td><td>

Select **All application scopes**.

</td></tr><tr><td>

Category

</td><td>

Leave this field empty.

</td></tr><tr><td>

Protection

</td><td>

Select **None**.

</td></tr><tr><td>

In-Flow Annotation

</td><td>

Leave this field empty.

</td></tr><tr><td>

Description

</td><td>

Description of your choice.

</td></tr><tr><td>

Run As

</td><td>

User who initiates session.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Add an integration profile input.

    |Label|Name|Type|Required|
    |-----|----|----|--------|
    |Integration profile|integration\_profile|Reference.Integration Profile|Yes|

6.  In the Actions section, select the plus icon and then select **Action** to add a new action.

7.  Select the spoke for the SaaS application that you want to integrate with from the list of installed spokes.

    **Note:** To add additional spokes to your list of installed spokes, request them on the [ServiceNow Store](https://store.servicenow.com). For a complete list of available spokes, see [IntegrationHub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US). If there’s no existing spoke for the SaaS application that you want to integrate with, you can [create a new spoke](create-saas-spoke.md).

8.  Select a data stream action to get users.

9.  Define the values to pass for any user authentication inputs for the data stream action.

    The data stream action might return users that you don't want to include in your list of user subscriptions. If you perform filtering to exclude some users, add an If flow logic as a child of the get users data stream action.

    The amount of filtering required, if any, depends on the application you're integrating with. For example, if the user targetObject has an **active** property, you could add a condition to check that the value is **true** to confirm that the subflow doesn't download deactivated users. An example of filtering used by the Jira Download Subscriptions subflow is that the account type can’t be **app** to help prevent the subflow from returning accounts that aren’t actual users.

    Add conditions to the If flow logic for any required filtering.

    -   If you're using an If flow logic to filter users, add the **Upsert user subscription using subscription identifier** action from the Software Asset Management spoke as a child of the flow logic.
    -   If you're not filtering users, add the **Upsert user subscription using subscription identifier** action as a child of the get users data stream action. This action adds the SaaS application user subscription to the Software Subscription table \[samp\_sw\_subscription\]. If the subscription is already in the table, the action updates the subscription record.
10. Fill in the inputs that are applicable to your integration.

    Use values from the data panel to fill in the action inputs. Your ask to the SaaS API might not return data for all the inputs.

<table id="table_cch_lsr_njb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

External user id

</td><td>

User id or account id from the user targetObject. This is generally a numeric, non human-readable value. This value must be unique.

</td></tr><tr><td>

User principal name

</td><td>

Email address from the user targetObject. If an email address isn’t available, use another value such as user name plus user id. This value should be human readable.

</td></tr><tr><td>

Integration profile

</td><td>

Integration profile input that you created for the subflow.

</td></tr><tr><td>

Last Activity

</td><td>

Date of most recent activity from the user targetObject. For example, the last login time.

</td></tr><tr><td>

External created

</td><td>

Account creation date from the user targetObject.

 This value helps create better reclamation candidates. A new user might not have any activity yet. If the record shows that the user account was created, a reclamation candidate isn't created for that user because it's a new account rather than an unused account.

</td></tr><tr><td>

Identifier

</td><td>

A unique identifier to identify the integration. Software models are automatically created for subscription with an identifier that matches an identifier in the Subscription Product Definitions \[samp\_sw\_subscription\_product\_definition\] table.

If an identifier doesn't exist, configure an identifier. For more information, see [Configure an identifier](create-subflow-get-users.md#).

</td></tr><tr><td>

Additional attributes

</td><td>

This is used to update any other field on the Software Subscriptions \[samp\_sw\_subscription\] table that’s not mentioned earlier.

</td></tr></tbody>
</table>11. To test your subflow, select **Test**.

    1.  View the test results and system logs for details about any errors.

        To view system logs, navigate to **System Logs** &gt; **System Log** &gt; **All**.

    **Note:** The data stream action to get users should retrieve multiple pages of users successfully. Don't write to the Software Subscriptions \[samp\_sw\_subscription\] table until you verify that the data stream action retrieves all users. To verify, you can make a subflow that consumes the data stream and log the results.

12. After verifying that the subflow is working as expected, select **Publish**.

    **Tip:** You can still edit the subflow after it's published.


## Configure an identifier

Configure an identifier if it doesn't exist to identify an integration.

### Before you begin

Role required: sam\_admin

### Procedure

1.  Create a custom product when your product doesn't exist in the Software Product \[samp\_sw\_product\] table.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_gnp_l4q_xvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Publisher

</td><td>

Publisher of the custom product.

</td></tr><tr><td>

Product

</td><td>

Name of the custom product.

</td></tr><tr><td>

Product type

</td><td>

Product type of the custom software product.

</td></tr><tr><td>

Product classification

</td><td>

Official UNSPSC classification.

</td></tr><tr><td>

Subscription software

</td><td>

Option indicating that your product is a subscription-based product.

</td></tr><tr><td>

Ignore installs

</td><td>

Option indicating that the product type is licensable. This check box is displayed only if you select Product type as Licensable and Subscription software is set to true.

</td></tr><tr><td>

Exclude from content service

</td><td>

Option that indicates that the product will be excluded from the content service.You must not select this check box.

</td></tr><tr><td>

Active

</td><td>

Option indicating that this product is used or not.

</td></tr></tbody>
</table>    3.  Select **Submit**.

2.  Create a custom discovery map by creating a custom entitlement definition from the Discovery maps \[samp\_custom\_sw\_entitlement\_definition\] table.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_xfz_dpq_xvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product

</td><td>

Current software product name. Custom product that you created in [step 1](create-subflow-get-users.md#step1).

</td></tr><tr><td>

Version condition

</td><td>

Condition qualifier for the Version field:-   starts with
-   is
-   is anything
 Default is **is anything**.

</td></tr><tr><td>

Version

</td><td>

Version of the software product. Required if version condition value is starts with or is.

</td></tr><tr><td>

Edition condition

</td><td>

Condition qualifier for the Edition field:-   starts with
-   is
-   is anything
 Default is **is anything**.

</td></tr><tr><td>

Edition

</td><td>

Platform of the software product to use when searching for the normalized discovery model.

</td></tr><tr><td>

Platform

</td><td>

Platform of the software product to use when searching for the normalized discovery model.

</td></tr><tr><td>

Language

</td><td>

Language of the software product to use when searching for the normalized discovery model, which is populated once it has been normalized or added manually.

</td></tr></tbody>
</table>    3.  Select **Submit**.

3.  Create a custom subscription product definition by creating a custom entitlement definition from the Custom Subscription Product Definitions \[samp\_sw\_custom\_subscription\_product\_definition\] table.

    1.  Select **New**.

    2.  On the form, fill in the fields.

<table id="table_gdg_4pq_xvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Identifier

</td><td>

Subscription identifier that is related with the custom product.

</td></tr><tr><td>

Subscription integration

</td><td>

List of SaaS and SSO providers that is mapped to subscription products in the Subscription Product Definition \[samp\_sw\_subscription\_product\_definition\] table. For this scenario, select **Custom Integration**.

</td></tr><tr><td>

Entitlement definition

</td><td>

Custom discovery map that you created in [step 2](create-subflow-get-users.md#step2).

</td></tr><tr><td>

Active

</td><td>

Check box indicating the identifier is used or not.

</td></tr></tbody>
</table>    3.  Select **Submit**.


