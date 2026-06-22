---
title: Minimize SMTP Recipient Quantity \[Updated in Security Center 1.3\]
description: The glide.email.smtp.max\_recipients specifies the maximum number of recipients the instance can list in the To: line for a single email notification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-max-smtp-recipients.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Business Logic, Hardening settings, Platform Security]
---

# Minimize SMTP Recipient Quantity \[Updated in Security Center 1.3\]

The **glide.email.smtp.max\_recipients** specifies the maximum number of recipients the instance can list in the **To:** line for a single email notification.

Set **glide.email.smtp.max\_recipients** to the recommended value of **100 or less**. Notifications that would exceed this limit instead create duplicate email notifications addressed to a subset of the recipient list. Each email notification has the same maximum number of recipients.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.email.smtp.max\_recipients**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Business Logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-business-logic.md)|
|Purpose|If this property is set to an insecure value above the default value of 100, then its possible a denial of service could happen on the instance.|
|Recommended value|100|
|Default value|100|
|Configuration type|Integer|
|Security risk|\(Moderate\) Notifications that would exceed this limit instead create duplicate email notifications addressed to a subset of the recipient list.|
|Security risk rating|4.9|

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Parent Topic:**[Business Logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-business-logic.md)

