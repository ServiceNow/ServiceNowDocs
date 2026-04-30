---
title: Grandfathered and exempted tables
description: Grandfathered and exempted custom tables are treated differently than other custom tables on your instance. Refer to your organization’s ServiceNow contract for additional information.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing custom tables and apps, Subscription Management, Get started, Administer]
---

# Grandfathered and exempted tables

Grandfathered and exempted custom tables are treated differently than other custom tables on your instance. Refer to your organization’s ServiceNow® contract for additional information.

## Grandfathered tables

Depending on your organization’s legacy subscription entitlements and contractual migration, grandfathered tables might be allotted to your production instance. Grandfathered table entitlements enable preservation of your organization's previous custom table entitlements through license migration. This one-time process ensures that custom tables that currently exist in a production instance don't count against your new custom table entitlements.

Grandfathered custom tables can't be transferred, reused, or otherwise classified as another custom table type. If you delete a grandfathered custom table, you can't classify any other custom table as a grandfathered custom table to take its place. Once a custom table has been associated with a grandfathered table subscription, it remains in the Custom Table Inventory even if the table is deleted from the instance.

To view your grandfathered tables, enter `ua_custom_table_inventory.list` in the filter navigator, and then add a filter with the condition **\[Allotment type\] \[is\] \[Grandfather\]**.

If you have a combination of custom tables and grandfathered tables in one application, the grandfathered tables must be mapped to a grandfathered table subscription and the remaining custom tables to one other subscription. Reach out to Customer Service and Support for help mapping a grandfathered table to a grandfather table subscription.

## Grandfathered tables on an instance

Scenario: Your organization purchases three new subscriptions with entitlements for a total of 55 App Engine Starter custom tables \(formerly Bundled Custom Tables\). To ensure your organization doesn't lose the previous custom table entitlements, a grandfather subscription with an entitlement for 25 grandfathered tables is allotted to your instance. This subscription requires the admin to identify and map the existing 25 tables. These subscriptions result in a total custom table entitlement of 80. Once a custom table has been assigned to the grandfather subscription there is no option to revert this.

|Subscription|Number of custom table entitlements|Number of mappable tables|
|------------|-----------------------------------|-------------------------|
|Grandfathered subscription|25|25|
|New Subscription 1|25|25|
|New Subscription 2|25|25|
|New Subscription 3|5|5|

## Exempted tables

Exempted tables are custom tables that do not count towards your subscription entitlements. These tables consist mostly of custom extensions of certain system-related tables, such as sys\_portal\_page and sys\_user\_preference, that you extend for operational improvements in your production instance.

To view a list of exempted tables, enter `ua_exempted_table_inventory.list` in the filter navigator.

The [Custom Table Guide legal schedule](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/custom-table-guide.pdf) provides the complete definition of which tables are considered exempt.

**Note:** Legal schedules are enforced based on when the contract is executed.

To find past versions of the Custom Table Guide, see the [Legal Schedules Custom Table Guide](https://www.servicenow.com/schedules-archived.html).

**Parent Topic:**[Managing custom tables and applications in Subscription Management](../concept/allocating-custom-tables-subscr-apps-v2.md)

