---
title: Restrict performance monitoring access \[Updated in Security Center 1.3\]
description: Use the glide.security.diag\_txns\_acl property to control stats.do, threads.do, thread\_pool\_stats, and replication.do access from an unauthenticated connection.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Restrict performance monitoring access \[Updated in Security Center 1.3\]

Use the **glide.security.diag\_txns\_acl** property to control stats.do, threads.do, thread\_pool\_stats, and replication.do access from an unauthenticated connection.

When you set this property to **true**, the **glide.security.diag\_txns\_acl** property only allows access to the following by the administrator account:

-   https://&lt;instancename&gt;.service-now.com/stats.do
-   https://&lt;instancename&gt;.service-now.com/threads.do
-   https://&lt;instancename&gt;.service-now.com/replication.do
-   https://&lt;instancename&gt;.service-now.com/thread\_pool\_stats.do

Without enabling this setting, it is still possible to access these resources from an unauthenticated connection.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.security.diag\_txns\_acl**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Configuration](sc-configuration.md)|
|Purpose|Restrict the access to configuration pages to administrator account only|
|Recommended value|true|
|Default value|true|
|Security risk rating|5.3|
|Functional Impact|This remediation enforces only administrator account to get access to the application sensitive data for logging and troubleshooting purposes.|
|Security risk|\(Moderate\) Sensitive data such as server details, threads, and processes executed on the server should never be visible or accessible to the end user without appropriate privileges.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Configuration](sc-configuration.md)

