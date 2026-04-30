---
title: Migrate a blueprint to an SFDC-integrated destination
description: Learn how to migrate a CPQ blueprint to a Salesforce-integrated ServiceNow CPQ environment. Recreate configurable products, update Product2 IDs, and verify connections to ensure accurate data mapping and seamless integration between Salesforce and ServiceNow CPQ.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-09-16"
reading_time_minutes: 2
breadcrumb: [Set up blueprints, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Migrate a blueprint to an SFDC-integrated destination

Learn how to migrate a CPQ blueprint to a Salesforce-integrated ServiceNow CPQ environment. Recreate configurable products, update Product2 IDs, and verify connections to ensure accurate data mapping and seamless integration between Salesforce and ServiceNow CPQ.

## Before you begin

If necessary, perform the steps in [Migrate a blueprint from environment to environment](cpq-migrating-env-to-env.md).

If necessary, install the ServiceNow CPQ Managed Package for Salesforce in the destination. For installation instructions, see [Installation and setup guide for environments linked to Salesforce orgs](../concept/installation-and-setup-guide-for-environments-linked-to-salesforce-org.md).

Ensure that the appropriate Salesforce users have access to ServiceNow CPQ.

Role required: \(unknown\)

## Procedure

1.  In your destination SFDC org, recreate the configurable product that is associated with the blueprint on the source SFDC org.

    1.  Note the Product2 ID of this product in the new org.

        To view the Product2 ID, select the product in Salesforce and view the value in the URL.

    2.  In the migration package, open the blueprint.yaml file.

    3.  In the blueprint.yaml file, locate the line that reads `-id: <oldProduct2Id`.

    4.  Replace the Product2 ID from the old org with the the new one that you just created, and save the blueprint.yaml file.

2.  Add all other products from the old org that were referenced in any product rules.

    Don’t forget to create pricebook entries for all your products! These records will be auto-replicated in our ServiceNow CPQ product cache every fifteen minutes. Wait at least fifteen minutes before continuing with the tests described below.

3.  Test the destination by walking through quote creation and configuration, and investigate and resolve any errors that you encounter.

4.  Verify that external or SFDC API calls complete successfully and point to the right external system endpoints.

    See External Connections setup in ServiceNow CPQ Admin.


## What to do next

After the import, configurable product IDs will not be the same as in the original blueprint—they are unique across organizations. To keep the references in rules accurate, if the setting for the ProductId field is set to Product Code, you can create new configurable products as needed and assign them the same product code.

**Related topics**  


[Testing in non-production environments before migration](../concept/cpq-env-to-env-bp-migration-intro.md)

[Migrate a blueprint from environment to environment](cpq-migrating-env-to-env.md)

[Installation and setup guide for environments linked to Salesforce orgs](../concept/installation-and-setup-guide-for-environments-linked-to-salesforce-org.md)

