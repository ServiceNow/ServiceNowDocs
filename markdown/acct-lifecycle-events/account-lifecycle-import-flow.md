---
title: Account onboarding data validation flow
description: This section describes how the data is imported from an external file, validated, and published to the target table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data capture and validation, Set up playbook, Account onboarding, Configure, Customer Success Management]
---

# Account onboarding data validation flow

This section describes how the data is imported from an external file, validated, and published to the target table.

The data import flow involves the following steps:

1.  The customer uploads an Excel file as an attachment to the account onboarding data import task.
2.  The data is loaded to the staging table and validated to verify that only the correct data can be published and moved to the target table. Several pre-defined validations are available with the base system. You can create additional validations or use a custom script if necessary. See [Configure data validation using the Data Validation Assist table](../task/account-lifecycle-data-valid-assist.md) for details.
3.  When the validation has been completed, the data is moved to one of the following categories:
4.  -   Ready to publish: The data meets all the validation conditions and can be published.
-   Needs attention: Review the records that are in the **Needs attention** state, resolve the errors, and select **Save**. These updated records are moved into the **Yet to validate** state.

**Parent Topic:**[Data capture and validation](account-lifecycle-use-playbook-data-capture.md)

