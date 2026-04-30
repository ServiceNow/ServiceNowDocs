---
title: Agent Client Collector certificate revocation reasons
description: The following table lists and describes the possible reasons for revoking an Agent Client Collector certificate to stop communication between the agent and ITOM cloud services.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector certificate revocation reasons

The following table lists and describes the possible reasons for revoking an Agent Client Collector certificate to stop communication between the agent and ITOM cloud services.

<table id="table_ckg_4yj_tfc"><thead><tr><th>

Reason

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unspecified

</td><td>

Revoke a certificate without providing a specific revocation code.**Note:** This reason code doesn’t provide an audit trail identifying why a certificate was revoked.

</td></tr><tr><td>

Key Compromise

</td><td>

You suspect that the private key associated with a certificate is compromised.For example, if a laptop belonging to a user in your organization is stolen, any private keys stored on the laptop may be compromised.

</td></tr><tr><td>

CA Compromise

</td><td>

You suspect that a Certificate Authority's \(CA\) private key has been compromised and is in the hands of an unauthorized individual. If a CA’s private key is revoked, the CA hierarchy considers all certificates below that CA revoked as well.

</td></tr><tr><td>

Affiliation Changed

</td><td>

An individual is no longer working in the organization, or the computer account to which the certificate was issued is no longer in use. Can also be used if a person changes roles within an organization and no longer requires using the certificate associated with their previous role.For example, an employee could move from the purchasing department and no longer require a certificate to authorize purchase requests.

</td></tr><tr><td>

Superseded

</td><td>

Indicates that a new certificate must be issued in place of a previously issued certificate. For example, if you update a certificate template and reissue certificates, you could revoke the previous certificate with this reason code.

</td></tr><tr><td>

Cessation of Operation

</td><td>

A server or workstation is decommissioned, and all certificates issued to the server are no longer required. You can use this revocation reason when decommissioning a CA.

</td></tr><tr><td>

Certificate Hold

</td><td>

A temporary revocation indicating that a CA won’t validate a certificate at that specific time.**Note:** Using this reason code makes it difficult to determine whether a certificate was valid at a specific time.

</td></tr><tr><td>

Remove from CRL

</td><td>

Enables future unrevoking of the certificate, removing the certificate from the certificate revocation list \(CRL\).

</td></tr><tr><td>

Privilege Withdrawn

</td><td>

The certificate holder no longer has the privileges required to continue using the certificate.

</td></tr><tr><td>

AA Compromise

</td><td>

Indicates suspected or actual compromise of the authentication authority \(AA\) validated in the certificate.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

