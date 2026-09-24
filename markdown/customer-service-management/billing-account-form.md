---
title: Billing Account form
description: The Customer Service Management application uses the Billing Account form to define customer billing arrangements, payment responsibility, and billing schedules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/billing-account-form.html
release: brazil
topic_type: reference
last_updated: "2026-09-18"
reading_time_minutes: 2
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Billing Account form

The Customer Service Management application uses the Billing Account form to define customer billing arrangements, payment responsibility, and billing schedules.

The Billing Account form includes the following fields.

<table id="table_billing_account_form_fields"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the billing account.

</td></tr><tr><td>

Number

</td><td>

Internal unique number identifying the billing account.

</td></tr><tr><td>

Parent billing account

</td><td>

References the parent billing account.

</td></tr><tr><td>

Account

</td><td>

Customer account to which this billing account belongs.In the default view, this field appears when the billing account type is Customer account.

</td></tr><tr><td>

Contact

</td><td>

Customer contact to which this billing account belongs.In the default view, this field appears when the billing account type is Customer account.

</td></tr><tr><td>

Consumer

</td><td>

Consumer to which this billing account belongs.In the default view, this field appears when the billing account type is Consumer.

</td></tr><tr><td>

Paying party

</td><td>

The party responsible for paying the charges on this billing account.

</td></tr><tr><td>

Paying billing account

</td><td>

Billing account that pays the charges. **Note:** This field is mandatory unless Paying party is None, and it isn't available when Paying party is None. When Paying party is Self, the field is set to the current billing account and is read-only. When Paying party is Parent or Designated, you select the account. Changing Paying party clears this field

.

</td></tr><tr><td>

Description

</td><td>

Description of the billing account.

</td></tr><tr><td>

Billing account type

</td><td>

Organization or user type associated with this billing account.When you create a billing account from a customer record, this field is set automatically from the source customer: Customer account for an account, or Consumer for a consumer. You can change the value before you save the record.

</td></tr><tr><td>

Status

</td><td>

Indicates the current state of the billing account.

</td></tr><tr><td>

Start date

</td><td>

Date when the billing account is set to active.

</td></tr><tr><td>

End date

</td><td>

Date when the billing account is closed or terminated.

</td></tr><tr><td>

Currency

</td><td>

Currency used for transactions in this billing account.

</td></tr><tr><td>

Billing schedule

</td><td>

The schedule that determines the billing cycle for the billing account.

</td></tr><tr><td>

Active

</td><td>

Status of the configuration. By using this functionality, you can enable or disable this configuration.

</td></tr></tbody>
</table>## Additional fields

**Note:** The following fields exist on the Billing Account table in the Billing Account Core application but aren't on the form by default. As an administrator, you can add them to the form view as needed.

|Field|Definition|
|-----|----------|
|Billing account code|A unique code for the billing account, generated automatically when the record is created.|
|External ID|The identifier for this billing account in an external system, such as a CRM, ERP, or identity provider. Use this field to correlate the billing account across systems. Values aren't required to be unique.|
|User|The user associated with the billing account.|
|Company|The company associated with the billing account.|
|Billing account path|The path that represents the billing account's position in the billing account hierarchy. This field is maintained by the system.|

**Related topics**  


[Billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configuring-billing-accounts.md)

[Install billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/install-billing-account.md)

