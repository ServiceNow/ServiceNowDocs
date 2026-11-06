---
title: MID Server IPKI reference
description: Learn about configuration parameters, keystore aliases, instance-side tables, and log messages for MID Server IPKI authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/mid-server/mid-server-ipki-reference.html
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 5
keywords: [iPKI, mid.ipki.enabled, DefaultSecurityKeyPairHandle]
breadcrumb: [MID Server IPKI authentication, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server IPKI reference

Learn about configuration parameters, keystore aliases, instance-side tables, and log messages for MID Server IPKI authentication.

## MID Server configuration parameters

<table id="table-mid-ipki-config"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**mid.ipki.enabled**

</td><td>

Set to `true` to put the MID Server into IPKI mode.

</td></tr><tr><td>

**mid.ipki.registration\_key**

</td><td>

A valid registration key. Required only for the initial registration, or to manually reregister a MID Server. Cleared automatically after use.

</td></tr><tr><td>

**mid.ipki.user**

</td><td>

The sys\_id of the MID Server user that this MID Server acts as.

</td></tr><tr><td>

**mid.ipki.rotation\_trigger\_threshold**

</td><td>

The number of days before a certificate expires at which the MID Server attempts to rotate it. IPKI certificates expire after 60 days. The default value is 15, so rotation starts 15 days before expiration. Enter a value from 8 to 59.

</td></tr></tbody>
</table>## Instance-side tables

|Table|Purpose|
|-----|-------|
|`sys_kmf_certificate`|Stores the issued certificates.|
|`sn_mid_infra_cert_map`|Maps a MID Server to its certificate and tracks whether that mapping is processing, active, superseded, or inactive. Controls revocation.|
|`sn_mid_registration_key`|Stores registration keys and their state: unused, consumed, or revoked.|
|`ecc_agent`|The MID Server record, including its status.|

## JWT claims

MID Server sends a signed JSON Web Token \(JWT\) to its instance as a bearer token with each request, so that the instance can authenticate the MID Server. The payload of the token contains the JWT claims used by IPKI.

|Claim|Description|
|-----|-----------|
|`iss`|The common name \(CN\) of the leaf certificate. The instance requires this claim and rejects the token if the value does not match the CN of the certificate in the token header.|
|`sub`|The user that the MID Server acts as. The MID Server takes it from the `UID` field of its certificate, using the part after the hyphen. The instance resolves the acting user using this claim.|
|`aud`|The target instance. The instance requires this claim. The claim value must match the instance name, the instance ID, the default instance URL, or a URL that contains the active instance DNS name. The instance rejects the token if the value does not match.|
|`exp`|The time at which the token expires. It is the issue time plus the value of the **mid.jwt.token\_ttl** parameter. The default value is 15 minutes, with a minimum of 60 seconds and a maximum of 1 hour. The instance requires this claim and allows 10 seconds of clock skew.|
|`nbf`|The time at which the token becomes valid. The MID Server sets it to the issue time, so the token is valid as soon as it is created. The instance requires this claim and allows 10 seconds of clock skew.|
|`iat`|The time at which the token was issued.|
|`nonce`|A random value that makes each token unique. The MID Server adds it to every token.|
|`jti`|A unique ID for the token. The MID Server does not set this claim.|
|`htm`, `htu`|The HTTP method and the path of the request. These claims are optional. If they are present, the instance checks them against the request.|

The instance also checks that the token header type is `kaa+jwt`. The header must contain the certificate chain. The signature must verify with the public key of the leaf certificate.

## Log messages and issues

|Message or issue|Cause|What to do|
|----------------|-----|----------|
|`IPKI migration rejected: MID server is not validated`|The MID Server isn't validated.|Validate the MID Server, and then migrate it again.|
|`IPKI migration rejected: MID server is already IPKI enabled`|The MID Server already uses IPKI.|The MID Server already uses IPKI. To confirm, check that the **mid.ipki.enabled** parameter is set to true in the MID Server configuration parameters.|
|`Missing parameter: migration_key_payload_encrypted`|The instance didn't send the migration payload to the MID Server.|Contact Customer Service and Support and include the agent log.|
|`Failed to complete IPKI migration` or `Unexpected error during IPKI migration`|The migration failed after the MID Server accepted the request. The message includes the reason.|Use the reason in the message to find the cause. If it doesn't help, contact Customer Service and Support with the message text.|
|`IPKI certificate rotation failed for alias DefaultSecurityKeyPairHandle`|The MID Server couldn't get a new certificate.|Check the instance logs for entries from the `sn_mid_infra` source to find more details about the failure.|
|The `Mid-CertificateRotationRequired` issue|Rotation keeps failing, and the certificate expires in 7 days or less.|To fix the problem immediately, force rotation from the instance. The MID Server also retries rotation automatically every hour. If the instance returned an error code, check the instance logs for entries from the `sn_mid_infra` source for more details.|
|`Automatic rotation is not possible; manual re-registration is required`|The certificate has expired.|Reregister the MID Server. For the steps, see [Reregister MID Servers to restore IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-reregister-ipki-authentication.md).|
|`MID service user lacks PolKit permission to manage the systemd service`|The user that runs the MID Server service isn't authorized to manage the system service. The MID Server might not restart after an upgrade or after certificate rotation.|Create a PolKit rule for the MID Server service user.|

## PolKit rules for the MID Server on Linux

During IPKI operations, the MID Server restarts automatically. On Linux, if the MID Server service runs as a user other than root, that user might need PolKit authorization to manage the service. To know about PolKit permission warning and resolution, see [KB2934327](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2934327).

**Parent Topic:**[MID Server IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-authentication.md)

**Related topics**  


[MID Server authentication methods comparison](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-authentication-comparison.md)

