---
title: Enable Problem Management models
description: Enable the Problem Management models system property so that you can create and use custom models.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/problem-management/enable-problem-mgmt-models.html
release: zurich
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Problem Management, IT Service Management]
---

# Enable Problem Management models

Enable the Problem Management models system property so that you can create and use custom models.

## Before you begin

The **com.snc.problem\_management.models.enabled** system property is enabled by default for new customers starting from the Yokohama release.

See considerations for enabling and disabling Problem Management models at [Problem Management models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/problem-mgmt-models.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  From the Name column, search for `*models`.

3.  Select the **com.snc.problem\_management.models.enabled** system property.

4.  Set the **Value** field to **True**.

5.  Select **Update**.


## Result

Problem Management models are enabled.

**Parent Topic:**[Configuring Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/configuring-problem-mgmt.md)

**Previous topic:**[Categorize a problem as a major problem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/categorize-major-problem.md)

**Next topic:**[Create a problem model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/problem-management/create-problem-model.md)

