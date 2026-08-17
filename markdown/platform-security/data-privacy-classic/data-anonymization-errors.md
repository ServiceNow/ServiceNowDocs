---
title: Data anonymization errors
description: When executing anonymization jobs, the following error states may be encountered. All known runtime errors are listed here.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/data-anonymization-errors.html
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Data anonymization, Data privacy, Data Privacy, Platform Privacy]
---

# Data anonymization errors

When executing anonymization jobs, the following error states may be encountered. All known runtime errors are listed here.

You can see the list of runtime errors for any anonymization job by looking at its logs:

-   For Data Privacy \(Classic\), navigate to **All &gt; System Security &gt; Data Privacy \(Classic\) &gt; Data Privacy Job Logs**.
-   For Data Priacy Store, error logs are linked to individual job records. Select any job name, then the **Error logs** tab to display a related list of runtime errors for that job.

|Error code|Designator|Description|
|----------|----------|-----------|
|RTE0001|`RUNTIME_ERROR_CODE_FOR_EXCEEDING_LENGTH`|Data anonymization was skipped. This is because the length of the anonymized value exceeded the column size by a defined percentage of characters.|
|RTE0002|`RUNTIME_ERROR_CODE_FOR_MANDATORY_COLUMN_EMPTY`|Data anonymization was skipped. This is because the target column was empty.|
|RTE0003|`RUNTIME_ERROR_CODE_FOR_DECRYPTION_ERROR`|Data anonymization was skipped. This is because the data anonymization job failed to decrypt the data.|
|RTE0004|`RUNTIME_ERROR_CODE_FOR_ENCRYPTION_ERROR`|Data anonymization was skipped. This is because the data anonymization job failed to re-encrypt the data.|

