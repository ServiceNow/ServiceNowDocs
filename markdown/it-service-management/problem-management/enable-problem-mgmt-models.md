---
title: Enable Problem Management models
description: Enable the Problem Management models system property so that you can create and use custom models.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Problem Management, Problem Management, IT Service Management]
---

# Enable Problem Management models

Enable the Problem Management models system property so that you can create and use custom models.

## Before you begin

The **com.snc.problem\_management.models.enabled** system property is enabled by default for new customers starting from the Yokohama release.

See considerations for enabling and disabling Problem Management models at [Problem Management models](../concept/problem-mgmt-models.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  From the Name column, search for `*models`.

3.  Select the **com.snc.problem\_management.models.enabled** system property.

4.  Set the **Value** field to **True**.

5.  Select **Update**.


## Result

Problem Management models are enabled.

**Parent Topic:**[Configuring Problem Management](../concept/configuring-problem-mgmt.md)

**Previous topic:**[Categorize a problem as a major problem](categorize-major-problem.md)

**Next topic:**[Create a problem model](create-problem-model.md)

