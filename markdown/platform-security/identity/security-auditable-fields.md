---
title: Security Auditable Fields
description: Displays table and field level details that will be audited in the ServiceNow instance.
locale: en-US
release: xanadu
product: Identity
classification: identity
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Identity and Access Audit, Identity]
---

# Security Auditable Fields

Displays table and field level details that will be audited in the ServiceNow® instance.

Security Auditable Fields displays the details of tables and fields that will be audited in the ServiceNow instance.

To access the Security Auditable Fields page, navigate to **All** &gt; **System Security** &gt; **Identity and Access Audit** &gt; **Configure Tables &amp; Fields**. The Security Auditable Fields page is displayed with the following information.

|Column Name|Description|
|-----------|-----------|
|Table to Audit|Details of the table that is audited.|
|Audit Storage Destination|Details of the destination where the audit details are stored.|
|Field List|Auditing will be done for fields specified in the list.|
|Create|Audit the changes that are related to Create operation.|
|Update|Audit the changes that are related to Update operation.|
|Delete|Audit the changes that are related to Delete operation.|
|Active|Audit only if the configuration for the table is active.|

![Security Auditable Fields](../images/security-auditable-fields.png)

The following tables can be audited using the Identity and Access Audit​:

-   Group \[sys\_user\_group\]​
-   Role \[sys\_user\_role\]​
-   Access Control \[sys\_security\_acl\]​
-   User \[sys\_user\]​
-   Group Role \[sys\_group\_has\_role\]​
-   User Role \[sys\_user\_has\_role\]​
-   Access Roles \[sys\_security\_acl\_role\]​
-   Contained Role \[sys\_user\_role\_contains\]​
-   Group Member \[sys\_user\_grmember\]​

