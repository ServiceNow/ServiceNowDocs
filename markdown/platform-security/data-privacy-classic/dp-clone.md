---
title: Data privacy clone
description: As customer data are cloned from a source to a target instance, typically from production to non-production, sensitive data are de-identified on the target instance.​
locale: en-US
release: yokohama
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data privacy \(Classic\), Data Privacy, Platform Privacy]
---

# Data privacy clone

As customer data are cloned from a source to a target instance, typically from production to non-production, sensitive data are de-identified on the target instance.​

A data privacy administrator configures post-clone policies.​ After the post-clone script completes on the target instance, the users will see de-identified data and will not have access to the original data. Data privacy administrators can configure de-identification policies to apply on the target instance when cloning to ensure that the target instance will not have original sensitive data.​ An order is specified for the policy relative to other policies to be executed.

**Note:** Data privacy cloning is not available on self-hosted instances.

Data privacy clone has the following additional attributes:

-   The data privacy plugin creates the post clone script to be executed on the target instance.
-   Data privacy jobs created for PostClone configuration can run in parallel if they don’t involve the same tables.​
-   A data privacy job for Postclone configuration with a higher Application Order might start before another job of lower order, if the job with the higher order does not involve any table related to other lower order job.
-   With the data privacy plugin, data privacy tables are by default in the Clone Data Preservers table set.​
-   An attempt to add a data privacy table \(dp\_\[table\]\) to Clone Exclude Tables will get a warning, that table should not be excluded.​

