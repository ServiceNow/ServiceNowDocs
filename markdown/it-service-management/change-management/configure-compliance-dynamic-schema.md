---
title: Configure the compliance dynamic schema
description: Review and adjust the dynamic namespace that supports the risk and compliance fields on a change request. Ensure the attributes and categories match the compliance obligations of your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/configure-compliance-dynamic-schema.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Compliance dynamic schema, Configure, Change Management, IT Service Management]
---

# Configure the compliance dynamic schema

Review and adjust the dynamic namespace that supports the risk and compliance fields on a change request. Ensure the attributes and categories match the compliance obligations of your organization.

## Before you begin

Decide which risk and compliance details your organization records with every change, because the attributes and categories in the base system are examples.

Role required: admin

## About this task

The compliance dynamic schema for change requests is delivered as a single dynamic namespace. Configuring the namespace changes which attributes users can record in the **Risk and compliance attributes** field and which categories they can select in the **Risk and compliance category** field. For information about the elements that make up the schema, see [Compliance dynamic schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/compliance-dynamic-schema.md).

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Compliance Dynamic Schema**.

    The module opens the `change_request/risk_and_compliance_attributes` dynamic namespace record directly. You can also reach the same record from the platform by opening the Dynamic Namespaces list.

2.  Review the fields on the dynamic namespace record.

    |Field|Description|
    |-----|-----------|
    |Label|Display name of the namespace. For change requests, the label is `Change request/risk and compliance attributes`.|
    |Name|System name of the namespace, `change_request/risk_and_compliance_attributes`. Scripts use this name to read the stored attributes.|
    |Description|Purpose of the namespace.|
    |Application|Application that the namespace belongs to.|
    |Active|Option for making the namespace available to the store field.|

3.  On the **Dynamic Attributes** tab, review the attributes that users can record.

    The related list shows the name, label, type, choice set, description, and active state of each attribute. To add or update a dynamic attribute, see [Dynamic Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dynamic-schema.md) .

4.  Select the **Dynamic Categories** tab and review the categories that users can select.

    A category groups the attributes that are relevant to a kind of change. Set the **Parent** field to place a category below a broader category, so that the category inherits the attributes of its parent. To add or update a dynamic category, see [Dynamic Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dynamic-schema.md).

5.  Select the **Dynamic Choices** tab to review the values that a choice set offers.

    A dynamic choice belongs to a choice set that an attribute of type `String` references. The **Order** field determines the sequence of the values, and the **Value** column holds the string that is stored on the change request.

6.  Select the **Dynamic Choice Overrides** tab to review the choices that are overridden for a category or an attribute.

7.  Deactivate the attributes and categories that are not required, and add the ones that are.

    Clear the **Active** check box on a record rather than deleting it, so that the values already recorded on existing change requests remain readable.


## What to do next

Add the **Risk and compliance attributes** and **Risk and compliance category** fields to the Change Request form. For information about recording values in the fields, see [Create a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/t_CreateAChange.md).

**Parent Topic:**[Compliance dynamic schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/compliance-dynamic-schema.md)

**Related topics**  


[Compliance dynamic schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/compliance-dynamic-schema.md)

[Dynamic Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dynamic-schema.md)

