---
title: Configure a workplace service record producer as a Universal Request
description: Enable an employee to submit a universal request using a workplace service record producer from the Workplace Service Portal. Configure a workplace service to create Universal Request whenever an employee makes a selection.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with Universal Request, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configure a workplace service record producer as a Universal Request

Enable an employee to submit a universal request using a workplace service record producer from the Workplace Service Portal. Configure a workplace service to create Universal Request whenever an employee makes a selection.

## Before you begin

Ensure that you have activated the Universal Request plugin.

Ensure that you have the following:

-   A workplace service that is linked to a record producer. For more information, see [Configure a Record producer](wsd-create-record-producer.md).
-   An active record producer.

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Record producers**.

2.  Select the record producer that you want to configure as a universal request.

3.  Select **Universal Request Config** tab.

4.  To enable the universal request feature, select **Create Universal Request**.

5.  If the universal request requires an extra review, select **Requires Additional Review**.

6.  Click **Update**.


## Result

The workplace service record producer is configured as a universal request.

When an employee submits an inquiry using this workplace service, a universal request is created. The request is automatically assigned to the Workplace services assignment group.

**Parent Topic:**[Workplace Service Delivery integration with Universal Request](../concept/wsd-intergration-with-universal-request.md)

**Related topics**  


[Create a workplace case from Universal Request](create-workplace-case-from-universal-req.md)

[Work on a workplace case from a Universal Request](work-on-workplace-case-of-universal-req.md)

[Transfer a workplace case created from a universal request](transfer-a-workplace-case-created-from-a-universal-request.md)

