---
title: Data anonymization
description: Anonymization provides a way to easily transform data so that it is unidentifiable and more compliant with data privacy regulations.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Platform Privacy]
---

# Data anonymization

Anonymization provides a way to easily transform data so that it is unidentifiable and more compliant with data privacy regulations.

Administrators can perform the anonymization process in both production and non-production instances. Data privacy can be used in production instances to de-identify users. Anonymization of data classes should only be used with non-production instances. This preservation ensures that data like email addresses or physical addresses are replaced with similarly formatted, but anonymized versions.

Administrators can also use anonymization as part of their General Data Protection Regulation \(GDPR\) Right to be forgotten \(RTBF\) processes to anonymize user information. See [https://gdpr-info.eu/art-17-gdpr/](https://gdpr-info.eu/art-17-gdpr/) for more information.

Use the anonymization section of data privacy to create and view privacy policies and techniques,and to perform privacy bulk assignment. View all of the jobs, with the description, private policy used, and status. In order to access the anonymization section, an admin must first elevate to the data\_privacy\_admin and data\_privacy\_processor roles.

## Anonymization techniques

Anonymization techniques are options you select to determine how your data is anonymized. You must create an anonymization technique to reference in the anonymization job. See [Create anonymization techniques](../task/dps-create-anonymization-techniques.md) to associate a privacy technique to an associated **Anonymization technique configuration**.

## Anonymization policies

Configure an anonymization policy to specify which data privacy techniques are used when anonymizing your data. See for [Create anonymization policies](../task/dps-create-anonymization-policies.md) details.

## Anonymization jobs

Anonymization jobs use all of these components to anonymize your data. For more information on these jobs, see [Create anonymization job](../task/dps-create-anonymization-job.md).

