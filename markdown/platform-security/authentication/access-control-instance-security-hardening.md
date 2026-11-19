---
title: Access control \(instance security hardening\)
description: Access controls determine whether access to a particular resource should be granted or denied. It only allows access to resources to those users permitted to use them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/access-control-instance-security-hardening.html
release: australia
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [REST API Auth Scope, REST API access policies, API access policy, Authentication, Access Management]
---

# Access control \(instance security hardening\)

Access controls determine whether access to a particular resource should be granted or denied. It only allows access to resources to those users permitted to use them.

Authorization is not equivalent to authentication, as these terms and their definitions are frequently confused.

-   Authentication is providing and validating identity.
-   Authorization includes execution rules that determine what functionality and data the user \(or principal\) can access, ensuring the proper allocation of access rights after authentication is successful.

Authorization is a process that comes after a successful authentication. You can configure security properties that designate if, after determining that a user holds valid credentials associated with a well-defined set of roles and privileges, resource authorization occurs.

The following are some security controls that an administrator can configure to restrict unauthorized access to sensitive entities within the ServiceNow AI Platform.

-   [Access Control Lists \(ACLs\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/access-control/access-control-rules.md)
-   [Configure an ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/access-control/t_CreateAnACLRule.md)
-   [ServiceNow access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/c_SNCAccessControl.md)

