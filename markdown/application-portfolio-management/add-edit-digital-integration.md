---
title: Create a digital integration
description: Create a digital integration in Enterprise Architecture \(formerly Application Portfolio Management\), to create a connection between a consuming business application and a provider business application.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Digital integrations, Manage digital intergations, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create a digital integration

Create a digital integration in Enterprise Architecture \(formerly Application Portfolio Management\), to create a connection between a consuming business application and a provider business application.

## About this task

The digital integration is a design object used by the Enterprise Architects. It describes a connection between two business applications or between a business application and an external service \(for example: AWS, Yahoo, a TimeZone Conversion service\) that provides an interface \(API\) to interact with.

You can define why a connection is required between two data entities, over which Interfaces they should communicate, and provides a link to relevant design and architectural material. A Digital Integration underpins a business capability and provides business value.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy digital integrations module is moved to the Enterprise Architecture Workspace. To learn more, see [Add or edit a digital integration in the EA Workspace](eaw-task/eaw-create-digital-integ.md).

If you have an Enterprise Architecture user role \(sn\_apm.apm\_user\), use the Business Application Life-cycle Management services to request, add, or retire a business application.

Role required: sn\_apm.apm\_analyst

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio** &gt; **Digital Integrations**.

2.  Select **New**

3.  On the Create Digital Integration form, fill in the fields.

    For a description of the field values, see [Create digital integration form](../reference/create-digital-integration-form.md).

4.  Select **Submit**.


## Result

On the Digital Integrations page, a success message and the link to the newly created digital integration appear.

After submission of the form, within the CMDB platform, a CI relationship \(Interfaces::Interfaced By\) gets created between provider and subscriber business applications. In a case, where the digital interface has no relation to a business application \(using Open or Public API\), the digital integration is created between the subscriber business application and a standalone digital interface.

