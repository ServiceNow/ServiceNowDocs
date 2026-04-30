---
title: Associate an application service to a software model - Legacy
description: Business applications have multiple instances such as development, QA, and production. Instances are nothing but application services. Application services must be associated with software models \(to the respective full versions\) to know the risk of the application service.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Associate an application service to a software model - Legacy

Business applications have multiple instances such as development, QA, and production. Instances are nothing but application services. Application services must be associated with software models \(to the respective full versions\) to know the risk of the application service.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy business applications module is moved to the Enterprise Architecture Workspace. To learn more, see [Manage the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](../concept/eaw-concept/eaw-tpm.md).

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Technology Portfolio Management \(TPM\)** &gt; **Application Services**.

2.  Select the service record, which is the application service, to which you want to associate the software models.

3.  Select the **Application Service Software Models** related list.

4.  Select **New**.

    The Application Service Software Models \[sn\_apm\_tpm\_service\_software\_model\] database table stores the application service software model information. You can also navigate directly to the Application Service Software Models table from the application navigator. Data from this table is rendered as the software model timeline in the By Software Model view of the TPM screen.

5.  On the form, fill in the fields.

    For field information, see [Application Service Software Model form](../reference/application-service-software-model-form.md).

6.  Select **Submit**.


## What to do next

[Create risk parameter scores](create-risk-parameters.md) to evaluate the risk of the software model. Based on the risk of the software model you can calculate the risk of the application service. Finally, based on the risk of the application service you can evaluate the risk of the business application.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/using-apm.md)

