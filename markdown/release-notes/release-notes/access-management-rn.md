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

See [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

## Access Management features

-   **[Machine identity access controls](https://www.servicenow.com/docs/access?context=machine-identity-access-controls&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Enforce fine-grained access to data via REST or SOAP endpoints using Machine Identity Access Controls. This feature enables you to define which integrations can access specific data, confirming that the integrations only have access to the resources they need.

-   **[Scripting Governance Tool](https://www.servicenow.com/docs/access?context=scripting-governance&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) tool and role**

    Review and help reduce the number of users with scripting privileges using the Scripting Governance Tool. This tool helps improve platform security with scripting governance based on user role.

    A new deny-by-default behavior is enforced for scripting unless you have the snc\_required\_script\_writer\_permission role. After an upgrade or zBoot, this role is automatically assigned via the Conditional Script Writer group.

-   **[Datatype ACL](https://www.servicenow.com/docs/access?context=datatype-acl&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Simplify and help reduce redundant ACL definitions with Datatype ACLs. Create a single ACL to target all table columns of a specific data type, streamlining access control configurations.


## Activation information

Access Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

