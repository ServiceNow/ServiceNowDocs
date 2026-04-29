---
title: Exploring Machine Identity Console
description: Manage your service accounts, which are used for integrations with ServiceNow.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Machine Identity Console, Identity]
---

# Exploring Machine Identity Console

Manage your service accounts, which are used for integrations with ServiceNow.

Machine Identity Console enables you to manage your non-human identities \(NHIs\) that are used to identify, authenticate, and authorize different software entities to access secured resources of ServiceNow. The entities that gain access include applications, workloads, APIs, bots, and automated systems. Unlike human identities, non-human identities \(NHIs\) aren’t governed in the same manner and aren’t directly associated with a human. Their identity and verification methods are distinct from the human users, and standard human security measures are not applicable to them.

**Note:** You need the `mi_admin` role to use the Machine Identity Console.

Overview of Machine Identity Console 

Here's what is available on the Machine Identity Console Overview page:

-   Total Machine identity \(integration\) accounts and the Accounts with high privilege roles.
-   Unique API calls - Last 7 days
-   Authentication method used - Last 7 days
-   Machine Identity Security score and findings related to the identity.

**Note:** Accounts that have the **Internal Integration User** field set to `true` in their `sys_user` record will not populate data in the Machine Identity Console.

**Related topics**  


[Activating Machine Identity Console](../task/activate-machine-identity-console.md)

[Security findings](security-score.md)

[Metrics](machine-identity-metrics.md)

[Machine Identity Console Settings](../task/machine-identity-console-settings.md)

[Inbound integrations](inbound-integrations.md)

