---
title: Create a Coupa integration profile
description: Create a Coupa integration profile to verify the status of the procurement-scheduled jobs, entitlements, and entitlement import errors created through this profile.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrating with Coupa, Integrating with external procurement applications, Procurement, IT Asset Management]
---

# Create a Coupa integration profile

Create a Coupa integration profile to verify the status of the procurement-scheduled jobs, entitlements, and entitlement import errors created through this profile.

## Before you begin

Role required: sam\_admin

Create an OAuth 2.0 connection with Coupa to get the Client ID and Client Secret. For more information, see [OAuth 2.0 Getting Started with Coupa API](https://compass.coupa.com/en-us/products/core-platform/integration-playbooks-and-resources/integration-knowledge-articles/oauth-2.0-getting-started-with-coupa-api). Save the Client ID and Client Secret in a secure location for later use.

You must set the following scopes while creating an OAuth 2.0 connection with Coupa.

-   core.approval.configuration.read
-   core.approval.read
-   core.approval.write
-   core.catalog.read
-   core.common.read
-   core.contract.read
-   core.contract.write
-   core.inventory.adjustment.read
-   core.inventory.adjustment.write
-   core.inventory.asn.read
-   core.inventory.common.write
-   core.inventory.consumption.read
-   core.inventory.consumption.write
-   core.inventory.receiving.read
-   core.inventory.receiving.write
-   core.inventory.return\_to\_supplier.read
-   core.inventory.transfer.read
-   core.inventory.transfer.write
-   core.invoice.delete
-   core.invoice.read
-   core.invoice.write
-   core.item.read
-   core.item.write
-   core.legal\_entity.read
-   core.purchase\_order.read
-   core.purchase\_order.write
-   core.requisition.read
-   core.requisition.write
-   core.sourcing.pending\_supplier.read
-   core.sourcing.pending\_supplier.write
-   core.sourcing.read
-   core.sourcing.response.award.write
-   core.sourcing.response.read
-   core.sourcing.response.write
-   core.sourcing.write
-   core.supplier.read
-   core.supplier.write
-   core.user.read
-   core.user.write

**Note:** If these scopes aren't associated with the Client ID and Client Secret, the OAuth token flow fails on ServiceNow.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Purchasing** &gt; **Procurement integrations**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_oxb_lg4_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the procurement integration profile. For example, `Coupa integration`.

</td></tr><tr><td>

Connection &amp; Credentials

</td><td>

Connection and credential alias for Coupa. This field gets automatically populated to **sn\_coupa\_spoke.Coupa\_OAuth**.

</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. Select **Coupa integration**.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you haven’t published the integration profile, this field is automatically set to Draft.
-   If you’ve already published the integration profile, this field is automatically set to Published.


</td></tr><tr><td>

Active

</td><td>

This field is visible and set to true only when the integration profile is published.

 If you set this field to false, the associated requisitions with this integration profile aren’t created and tracked.

</td></tr></tbody>
</table>4.  Select **Save**.

5.  Select the Preview icon ![Preview icon](../../software-asset-management2/image/preview-icon.png) next to the Connection &amp; Credentials field.

    You get redirected to the Connection &amp; Credential Aliases form.

6.  Select **Create New Connection &amp; Credential** in the Related Links section to create connection credential.

7.  In the dialog box, fill in the fields.

<table id="table_tg3_2sh_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \(Connection\)

</td><td>

Name to identify the connection uniquely. For example, `Coupa OAuth connnection`.

</td></tr><tr><td>

Connection URL

</td><td>

URL to make a connection to Coupa. Use the `https://<coupa-instance-url>` format.-   For customer instances, use the `https://{organization_name}.coupahost.com` format.
-   For partner and demo instances, use the `https://{organization_name}.coupacloud.com` format.


</td></tr><tr><td>

Name \(Credential\)

</td><td>

Name to identify the credential uniquely. For example, `Coupa OAuth credential`.

</td></tr><tr><td>

Token URL

</td><td>

URL used to generate OAuth token. Use the `https://<coupa-instance-url>/oauth2/token` format.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Identifier \(Client ID\) generated in Coupa.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Secret \(Client Secret\) generated in Coupa.

</td></tr></tbody>
</table>8.  Select **Create and Get OAuth Token**.

    Your ServiceNow instance creates an OAuth for Coupa and then automatically returns you to the Integration Profile form.

9.  Create a child alias that can uniquely identify the connection and credentials for this integration profile.

    The first Coupa integration profile that you create uses the default \(parent\) connection and credential alias for Coupa. Each additional Coupa integration profile that you create needs a unique child alias that helps differentiate the connection and credentials between each integration profile.

    1.  On the Connection &amp; Credential Aliases form, select the link under **Child Aliases &gt; Parentalias=\*\*\*** to add child aliases.

    2.  Select **New**.

    3.  Enter a name for the child alias in the Name field.

    4.  Right-click the form header and then select **Save**.

    5.  After the form reloads, select the **Create New Connection &amp; Credential** related link.

    6.  Repeat steps 7 and 8.

    7.  In the Connection &amp; Credential field of the Integration Profile form, select the lookup icon to locate and select the child alias that you created.

        Selecting the child alias associates the alias with the integration profile. Your ServiceNow instance uses this alias to identify the connection and credentials for this integration profile.

10. Select **Publish**.


## Result

After you publish the integration profile, the scheduled job **ITAM - Sync Coupa purchase orders** runs daily and fetches the status of the already created requisitions.

**Note:** If you haven't created any requisition, the scheduled job doesn't run.

You can view this information by clicking the **Procurement Integration Jobs** tab.

## What to do next

Verify if the scheduled job **ITAM - Sync Coupa purchase orders** has run successfully by selecting the **Integration Scheduled Job Results** tab. If the job has failed, you can view the list of errors by following these steps:

1.  On the Procurement integration profile form, select the **Procurement Integration Job Log** related list.
2.  Open the job log record where the displayed status shows as failed.
3.  Select the related list **Asset Job Log Details** to find out the reason for the job failure.

Create software requisitions directly on Coupa through the ServiceNow Procurement application to purchase software.

If you want to delete the Coupa integration profile, see [Deleting an external procurement application integration profile](../concept/delete-ext-profile.md).

