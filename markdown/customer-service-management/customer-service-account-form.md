---
title: Account form
description: The Customer Service Management application uses the Account form to store customer account information.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Account form

The Customer Service Management application uses the Account form to store customer account information.

For information about creating a customer account, see [Configure accounts and contacts](../task/configure-csm-accounts-contacts.md).

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the company.

</td></tr><tr><td>

Number

</td><td>

The automatically generated account number for this customer.

</td></tr><tr><td>

Primary Contact

</td><td>

The name of a user who is the main contact for this company.

</td></tr><tr><td>

Parent Account

</td><td>

The parent account for this account. Use this field to create an [Account hierarchy](../concept/c_AccountHierarchy.md).

</td></tr><tr><td>

Registration Code

</td><td>

A unique code for this account. The customer administrator can provide this code to customers for use when requesting a login on the customer portal. The registration code provides a method for validating the customer and the company before the login request is granted. Enter an alphanumeric code in this field or click the Generate Code icon to generate a unique code.

 For more information about generating unique account registration codes, see the [Account Registration code generation in Customer Service \[KB0753505\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0753505) article in the HI Knowledge Base.

</td></tr><tr><td>

Customer

</td><td>

Denotes this account as a customer account. **Note:** If you are creating a customer account, this field is enabled by default.

</td></tr><tr><td>

Partner

</td><td>

Denotes this account as a partner account. A partner can report and manage cases on behalf of customers. A partner can also be a customer.

 **Note:** If you are creating a partner account, this field is enabled by default.

</td></tr><tr><td>

Website

</td><td>

The web address for the company.

</td></tr><tr><td>

Phone

</td><td>

The phone number for the company.

</td></tr><tr><td>

Street

</td><td>

The street address of the company.

</td></tr><tr><td>

City

</td><td>

The city in which the company is located.

</td></tr><tr><td>

State/Province

</td><td>

The state or province in which the company is located.

</td></tr><tr><td>

Zip/Postal code

</td><td>

The zip code or postal code for the company.

</td></tr><tr><td>

Country

</td><td>

The country in which the company is located.

</td></tr><tr><td>

Notes

</td><td>

Any additional information about the company.

</td></tr><tr><td>

Account Code

</td><td>

This field stores a unique value for each account. The value is determined by the last used value, which is stored in the **com.snc.cs\_base.last.generated.code.tree.path** system property. For more information, see [Properties installed with Customer Service Management](r_PropInstallWcustServ.md).**Note:** If this property is reset to the original value, the system attempts to create new accounts with account codes that are already in use, which can result in an invalid insert.

</td></tr></tbody>
</table>