---
title: Restrict MID IPKI registration key retry attempts
description: Configure the registration key retry threshold to prevent unauthorized Management, Instrumentation, and Discovery \(MID\) Server registration attempts. Setting the sn\_mid\_infra.registration\_key.max\_use\_count property limits how many times a registration key can be used before it is revoked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-restrict-mid-ipki-registration-key-retry.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Restrict MID IPKI registration key retry attempts

Configure the registration key retry threshold to prevent unauthorized Management, Instrumentation, and Discovery \(MID\) Server registration attempts. Setting the **sn\_mid\_infra.registration\_key.max\_use\_count** property limits how many times a registration key can be used before it is revoked.

The MID Internal Public Key Infrastructure \(IPKI\) feature uses registration keys to issue IPKI certificates to MID agents. This property controls the maximum number of failed attempts allowed before a registration key is revoked. The default value of `five` allows a limited number of retries. Lower values restrict retries further; higher values increase retry attempts.

Configure the **sc-restrict-mid-ipki-registration-key-retry** property

1.  Navigate to `/sys_properties_list.do` on your ServiceNow instance.
2.  Search for the **sn\_mid\_infra.registration\_key.max\_use\_count** property.
3.  Set the value to a number between 3-5. Don't exceed 5.

    Lower values within this range provide a more restrictive security posture while maintaining reasonable tolerance for legitimate registration failures. Save the property configuration.

4.  Test the configuration by initiating a new MID IPKI registration and verify that the certificate is issued successfully.
5.  Monitor MID registration logs for any revocation events indicating the retry threshold has been reached.

## More information

<table id="table_ajc_y23_3ik"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_mid\_infra.registration\_key.max\_use\_count**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \( `/sys_properties_list.do`\)

</td></tr><tr><td>

Data type

</td><td>

Integer

</td></tr><tr><td>

Recommended value

</td><td>

3-5

</td></tr><tr><td>

Default value

</td><td>

5

</td></tr><tr><td>

Fallback value

</td><td>

5

</td></tr><tr><td>

Category

</td><td>

[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.4
-   CVSS rating: Medium
-   Security risk details: Setting this property to a high value allows an attacker with a registration key to attempt multiple failed registrations before the key is auto-revoked. A higher retry threshold extends the attack window and can increase the opportunity to identify validation weaknesses or bypass registration controls. This can lead to unauthorized IPKI certificate issuance or compromise of MID agent identity validation.

</td></tr><tr><td>

Functional impact

</td><td>

Modifying this property changes the maximum number of retries allowed for a registration key on failure before permanent revocation.

 Setting a lower value reduces the chances of successful registration if temporary or transient failures occur during the registration process. Setting a higher value increases the likelihood of successful registration but allows more retry attempts before revocation, potentially delaying detection of persistent registration failures.

 Instance owners must test new MID IPKI registrations to verify that the registration key is issued successfully with the configured retry count.

 Beyond confirming successful registration, no additional regression testing is possible.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-authentication.md)

