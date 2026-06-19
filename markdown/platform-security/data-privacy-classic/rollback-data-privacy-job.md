---
title: Roll back a data privacy job
description: Roll back a data privacy job on your non-production instance that uses anonymized data from your production instance to a state prior to de-identification of a data class or user job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/data-privacy-classic/rollback-data-privacy-job.html
release: zurich
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data privacy job rollback, Data privacy \(Classic\) configuration, Data privacy \(Classic\), Data Privacy, Platform Privacy]
---

# Roll back a data privacy job

Roll back a data privacy job on your non-production instance that uses anonymized data from your production instance to a state prior to de-identification of a data class or user job.

## Before you begin

Role required: data\_privacy\_admin or data\_privacy\_processor, and admin

## Procedure

1.  Elevate to the **data\_privacy\_processor** or **data\_privacy\_admin** role.

    For details on role elevation, see [Elevate to a privileged role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/t_ElevateToAPrivilegedRole.md).

2.  Navigate to **All** &gt; **System Security** &gt; **Data Privacy** &gt; **Data Privacy Job**.

    **Note:** In advance, a data privacy policy configuration that supports rollback must be created. [Create a data privacy policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/config-dp-policy.md).

3.  Create a data privacy job and select a Privacy Configuration that supports Rollback.

    See [Configure a data privacy job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/config-data-privacy-job.md).

4.  Schedule the job for data anonymization.

    -   After the job has run, the data will be anonymized for the selected configuration.
    -   A message displays in the job informing of the expiration time. Within the expiry period you have the ability to roll back the job.\[Omitted image "dp-rollback-expiry-message.png"\] Alt text: Data privacy job rollback expiration time message.
5.  Elevate to the **data\_privacy\_processor** role.

6.  Open the data privacy job to be rolled back.

7.  Select **Rollback** to de-anonymize the data.


