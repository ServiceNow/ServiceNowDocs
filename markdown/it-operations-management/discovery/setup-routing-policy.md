---
title: Set up the routing policy for automated certificate management
description: Set up a routing policy to automate your Certificate Inventory and Management. Creating a policy based on Certificate Authority \(CA\), environment, and other features ensures efficient TLS certificate management.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Automated certificate management for TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Set up the routing policy for automated certificate management

Set up a routing policy to automate your Certificate Inventory and Management. Creating a policy based on Certificate Authority \(CA\), environment, and other features ensures efficient TLS certificate management.

## Before you begin

Role required: pki\_admin or admin

## About this task

The routing policy decides which CA must be contacted for certificate operations. It contains the CA, CA URL, Credential, Approval Group, Assignment Group, and CSR attributes. The routing policy triggers the flow for requesting certificates for specific CAs.

**Note:** A certificate request is considered a duplicate if there is another certificate task with the same domain name that is still in progress. Duplicate certificate requests are not allowed. However, you can override this setting by checking the Allow duplicate requests check box. Approvals are only supported in the Fulfiller approval experience at this time. See a table of fields that go into the routing policies at, [Certificate routing policy form table](../reference/certificate-routing-policy-form-table.md).

## Procedure

1.  Navigate to **All** &gt; **Certificate Management** &gt; **Certificate Routing Policies**.

2.  Select **New** and fill in the required fields on the form.

    While requests for new certificates and certificate renewal can be automated, many PKI teams prefer human validation before fulfillment. If so, select the **Approval required** check box.

    **Note:**

    Organization, Organizational Unit, Locality, State, Country, and Email accept comma-separated values. \* will be considered as any. Subject common name and Subject alternative name are supported with RegEx. The RegEx format has the following restrictions:

    -   It should not contain commas.
    -   It should not start and end with a forward slash \(/\) and \* matches any.
    -   For more inforamtion about the fields and values on a routing policy form, see [.](../reference/certificate-routing-policy-form-table.md)
3.  The following CSR attributes are matched with the entries in the Routing Policy \[sn\_disco\_certmgmt\_routing\_policy\] table:

    -   Organization
    -   Organizational Unit
    -   Locality
    -   State
    -   Country
    -   Email
    -   Environment
    -   Certificate Purpose\(internal/external\)
    -   Subject common name
    -   Subject alternative name
    **Note:** For Entrust CA Gateway, there are also these fields: Certificate Authority Identifier, Certificate Profile, and Certificate Format. For Microsoft CA also use these fields: Certificate Authority, CA template name, CA Host IP, Credential, and CSR attributes. For DigiCert, the routing policy also requires a Certificate Authority API URL field to handle automated processes and revocation flows.

4.  The following options may occur.

<table id="choicetable_ccx_lnc_nqb"><tbody><tr><td id="d72542e186">

**If a single routing policy matches**

</td><td>

Verify the following conditions: -   Validate the subject common name using the RegEx pattern provided in the Routing Policy table, domain name, or \*.
-   Check for certificate request validity period not greater than the maximum validity period in the Routing Policy table.
-   Check for duplicate Certificate Request is allowed flag in the Routing Policy table.


</td></tr><tr><td id="d72542e207">

**If multiple routing policies are eligible**

</td><td>

The task is assigned to the default approver group.

</td></tr><tr><td id="d72542e216">

**If there is no routing policy found**

</td><td>

The task is assigned to the default approver group.

</td></tr><tr><td id="d72542e225">

**If single policy matches and approval needed flag is true**

</td><td>

The task is assigned to the task approval group defined in the routing policy.

</td></tr></tbody>
</table>
## Result

The approval group is assigned to the routing policy and contains the role: pki\_approver and at least one of the active group members available in that group. If the routing policy requires manual approval, then approval is requested from those in the approval group.

## What to do next

The following knowledge base articles guide you through the process of producing the credentials required and configuring routing policies for different certificate authorities:

For Digicert, see [\[Digicert\] Configure automated certificate management for TLS certificates \[KB2166364\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2166364).

For Entrust, see [\[Entrust\] Configure automated certificate management for TLS certificates \[KB2173533\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2173533).

For Let's Encrypt, see [\[Let's Encrypt - ACME\] Configure automated certificate management for TLS certificates \[KB2197962\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2197962).

For Microsoft CA, see [\[Microsoft CA\] Configure automated certificate management for TLS certificates \[KB2198094\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2198094).

