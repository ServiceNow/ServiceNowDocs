---
title: Sample ATF tests for Service Catalog in Service Portal
description: Validate the continued functionality of Service Catalog after any configuration change such as an upgrade or after developing an application. All test suites and tests should pass on a default implementation. To validate a custom implementation, copy the automated tests and configure them for your customizations.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Sample ATF tests for Service Catalog in Service Portal

Validate the continued functionality of Service Catalog after any configuration change such as an upgrade or after developing an application. All test suites and tests should pass on a default implementation. To validate a custom implementation, copy the automated tests and configure them for your customizations.

Service Catalog sample tests require activating the Service Catalog - ATF Tests plugin \(com.glideapp.servicecatalog.atf.test\) along with the demo data. To run these tests using a suite, follow the procedure described in [Run an automated test suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-run-suite.md) by selecting the **Service Catalog - ATF Tests** test suite. These sample tests are dependent on the demo data items.

|Test|Description|
|----|-----------|
|Ordering an item with a multi-row variable set \(SP\)|Validate ordering an item in Service Portal that needs data from a multi-row variable set|
|Ordering catalog items using an Order Guide \(SP\)|Validate ordering an item from an order guide in Service Portal|
|Request a catalog item \(SP\)|Validate requesting a catalog in item in Service Portal|
|Search for items, add to cart and checkout \(SP\)|Validate using the cart in Service Portal|
|Submitting requests using a Record Producer \(SP\)|Validate using a record producer in Service Portal|
|Viewing and editing catalog item variables in the Catalog Task page|Validate catalog item variables from a catalog task|
|Viewing and editing catalog item variables in the Requested Item page|Validate catalog item variables from a requested item|
|Add comment on catalog item\(s\) request created by user|Add comments on a ticket page for a requested item or incident|
|Approving requests on different catalog item ordered from end-users|Approving a request for catalog items|
|Catalog item\(s\) ordering from multiple catalogs|Order catalog items from multiple catalogs|
|Filter for recent records from My Request filter|Filter for recent open and closed records from the **My Requests** menu|
|Ordering catalog item\(s\) from saved bundle|Order catalog items from a saved bundle|
|Validate contents of 'My Recent Items'|Validate contents of the My Recent Items widget|
|Validating Regex for Variables|Validate variables using a regular expression|
|Validate Requested For variable flow for Cart Checkout|Validate the Requested For variable flows for cart checkout|
|Validate Requested For variable flow for Order Guide|Validate the Requested For variable flows for an order guide|
|Validate Requested For variable flow with Catalog Item access|Validate the Requested For variable flows based on the catalog item access|

**Parent Topic:**[Service Catalog Reference](../concept/service-catalog-reference.md)

