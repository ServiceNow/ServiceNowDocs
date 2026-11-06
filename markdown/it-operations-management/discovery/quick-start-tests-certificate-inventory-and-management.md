---
title: Quick start tests for Certificate Inventory and Management
description: Validate that Certificate Inventory and Management still works after you install the application or make a configuration change such as applying an upgrade. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/quick-start-tests-certificate-inventory-and-management.html
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [Reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Quick start tests for Certificate Inventory and Management

Validate that Certificate Inventory and Management still works after you install the application or make a configuration change such as applying an upgrade. Copy and customize these quick start tests to pass when using your instance-specific data.

The quick start tests for Certificate Inventory and Management validate certificate discovery for the supported certificate authorities, URL-based certificate discovery, new certificate requests, and the renewal of expired certificates. Run them as a sanity check after you install the application, to confirm that these features work on your instance.

The tests are inactive when the application is installed. Enable the Automated Test Framework test execution properties such as Test/Test Suite Properties, Test Debugging Properties, and Screenshot Properties before you run them. Run the tests only on development, test, and other non-production instances.

To run a test, navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**, open the test that you want, copy it, enter the parameter values for your instance, and then run the test using the **Run Test** button. Certificate Inventory and Management doesn't provide a test suite, so copy and run each test individually.

The certificate authority discovery tests require a MID Server, a credential alias for the authority, and the authority's URL.

|Test|Description|
|----|-----------|
|Certificate Discovery|Certificate discovery for GoDaddy, Entrust, Digicert, and Sectigo. Discovery brings the certificates and persists them in cmdb\_ci\_certificate table. This test validates the certificates and CIs in the cmdb\_ci\_certificate tables.|

**Parent Topic:**[Certificate Inventory and Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/cert-invt-mgmt-references.md)

**Related topics**  


[Quick start tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/quick-start-tests.md)

