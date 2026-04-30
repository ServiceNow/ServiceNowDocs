---
title: Properties installed with Customer Service Management
description: Properties are added with the activation of the Customer Service Management application.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Components installed with Customer Service Management, Reference, Customer Service Management]
---

# Properties installed with Customer Service Management

Properties are added with the activation of the Customer Service Management application.

To open the System Property \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter. You can narrow the list results by using the **Application** field.

You can also navigate to **Customer Service** &gt; **Administration** &gt; **Properties** to view a list of the most frequently used properties that you can configure for Customer Service Management.

The following table lists the properties that are used for Customer Service Management.

<table id="table_jzs_2kx_kt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.cs.email.case\_queue\_address

</td><td>

Email case queue address.-   **Type**: string
-   **Default value**: none
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

glide.cs.email.new\_case\_prefix

</td><td>

Email subject prefix format for new case. -   **Type**: string
-   **Default value**: Case:
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.email.create\_case\_for\_non\_matched\_user

</td><td>

Create case for non-matched user.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

glide.cs.company\_name

</td><td>

Your company name.-   **Type**: string
-   **Default value**: none
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.ui.activity.email\_roles

</td><td>

Roles that can view the mail in the Activity formatter when including "Sent/Received Emails.-   **Type**: string
-   **Default value**: itil, sn\_customerservice\_agent, sn\_esm\_location\_agent, sn\_esm\_agent, sn\_csm\_ocs.ext\_agent, sn\_customerservice.case\_task\_agent, sn\_customerservice.relationship\_agent, sn\_customerservice.case\_contributor\_creator
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.ui.sn\_customerservice\_case\_activity.fields

</td><td>

Case activity formatter fields.-   **Type**: string
-   **Default value**: assigned\_to,asset, product, state, priority, short\_description, comments, entitlement, contract, \*Email\*,work\_notes
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.FTS\_flag\_enabled

</td><td>

Enable the follow the sun flag on the Customer Service Case form.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

sn\_customerservice.glide.script.block.client.globals

</td><td>

-   **Type**: true \| false
-   **Default value**:false
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.shn\_asset

</td><td>

Special Handling Notes for assets.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Special Handling Notes** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.shn\_contact

</td><td>

Special Handling Notes for contacts.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Special Handling Notes** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.shn\_product

</td><td>

Special Handling Notes for products.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Special Handling Notes** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.shn\_account

</td><td>

Special Handling Notes for accounts.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Special Handling Notes** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.shn\_case

</td><td>

Special Handling Notes for cases.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Special Handling Notes** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.portal.chat\_queue

</td><td>

-   **Type**: string
-   **Default value**: none
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

csm.captcha.google.enabled

</td><td>

Enable the Google Captcha tool on the customer portal self-service portal self-registration form.-   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.use\_asset\_contact\_relationship

</td><td>

Restrict assets that are based on the contacts assigned to the assets.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.account\_relationship\_access\_roles

</td><td>

Roles that need to be shown in the reference qualifier for the Account Relationship Access table \[sn\_customerservice\_account\_relationship\_access\]. -   **Type**: string
-   **Default value**: none
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.contact\_role\_assignment

</td><td>

External roles that can be assigned to contacts from the Customer Service Portal. The roles stored in this property are displayed in the **Available** column on the Edit Role pop-up window. -   **Type**: string
-   **Default value**: sn\_customerservice.partner\_admin, sn\_customerservice.partner,sn\_customerservice.customer\_admin, sn\_customerservice.customer
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.registration\_workflow\_id

</td><td>

Default registration workflow sys\_id.-   **Type**: string
-   **Default value**: 9b6cf2dac31302003a657bfaa2d3aee8
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.consumer\_max\_products

</td><td>

Maximum registered products per consumer. -   **Type**: integer
-   **Default value**: 25
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

com.snc.cs\_base.last.generated.code.tree.path

</td><td>

Property that gets created by the system when the first customer\_account record is inserted into an instance. It stores the **Account Code** value for the most recently created customer account in the Account \[customer\_account\] table. When a new customer account record is created, the system uses this property to determine a unique account code value for the account. The property is then updated with this latest assigned value so that the next account code value can be set as a unique value for the next account record insert. See [Set the account code property](set-csm-account-code-property.md) for more details.

 -   **Type**: string
-   **Default value**: none
-   **Location**: System Property \[sys\_properties\] table

**Note:** If this property is reset to the original value, the system attempts to create new accounts with account codes that are already in use, which can result in an invalid insert.

</td></tr><tr><td>

sn\_customerservice.enable\_knowledge\_kcs

</td><td>

Knowledge Centered Services \(KCS\) for Customer Services Management.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

skills\_management.migration

</td><td>

List of task tables to migrate to the Task Skills \[task\_m2m\_skill\] table when an administrator runs the **Migrate Skills to Task Skill M2M** script. -   **Type**: choice list
-   **Default value**: wm\_task,customerservice\_case,wm\_order
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.rest.api.case\_sla\_async

</td><td>

Enable asynchronous processing of SLAs while creating a case using a REST API.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

com.snc.skills\_management.task\_skill\_migrated\_tables

</td><td>

List of tables where the **Skills** field has already been migrated to the Task Skills \[task\_m2m\_skill\] table. If the table name is listed in this property, the data has been migrated and will not be migrated again. -   **Type**: choice list
-   **Default value**: none
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.case\_fields\_to\_sync

</td><td>

Comma-separated list of fields that synchronize from parent case to child cases.-   **Type**: string
-   **Default value**: priority,state,comments,work\_notes, close\_notes, resolution\_code
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.parent\_child\_case\_sync

</td><td>

Synchronize fields from parent to child cases.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.parent\_child\_case\_sla\_async

</td><td>

Processes SLA asynchronously during parent to child case creation and synchronization.-   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.ui.sn\_customerservice\_escalation\_activity.fields

</td><td>

Escalation activity formatter fields.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.kcs.enable\_template\_on\_case\_workspace

</td><td>

Enables creation of knowledge articles by using a knowledge article template from a customer service case in Agent Workspace.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.case.autoresponder.enable

</td><td>

Enables sending content as recommendations for closing a case by using the Auto-Responder feature.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.case.autoresponder.customportal

</td><td>

Custom portal URL that contains the knowledge article parameter such as sys\_kb\_id or kb\_number. Example: https://&lt;instance-name&gt;.service-now.com/csm?id=kb\_article\_view&amp;sys\_kb\_id=\{sys\_kb\_id\}

 -   **Type**: string
-   **Default value**: none
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_customerservice.contact\_relationship.restrict\_within\_account\_hierarchy

</td><td>

Create a contact relationship with contacts outside the account hierarchy.When set to **false**, users are allowed to create contact relationships with any account. When set to **true**, only contacts within the account hierarchy will be shown.

 -   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_bus\_loc.int\_bus\_loc.onboard\_location\_manager\_as\_contributor

</td><td>

Assign the sn\_customerservice.svc\_location\_manager\_contributor role to the internal business location managers when the system property is set to **true**. When set to **false**, the internal business location managers are assigned the sn\_customerservice.svc\_location\_manager role.-   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

enable\_account\_address\_sharing

</td><td>

Enable an existing address to be associated with multiple accounts. The associations are present in the account\_address\_relationship table. Setting the property back to false once set to true leads to inappropriate behavior for account address data.-   **Type**: true\| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.create\_case.description\_enable\_html\_editor

</td><td>

Enable the flag to add description by using the HTML editor on the Create Case form page.-   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_customerservice.emails.customportal

</td><td>

Base URL for custom portals.-   **Type**: string
-   **Default value**: none
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_query\_rules.number\_of\_nq\_ops\_zing\_search\_supports

</td><td>

Defines the number of query rules that must be applied to filter the data.-   **Type**: string
-   **Default value**: 10

</td></tr><tr><td>

sn\_customerservice.consumer\_max\_new\_cases\_daily

</td><td>

Defines the maximum number of new cases that a consumer can create in a day.-   **Type**: integer
-   **Default value**: 10
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

**Note:** This restriction only applies to an external unified consumer.

</td></tr><tr><td>

sn\_customerservice.consumer\_max\_comments\_per\_case\_daily

</td><td>

Defines the maximum number of comments that a consumer can add for a case in a day.-   **Type**: integer
-   **Default value**: 25
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

**Note:** This restriction only applies to an external unified consumer.

</td></tr><tr><td>

sn\_customerservice.consumer\_max\_attachments\_per\_record

</td><td>

Defines the maximum number of attachments that a consumer can attach to a record.-   **Type**: integer
-   **Default value**: 5
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

**Note:** This restriction only applies to an external unified consumer.

</td></tr><tr><td>

sn\_cs\_queryrules.use\_query\_rules

</td><td>

Rules or filters from the sn\_query\_rule table to determine read access to customer service management-related tables for the logged-in users through query business rules and READ ACLs when the system property is set to **True**. When set to **False**, rules or filters from the `CSMQueryBRUtilOOBConstants` and its extensions are used.

 -   **Type**: true \| false
-   **Default value**: true
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td id="advanced-entitlements">

sn\_customerservice.advanced\_entitlements

</td><td>

This property displays or hides the Case Entitlements related list for case records.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: **Customer Service** &gt; **Administration** &gt; **Properties**

If **true**:

-   The Case Entitlements related list is visible on the Case form.
-   The **Entitlement** field on the Case form is hidden.

If **false**:

-   The **Entitlement** field is visible on the Case form.
-   The Case Entitlements related list is hidden on the Case form.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Customer Service Management](r_InstalledWithCustomerService.md)

