---
title: Authenticator configuration options
description: Use the Authenticator Configuration page to manage authenticator options on your instance.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Web Authentication, MFA verification methods, Configure MFA, Multi-factor authentication, Authentication, Access Management]
---

# Authenticator configuration options

Use the Authenticator Configuration page to manage authenticator options on your instance.

Navigate to **Multi-factor Authentication** &gt; **Web Authentication** &gt; **Authenticator Configuration** to view and edit the default configuration options.

<table id="table_uds_zcj_zpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allowed authenticator type

</td><td>

Type of authenticators allowed to be registered. Select from: -   **Platform** authenticators are attached or integrated into a device. Fingerprint readers or facial recognition available on mobile devices \(such as Apple FaceID or TouchID\) fall under this category.
-   **Roaming** authenticators can be removed from a computer or other client device and used elsewhere. Hardware keys fall under this category.

</td></tr><tr><td>

Attestation Type

</td><td>

Setting the value to direct or indirect will require importing authenticator metadata to attest to the provenance of an authenticator during registration.-   None
-   Direct
-   Indirect

</td></tr><tr><td>

Platform self-attestation

</td><td>

Whether self-attestation is enabled for platform authenticators.

</td></tr><tr><td>

Cross platform self-attestation

</td><td>

Whether self-attestation is enabled for roaming authenticators.

</td></tr><tr><td>

User verification

</td><td>

Select from **Preferred** or **Required**. If required, web authentication flow prompts users for verification using PIN or Biometrics.

</td></tr><tr><td>

Verify user presence

</td><td>

Whether web authentication flow requires the user presence verification.

</td></tr><tr><td>

Resident key

</td><td>

Select from **Preferred** or **Required**. If required, the authenticator persists the public key credentials within the authenticator storage.

</td></tr><tr><td>

Timeout \(In ms\)

</td><td>

Maximum time limit for completing web authentication registration and authentication. Time is in milliseconds.

</td></tr></tbody>
</table>