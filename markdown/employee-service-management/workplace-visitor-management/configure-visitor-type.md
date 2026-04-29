---
title: Configure a visitor type
description: Create a visitor type that can be used to categorize visitors for your hosts or reception staff.
locale: en-US
release: australia
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2026-03-15"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Configure a visitor type

Create a visitor type that can be used to categorize visitors for your hosts or reception staff.

## Before you begin

Role required: sn\_wsd\_visitor.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Visitor Management** &gt; **Administration** &gt; **Visitor types**.

2.  On the Visitor types list, select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the visitor type, like prospect or candidate.|
    |Order|Order of the visitor type in the list while adding visitors. Visitor types with a lower order are displayed first.|
    |Label|Label of the visitor type that is displayed while adding visitors.|
    |Active|Option to set the record to active. Inactive visitor types are not displayed while adding visitors.|

4.  In the **Available if** field, add conditions for when the visitor type is available.

    For more information about conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    To include workplace locations within a parent location, you must add conditions to dot-walk from the nested locations to the parent location.

    To include all the buildings, floors, and spaces in the Demo Campus, add the following conditions.

    -   `Workplace Location is Demo Campus` OR
    -   `Workplace Location.Building.Campus is Demo Campus` OR
    -   `Workplace Location.Floor.Campus is Demo Campus` OR
    -   `Workplace Location.Space.Campus is Demo Campus`
5.  Save the record.

    The visitor type is created and is available to hosts and reception staff members.


**Parent Topic:**[Configuring Workplace Visitor Management](../concept/configure-visitor-mgmt.md)

**Related topics**  


[Install Workplace Visitor Management](install-workplace-visitor-mgmt.md)

[Create a visitor policy](create-visitor-policy.md)

[Create a record producer for visitor management](create-rec-prodcr-visit-mgmt.md)

[Configure visit requirements](configure-visit-requirements.md)

[Create a visitor badge template](create-visitor-badge-template.md)

[Configuring Workplace Visitor Management for Workplace Services Kiosk](../concept/config-visitor-for-kiosk.md)

[Quick start test for Workplace Visitor Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-wsd-visitor-mgmt.md)

