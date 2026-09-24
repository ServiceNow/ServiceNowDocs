---
title: Consumer form
description: The Customer Service Management application uses the Consumer form to record information about an individual business-to-consumer \(B2C\) customer, including contact details, address, preferences, and portal sign-in.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/consumer-form.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Consumer form

The Customer Service Management application uses the Consumer form to record information about an individual business-to-consumer \(B2C\) customer, including contact details, address, preferences, and portal sign-in.

The Consumer form includes the following fields.

|Field|Definition|
|-----|----------|
|Name|The full name of the consumer, assembled from the first, middle, and last name fields. This field is read-only.|
|Prefix|The title that precedes the consumer's name, such as Mr. or Ms.|
|First name|The first name of the consumer.|
|Middle name|The middle name of the consumer.|
|Last name|The last name of the consumer.|
|Suffix|The suffix that follows the consumer's name, such as Jr. or Sr.|
|Mobile phone|The mobile phone number of the consumer.|
|Business phone|The business phone number of the consumer.|
|Home phone|The home phone number of the consumer.|
|Fax|The fax number of the consumer.|
|Number|The identifier automatically generated for the consumer record.|
|Email|The email address of the consumer.|
|Gender|The gender of the consumer.|
|Photo|An image that represents the consumer. Select **Click to add** to upload a photo.|
|Active|Indicates whether the consumer record is active. Inactive consumers don't appear in lists.|

## Primary Address

|Field|Definition|
|-----|----------|
|Street|The street address of the consumer.|
|City|The city of the consumer's address.|
|State / Province|The state or province of the consumer's address.|
|Zip / Postal code|The ZIP or postal code of the consumer's address.|
|Country|The country of the consumer's address.|
|Use same address for|The additional address types that reuse this address: Billing, Shipping, Mailing, and Cloud Operations. Select each type that applies.|

## Preferences

|Field|Definition|
|-----|----------|
|Language|The preferred language for the consumer's communications and self-service experience.|
|Time zone|The time zone used to display dates and times for the consumer. The default is the system time zone.|
|Date format|The format used to display dates for the consumer.|
|Notification|Whether the consumer receives notifications. Select **Enable** to send notifications to the consumer.|
|Time format|The format used to display times for the consumer.|

## Login Details

|Field|Definition|
|-----|----------|
|User|The user record associated with the consumer for signing in to the self-service portal.|
|Active|Indicates whether the associated user account is active and can sign in.|
|Last login time|The date and time when the consumer last signed in. This field is read-only.|
|Failed login attempts|The number of consecutive failed sign-in attempts for the associated user account.|

## Notes

|Field|Definition|
|-----|----------|
|Notes|Additional information about the consumer.|

## Customer data model fields

**Note:** These fields were added to the Consumer table \(`csm_consumer`\) in the Brazil release. They appear on the Consumer form after an administrator adds them to the form view.

|Field|Definition|
|-----|----------|
|Consumer stage|The stage of the consumer in the customer lifecycle. The available values are configured for your instance.|
|Consumer status|The consumer's current operational status, such as Onboarding. The available statuses depend on the value selected in the **Consumer stage** field.|
|Relationship tier|The tier that reflects the consumer's overall value or engagement. The available values are configured for your instance.|
|Customer since|The date the consumer became a customer.|
|External ID|The identifier for this consumer in an external system, such as a CRM, ERP, or identity provider. Use this field to correlate the consumer across systems. Values aren't required to be unique.|

**Related topics**  


[Configure consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-csm-consumers.md)

[Create consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/import-create-csm-consumers.md)

