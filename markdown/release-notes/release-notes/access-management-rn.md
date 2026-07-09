---
title: Access Management release notes
description: The ServiceNow Access Management application provides robust tools to manage security data on the ServiceNow AI Platform. Access Management includes many controls, such as access control lists \(ACLs\), security attributes, contextual security manager, and data filtration. These controls provide granular control and help improve security for managing data access. Access Management is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Access Management release notes

The ServiceNow® Access Management application provides robust tools to manage security data on the ServiceNow AI Platform. Access Management includes many controls, such as access control lists \(ACLs\), security attributes, contextual security manager, and data filtration. These controls provide granular control and help improve security for managing data access. Access Management is a new application in the Zurich release.

## Access Management highlights for the Zurich release

-   Enforce access to data via REST or SOAP endpoints using the Machine Identity Access Controls, which helps improve security, governance, and auditability.
-   Target all table columns of a given data type with a single ACL using Datatype ACLs.
-   Govern scripting permissions with the Scripting Governance tool, a new base system deny-by-default behavior.

See [Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/access-control-rules.md) for more information.

## Access Management features

-   **[Machine identity access controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/machine-identity-access-controls.md)**

    Enforce fine-grained access to data via REST or SOAP endpoints using Machine Identity Access Controls. This feature enables you to define which integrations can access specific data, confirming that the integrations only have access to the resources they need.

-   **[Scripting Governance Tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/scripting-governance.md) tool and role**

    Review and help reduce the number of users with scripting privileges using the Scripting Governance Tool. This tool helps improve platform security with scripting governance based on user role.

    A new deny-by-default behavior is enforced for scripting unless you have the snc\_required\_script\_writer\_permission role. After an upgrade or zBoot, this role is automatically assigned via the Conditional Script Writer group.

-   **[Datatype ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/datatype-acl.md)**

    Simplify and help reduce redundant ACL definitions with Datatype ACLs. Create a single ACL to target all table columns of a specific data type, streamlining access control configurations.


## Activation information

Access Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-security-rn-landing.md)

