---
title: Migrate a blueprint to an SFDC-integrated destination
description: Migrate a CPQ blueprint to a Salesforce-integrated CPQ environment. Recreate configurable products, update Product2 IDs, and verify connections for accurate data mapping and integration between Salesforce and CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-migrating-to-sfdc.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Migrate a blueprint to an SFDC-integrated destination

Migrate a CPQ blueprint to a Salesforce-integrated CPQ environment. Recreate configurable products, update Product2 IDs, and verify connections for accurate data mapping and integration between Salesforce and CPQ.

## Before you begin

If needed, perform the steps mentioned in the [Migrate a blueprint between environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown) topic.in .

If needed, install the CPQ Managed Package for Salesforce in the destination. For installation instructions, see [Installation and setup guide for environments linked to Salesforce orgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

Confirm that the appropriate Salesforce users have access to CPQ.

Role required: admin

## Procedure

1.  In your destination SFDC org, recreate the configurable product that is associated with the blueprint on the source SFDC org.

    1.  Note the Product2 ID of this product in the new org.

        To view the Product2 ID, select the product in Salesforce and view the value in the URL.

    2.  In the migration package, open the blueprint.yaml file.

    3.  In the blueprint.yaml file, locate the line that reads `-id: <oldProduct2Id`.

    4.  Replace the Product2 ID from the old org with the new one that you just created, and save the blueprint.yaml file.

2.  Add all other products from the old org that were referenced in any product rules.

    You must create pricebook entries for all your products! These records will be auto-replicated in our CPQ product cache every fifteen minutes. Wait at least fifteen minutes before continuing with the tests described in the following steps.

3.  Test the destination by walking through quote creation and configuration.

4.  Confirm that external or SFDC API calls complete successfully and point to the right external system endpoints.

    See External Connections setup in CPQ Admin.


## What to do next

After the import, configurable product IDs will not be the same as in the original blueprint. They are unique across organizations. To keep the references in rules accurate, create configurable products as needed and assign them the same product code if the ProductId field is set to Product Code.

**Related topics**  


[Testing in non-production environments before migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-env-to-env-bp-migration-intro.md)

[Migrate a blueprint between environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Installation and setup guide for environments linked to Salesforce orgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

