---
title: Account form
description: The Customer Service Management application uses the Account form to store customer account information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-service-account-form.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Account form

The Customer Service Management application uses the Account form to store customer account information.

For information about creating a customer account, see [Configure accounts and contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-csm-accounts-contacts.md).

The Account form includes the following fields.

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

The parent account for this account. Use this field to create an [Account hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/c_AccountHierarchy.md).

</td></tr><tr><td>

Registration Code

</td><td>

A unique code for this account. The customer administrator can provide this code to customers for use when requesting a login on the customer portal. The registration code provides a method for validating the customer and the company before the login request is granted. Enter an alphanumeric code in this field or select the Generate Code icon to generate a unique code.

 For more information about generating unique account registration codes, see the [Account Registration code generation in Customer Service \[KB0753505\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0753505) article in the HI Knowledge Base.

</td></tr><tr><td>

Customer

</td><td>

Denotes this account as a customer account. **Note:** If you're creating a customer account, this field is enabled by default.

</td></tr><tr><td>

Partner

</td><td>

Denotes this account as a partner account. A partner can report and manage cases on behalf of customers. A partner can also be a customer.

 **Note:** If you're creating a partner account, this field is enabled by default.

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

The ZIP code or postal code for the company.

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

This field stores a unique value for each account. The value is determined by the last used value, which is stored in the **com.snc.cs\_base.last.generated.code.tree.path** system property. For more information, see [Properties installed with Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/r_PropInstallWcustServ.md).**Note:** If this property is reset to the value that's already being used, the system attempts to create accounts with account codes that are already in use, which can result in an invalid insert.

</td></tr><tr><td>

DUNS Number

</td><td>

DUNS stands for Data Universal Numbering System. It is a globally recognized unique identifier for businesses, widely adopted by governments and organizations around the world.

</td></tr><tr><td>

Active

</td><td>

This field indicates whether a customer account is active or inactive.

</td></tr></tbody>
</table>## Details

|Field|Definition|
|-----|----------|
|Industry|The industry in which the company operates.|
|Legal entity name|The registered legal name of the company.|
|Business structure|The legal structure of the business, such as a corporation or a partnership.|
|Assumed name|The name under which the company does business when it differs from the legal entity name, also known as a "doing business as" \(DBA\) name.|
|Date of Incorporation|The date the company was incorporated.|
|Trademark|An image of the company's trademark. Select **Click to add** to upload an image.|
|Tax ID|The tax identification number for the company.|

## Contact Information

|Field|Definition|
|-----|----------|
|Email|The primary email address for the company.|

## Customer data model fields

**Note:** These fields were added to the Account table \(`customer_account`\) in the Brazil release. They appear on the Account form after an administrator adds them to the form view.

|Field|Definition|
|-----|----------|
|Account stage|The stage of the account in the customer lifecycle. Available values are Suspect, Prospect, Customer, and Former customer.|
|Account status|The account's current operational status, such as Onboarding. The available statuses depend on the value selected in the **Account stage** field.|
|Customer since|The date the account became a customer.|
|Relationship tier|The tier that classifies the depth and value of the relationship with the customer. Available values are Standard, Preferred, Premium, Gold, Platinum, Elite, and Strategic.|
|Market segment|The segment that classifies the account by size and position in the market, based on characteristics such as employee count, company revenue, and industry.|
|Total ACV|The annual contract value \(ACV\) generated from the customer's agreement, shown as a currency amount.|
|External ID|The identifier for this account in an external system, such as a CRM, ERP, or identity provider. Use this field to correlate the account across systems. Values aren't required to be unique.|

**Related topics**  


[Configure accounts and contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-csm-accounts-contacts.md)

[Create customer accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/import-create-csm-accounts.md)

