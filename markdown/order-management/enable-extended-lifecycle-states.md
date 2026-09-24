---
title: Enable extended life cycle states for product offerings
description: Turn on the In Test and Staged life cycle states for product offerings and product, service, and resource specifications, and optionally preview pre-publish records before they're published.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/enable-extended-lifecycle-states.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Validating product offerings, Specifications and product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Enable extended life cycle states for product offerings

Turn on the In Test and Staged life cycle states for product offerings and product, service, and resource specifications, and optionally preview pre-publish records before they're published.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin

## About this task

Turning on the sn\_prd\_pm.enable\_product\_lifecycle\_prepublish\_visibility property has no effect unless the sn\_prd\_pm.enable\_extended\_product\_lifecycle property is also on.

## Procedure

1.  Navigate to **All** and enter `sys_properties.LIST` in the navigation filter.

2.  Enable the extended states between Draft and Published.

    1.  In the Name field, search and select the **sn\_prd\_pm.enable\_extended\_product\_lifecycle** property.

    2.  Activate the system property by changing the value of the **Value** field to `true`.

        This adds the In Test and Staged states between Draft and Published for product offerings and specifications.

    3.  Select **Update**.

3.  Enable preview of the In Test and Staged entities in test or pre-production environments.

    1.  In the Name field, search and select the **sn\_prd\_pm.enable\_product\_lifecycle\_prepublish\_visibility** property.

    2.  Activate the system property by changing the value of the **Value** field to `true`.

        The sn\_prd\_pm.enable\_product\_lifecycle\_prepublish\_visibility property is turned off in production environment.

    3.  Select **Update**.


## Result

Product offerings and specifications can now move through Draft, In Test, Staged, and Published states. The **Return to Draft** button becomes available on the Product Offering, Resource, Service, and Product Specification pages, used for changing an In Test record to Draft for editing.

## What to do next

[36e0738cf8938e71ff603b1a07014fedcf33c1e8.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/move-offering-spec-states.md)

**Parent Topic:**[Validating product offerings before publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md)

**Related topics**  


[b03a1337caec0f2c07d23b948e7198add0b33a29.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/channel-specific-availability.md)

