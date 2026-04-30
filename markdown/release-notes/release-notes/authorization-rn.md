---
title: Access Management release notes
description: The ServiceNow Access Management includes access control lists \(ACLs\), security attributes, contextual security manager, data filtration, and many more controls. These tools provide finer control and improved security for managing data access. Access Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Access Management release notes

The ServiceNow® Access Management includes access control lists \(ACLs\), security attributes, contextual security manager, data filtration, and many more controls. These tools provide finer control and improved security for managing data access. Access Management was enhanced and updated in the Xanadu release.

## Access Management highlights for the Xanadu release

-   Fine-tune your access control with the new Deny-Unless ACL and query operators.
-   Enhance ACL security with a new default denial behavior.
-   Identify and fix empty or misconfigured ACLs with new ACL creation rules.

See [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for more information.

## Changed in this release

-   **[Deny-Unless condition for ACLs](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    A new decision type field helps administrators define the conditions that give or deny users access to data. It enables more granular decision-making while defining the right access strategy on the platform.

-   **[Enhanced ACL Security](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    If an ACL is misconfigured or empty, you can deny access to data by default, enhancing the overall security of the platform.

-   **[ACL Query Behavior](https://www.servicenow.com/docs/access?context=r_SecurityJumpStartACLRules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Fine-tune your access control by dictating rules for querying data with the introduction of new operators: query match and query range.

-   **&gt;[Explicit Roles behavior adjustment](https://www.servicenow.com/docs/access?context=explicit-roles&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    When the system property `glide.security.explicit_roles.do_not_fix` is true, the **snc\_internal** role is no longer added in memory or to the User Roles \[sys\_user\_has\_role\] table.


## Activation information

Access Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

