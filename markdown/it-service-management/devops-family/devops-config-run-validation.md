---
title: Run validation in DevOps Config
description: After you have installed and configured DevOps Config, validate the configuration and review the results.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, DevOps Config, IT Service Management]
---

# Run validation in DevOps Config

After you have installed and configured DevOps Config, validate the configuration and review the results.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: sn\_devops\_config.admin

## About this task

Having the policy validation action at the deployable level and the publish action at the snapshot level protects against non-compliant changes in your production environment.

You can also validate further by mapping more policies to a deployable and validating against your latest snapshot.

## Procedure

1.  Open your application and in the **Snapshots** tab, and select the snapshot created from the changeset created.

2.  Select **Validate** and confirm.

    All policies that are mapped statically and dynamically are run to validate the snapshot.

3.  Review compliance results.

    Any future snapshots generated are automatically validated against the configured statically mapped policies.Dynamic mappings are determined at runtime based on the latest conditions matching the deployable.


