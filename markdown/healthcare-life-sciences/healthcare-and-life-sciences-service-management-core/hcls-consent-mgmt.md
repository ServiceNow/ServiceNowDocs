---
title: Determining the consent management process for patients
description: You can determine whether the privacy policy for patient consent needs to be routed for review and signature to the patient.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Determining the consent management process for patients

You can determine whether the privacy policy for patient consent needs to be routed for review and signature to the patient.

As a user with the sn\_hcls.admin role, you can configure a privacy policy for obtaining consent from patients in a healthcare organization. For more information, see [Configure a privacy policy for managing patient consent](../task/hcls-config-policy-consent.md).

You can determine the consent management process as one of the following types:

-   [Standard](hcls-consent-mgmt.md#section_ar1_sb2_ftb)
-   [Document](hcls-consent-mgmt.md#section_lgc_pb2_ftb)

## Configuring standard policy types

A standard policy doesn't require a consent form to be reviewed or signed by a patient.

With the Standard policy type, a patient is required to sign the same consent again and again each time a service is requested.

## Configuring document policy types

A document policy requires a consent form to be reviewed, signed, or both by a patient.

With the Document template policy type, a to-do item is created for the patient to sign the consent form.

You must configure the document that needs to be signed by a patient, create decision rules for it, and reference the document in the policy. For more information, see [Configuring document templates for Healthcare and Life Sciences Service Management Core](hcls-config-doc-templates.md).

**Note:** You can associate only one active policy with a document template.

When setting up the privacy policy, you can also specify the validity duration in days for the consent after a patient signs the consent form. An accepted consent for an active policy is valid for multiple healthcare requests until the validity duration specified in the policy starting from date when the consent was given. Therefore, a patient needs to give consent only once for all healthcare requests submitted during the validity duration of an active consent policy. By default, the **Set inactive status for expired policy consents** scheduled job is configured to set any policy consent as inactive when the policy validity duration has expired.

After a patient gives the consent, the consent document is added as an attachment to the policy consent. The case associated with the initial healthcare request for which the consent was given is associated with the policy consent record.

The existing policy consent is associated with a new case to address another request from the same patient when all of the following conditions are true:

-   The consent privacy policy is still active.
-   The case was created within the validity duration of the accepted consent.
-   The document decision rule of the document template associated with the new case is met.

Else, another to-do item is created for the patient to provide the consent.

When working on a healthcare case, a healthcare agent can then review and verify the accepted consent. If no consent was accepted, the healthcare agent has to wait until the patient gives the consent.

