---
title: Process administration
description: Process administration allows administrators to set domain-specific policies.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setup and administration, Domain separation for service providers, Access Management]
---

# Process administration

Process administration allows administrators to set domain-specific policies.

The policies set lower in the domain hierarchy override policies set higher in the domain hierarchy. While in a domain, administrators can set domain-specific versions of these global policies and settings:

-   Client scripts
-   System policies
-   Application and module names
-   Application roles
-   Module filters

**Warning:** All users with the admin role have special access to all system features, functions, and data because administrators can override ACL rules and pass all role checks. Grant this privilege carefully.

When users have the **admin** role, then all policies in the instance are available to them regardless of the assigned domain. They can enter a specific domain, and then only policies in that domain or higher are visible and processed during a relevant transaction. When an administrator modifies a policy that is in a higher domain or the global domain, the system automatically creates a new record for that administrator's current domain. It does not modify the original policy, application, or module record. This new record overrides the original.

To make changes to a policy in a lower-level domain, go into that domain and modify the policy. This approach creates the policy record in your domain that overrides the original, higher-level policy record.

Do not change the higher-level policy and then change the **Domain** field on that policy. This approach does not create a policy record in your lower-level domain, nor does it keep the policy record for the higher-level domain.

The **sys\_overrides** field indicates that a policy, application, or module at a lower level in the hierarchy overrides a record at a higher level. The system automatically sets this field when an administrator attempts to modify a policy, application, or module that belongs to another domain higher in the hierarchy.

Rather than changing the higher-level record, the attempted update is changed into an insert, and the **sys\_overrides** field is set to indicate the higher-level policy, application, or module that is being overridden. Later when the records for a relevant transaction are loaded, the overriding domain-specific policy, application, or module is used instead of the original.

## Domains for process administration

By default, process administration always uses the record's domain to determine what policies to apply.

The record's domain takes precedence over the user's domain. If there are no policies in the record's domain, delegated administration checks for policies in the next highest level of the domain hierarchy. The search for domain policies continues up the domain hierarchy until reaching the global domain. If there are no domain policies lower in the domain hierarchy, processes administration uses the policies for the global domain.

For example, Fred Luddy is a user in the Acme domain who can see records in the child domains of Acme: Atlanta, Acme: San Diego, and Acme: NY child domains. When this user opens a record in the Acme: San Diego domain, process administration first checks for policies in the Acme: San Diego domain. If there are no policies at this level of the domain hierarchy, process administration checks for policies from the Acme domain. If there are no policies in the Acme domain, process administration uses the global domain polices as there are no other domains higher in the domain hierarchy.

