---
title: Create aliases
description: Aliases are the variants of a field value in the instance that will be replaced by the normal value.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Normal values, Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create aliases

Aliases are the variants of a field value in the instance that will be replaced by the normal value.

## Before you begin

Role required: admin or normalizer

## About this task

The list of potential aliases is the contents of the **Pending Values** related list. After creating a normal value, assign aliases to this value if the pool of pending values is small. A normalized field can have a combination of aliases and rules.

## Procedure

1.  Navigate to **All** &gt; **Field Normalization** &gt; **Configurations** &gt; **Normalizations**.

2.  Open a normalization record.

3.  Click the **Normal Values** related list.

4.  Select one of the values.

5.  In the normal value record, click the **Aliases** related link.

6.  Select aliases for this normal value from the available \(pending\) values that appear in the slushbucket, and then click **OK**.

    ![Normalization alias slush](../image/NormalizationAliasSlush.png)

    The aliases for this normal value now appear in the **Aliases** related list.


## What to do next

Apply the aliases by running the associated data jobs.

