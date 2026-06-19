---
title: Data import and validation
description: Use this feature to streamline the migration and onboarding of customer data into the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/customer-success-management/account-lifecycle-data-import-valid.html
release: australia
product: Customer Success Management
classification: customer-success-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Account onboarding, Explore, Customer Success Management]
---

# Data import and validation

Use this feature to streamline the migration and onboarding of customer data into the ServiceNow AI Platform.

The data import option enables you to organize and track tasks required for importing data and verify that the data is complete and accurate. It plays a critical role in onboarding new accounts and facilitating updates to existing ones, helps reduce manual effort, and improves data integrity.

The Data Validation Assist feature streamlines the manual data entry process by verifying that required fields are completed and potential errors are flagged. This option is useful in scenarios where automated or large-scale integrations may not be available or practical.

The data import flow involves the following steps:

1.  The customer uploads an Excel file as an attachment to the account onboarding data import task.
2.  The data is loaded to the staging table and validated to verify that only the correct data can be published and moved to the target table. Several pre-defined validations are available with the base system. You can create additional validations or use a custom script if necessary. See [Configure data validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-data-valid-assist.md) for details.
3.  When the validation has been completed, the data is moved to one of the following categories:
4.  -   Ready to publish: The data meets all the validation conditions and can be published.
-   Needs attention: Review the records that are in the **Needs attention** state, resolve the errors, and select **Save**. These updated records are moved into the **Yet to validate** state.
-   Yet to validate: The record hasn't been validated yet, including records updated from the Needs attention state.

**Parent Topic:**[Account onboarding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-playbook-overview.md)

