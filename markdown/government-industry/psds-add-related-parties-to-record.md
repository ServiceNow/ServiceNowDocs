---
title: Configure related parties for Items Received
description: Add related parties to an item received in the Public Sector Digital Services application so that the contacts, businesses, constituents, or agencies can get the correct access level to perform the actions that they need for a case.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User management, Set up your environment, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure related parties for Items Received

Add related parties to an item received in the Public Sector Digital Services application so that the contacts, businesses, constituents, or agencies can get the correct access level to perform the actions that they need for a case.

## Before you begin

Role required: admin, sn\_gsm.constituent, sn\_gsm.constituent\_agent, sn\_gsm.business\_agent, sn\_gsm.agency\_agent, sn\_gsm.relationship\_agent, or sn\_gsm.service\_manager

## Procedure

1.  Navigate to the CSM Configurable Workspace and select the Lists icon ![Lists icon.](../image/lists-icon.png) in the sidebar.

2.  Navigate to **Item Received** &gt; **All**.

3.  Select the record that you want to add the related parties to.

4.  From the Related Parties related list, select **New**.

5.  On the form, fill in the fields.

<table id="table_esz_qdw_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Related party type. The related party type can be a contact, consumer, or a contributor user. You can select from the list of related party configurations for the cases that are provided with the base system:-   Authorized Business
-   Authorized Contact
-   Authorized Constituent
-   Authorized Household
-   Authorized Agency
-   Authorized User
-   Listed Constituent
-   Listed Agency


</td></tr><tr><td>

Case

</td><td>

Auto-generated case number.

</td></tr><tr><td>

Business, constituent, household, or user

</td><td>

Contact responsible for the case.

</td></tr><tr><td>

Responsibility

</td><td>

Access level to the case information.When you select the related party type, the associated responsibility gets added by default. If the related party type is changed, the responsibility that corresponds with the related party type gets updated accordingly.

 **Note:** If the related party type is selected but the responsibility field isn’t automatically filled in, your contacts don't have access to the sold product \(service received\) and associated case.

</td></tr></tbody>
</table>6.  Select **Submit**.

    The related parties are added to the case.


## Result

After a related party is added to the case as an authorized representative with a functional role, the related party can perform the following actions:

-   Close a case.
-   Create a case for service received \(sold product\).
-   Receive notifications on case updates.
-   Update the customer-visible case tasks.
-   Add additional comments and attachments.
-   Accept or reject a solution.

