---
title: Data privacy job rollback
description: Database changes are captured for actions like jobs and scripts so that the changes can be rolled back. Roll back a data privacy job for when human error inadvertently anonymizes incorrect user information. The rollback de-anonymizes the data from the data privacy job.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/data-privacy-classic/data-privacy-job-rollback.html
release: zurich
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data privacy \(Classic\) configuration, Data privacy \(Classic\), Data Privacy, Platform Privacy]
---

# Data privacy job rollback

Database changes are captured for actions like jobs and scripts so that the changes can be rolled back. Roll back a data privacy job for when human error inadvertently anonymizes incorrect user information. The rollback de-anonymizes the data from the data privacy job.

## Overview

-   Rollback is limited to a few days, per the configured expiry duration of the RollbackContext of the new RollbackType **REDACT**. After expiration of the RollbackContext associated with a data privacy job, the rollback function is no longer available for that job.
    -   A rollback context from de-anonymization is saved for three days by default.
    -   The default expiry time can be set to a value greater than one by the data privacy administrator in the **RollbackContext** of the new **RollbackType** **REDACT.** Set the value in the Glide system property **glide.rollback.expiration\_days\_redact**. See [Roll back and delete recovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/table-administration-and-data-management/rollback-delete-recovery.md).

        To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

        for additional information.

-   Rollback is available for data privacy jobs that are in a Completed, Canceled, or Error state.
-   For every successful sys\_user de-anonymization job which is configured with a data privacy policy with rollback support turned on, a rollback context is created. There can be at most one rollback context per data privacy job.

