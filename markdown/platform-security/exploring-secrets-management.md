---
title: Exploring Secrets Management
description: Use ServiceNow Secrets Management for granular management of access to your passwords to fit your business needs.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Secrets Management, Platform Security]
---

# Exploring Secrets Management

Use ServiceNow Secrets Management for granular management of access to your passwords to fit your business needs.

**Important:** Admins must have the role to see modules and records related to Secrets Management. For secrets management role information, see [Secrets management roles](../reference/roles-sec-man.md#).

## Select from Core and Enterprise versions of Secrets Management

Choose from Secrets Management Core and Secrets Management Enterprise depending on your business needs.

The Secrets Management Core plugin \(com.glide.sm.core\) is available by default. No installation is required on the instance for use. The Secrets Management Enterprise plugin is only available with a ServiceNow Vault v1, PROD18537 license. Contact Customer Support for assistance with the Secrets Management Enterprise plugin.

<table id="table_uc4_pq2_xtb"><thead><tr><th>

Secrets Management Core

</th><th>

Secrets Management Enterprise

</th></tr></thead><tbody><tr><td>

Secrets Management Core is available to install on your instance at no additional cost. The plugin provides the ability to use secrets groups with criteria in non-custom tables provided in the ServiceNow platform that have been created by ServiceNow application engineering teams.

</td><td>

Secrets Management Enterprise includes additional functions to help admins create and manage secrets groups. Enterprise provides the following features in addition to the features listed in Core.-   Use granular access controls to create secrets groups based on the any of these criteria.
    -   Scope
    -   Table
    -   Column
    -   Record
-   Create client-accessible secrets that are encrypted using your own key which ServiceNow can’t access.
-   Use the Secrets Management Dashboard to review the secret groups configured on your instance, and learn about potential security issues.

 **Note:** Secrets Management Enterprise is a paid plugin that ServiceNow personnel must activate on your production instance.

</td></tr></tbody>
</table>## Use secret groups to organize your secrets

Use Secrets Management to organize your secrets into groups, and then apply access policies to those secrets at a group level.

-   **Basic secret group**

    These groups apply to all secrets in a scope. These secrets are decrypted by a common cryptographic module and module access policies.

-   **Secret group with criteria**

    Secret groups with criteria function the same as a basic secret group, but further refine what is included using criteria. These criteria include:

    -   Application scope
    -   Package
    -   Table
    -   Secret column
    -   Filter record

Secret groups of either type can be made instance accessible or client accessible.

-   **Instance side secret groups**

    Instance side secret groups contain secrets that can be decrypted by your instance.

-   **Client-side secret groups**

    Client-side secrets groups use a public and private key pair to help ensure that secrets can only be decrypted by the client. When you create a client-accessible secrets group, you upload the public key to the instance, and retain the private key on your MID Server. The instance uses the public key to encrypt your secrets, but they can only be decrypted using the private key.


**Note:** For more information on these group types, see [Understanding client side Secrets Management](understand-sec-man.md).

## Use secrets groups for more granular control

While password2 is available on the ServiceNow platform, Secrets Management provides these additional features.

<table id="table_eqh_b2j_ktb"><tbody><tr><td>

Granular access controls

</td><td>

-   **Password2**

With password2, admins can control access to an application scope, but can’t restrict access to elements within the scope.

-   **Secrets Management**

With Secrets Management, admins can restrict access based on criteria they define. Criteria types can be based on criteria such as package, table, or column.


</td></tr><tr><td>

Secure Storage

</td><td>

For client-side secret groups, Secrets Management uses a new encryption scheme. In this encryption scheme, ServiceNow doesn’t save the encryption key. For this reason, the security of your data doesn’t depend on ServiceNow security.

</td></tr></tbody>
</table>## Apply module access policies to your groups

After you’ve grouped your secrets into a secret group, you can apply policies that determine how you can access them at a group level. Module access policies are the access control mechanisms that you apply to cryptographic modules to define instance-level controls, such as a validity time frame for the cryptographic key. For more information on module access policies, see [Module access policy overview](../../key-management-framework/concept/module_access_policy_overview.md).

## Tables installed with Secrets Management

Secrets Management adds or modifies these tables.

<table id="table_orx_gt1_dtb"><tbody><tr><td class="sub-head" colspan="2">

New Tables

</td></tr><tr><td>

\[sn\_sm\_secret\_group\]

</td><td>

Stores secret groups

</td></tr><tr><td>

\[sn\_sm\_secret\_group\_criteria\]

</td><td>

Stores criteria secret groups

</td></tr><tr><td>

\[sn\_sm\_secret\]

</td><td>

Stores wrapped secrets

</td></tr><tr><td>

\[sn\_sm\_identity\_group\]

</td><td>

Defines the identity group for mapping a group of identities to the public key

</td></tr><tr><td>

\[sys\_kmf\_wrapped\_module\_key\]

</td><td>

Stores the wrapped symmetric cryptographic keys

</td></tr><tr><td class="sub-head" colspan="2">

Modified Tables

</td></tr><tr><td>

\[sys\_kmf\_crypto\_module\]

</td><td>

Added cryptographic module type. \(Identity cryptographic module or secret group cryptographic module\)

</td></tr><tr><td>

\[sys\_kmf\_module\_key\]

</td><td>

-   Stores conceptual secret encryption key \(with no key material\)
-   Stores the identity public key

</td></tr><tr><td>

\[sys\_kmf\_crypto\_caller\_policy\]

</td><td>

Added new module access policy type

</td></tr></tbody>
</table>## Secrets Management use case examples

-   **Help ensure secure ITOM Discovery**

    This infographic shows a simplified reference architecture of how ServiceNow IT Operations Management \(ITOM\) Discovery can be deployed by your organization. As shown in the infographic, multiple Windows and Linux servers connect to the Management, Instrumentation, and Discovery \(MID\) Server and several MID Server agents enable the discovery process to update the Configuration Management Database \(CMDB\). Every MID server transaction requires a secure authentication, hence managing the authentication credentials is critical from a security perspective.

-   **Accelerating workflow connectivity with Integration Hub securely**

    Use ServiceNow's Integration Hub to connect to different systems using automated application programming interface \(APIs\). Each time Integration Hub connects to a system using an API, an authentication credential is required to establish connectivity. Management of a multitude of applications and APIs for connectivity requires a secrets management solution.

    Secrets Management is a key part of ensuring your organization’s cybersecurity. It covers all processes and tools related to the creation, storage, transmission, and management of digital credentials such as encryption keys, API tokens, and passwords. To manage secrets both securely and effectively, you can build a core secrets management policy that establishes standard rules and procedures for all phases of a secret’s lifecycle.


-   **[Understanding client side Secrets Management](understand-sec-man.md)**  
Learn how use Secrets Management to manage access to secrets and groups.

**Parent Topic:**[Secrets Management](secrets-management.md)

