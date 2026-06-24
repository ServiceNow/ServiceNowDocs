---
title: Account onboarding data validation flow
description: This section describes how the data is imported from an external file, validated, and published to the target table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/acct-lifecycle-events/account-lifecycle-import-flow.html
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data capture and validation, Set up the account onboarding playbook, Configuring account onboarding, Account onboarding, Account Lifecycle Events]
---

# Account onboarding data validation flow

This section describes how the data is imported from an external file, validated, and published to the target table.

See the following diagram to view the flow of data from the upload stage to the final stage when it’s published.

\[Omitted image "account-lifecycle-valid-assist.png"\] Alt text: Account onboarding import and validation flow

The data import flow involves the following steps:

1.  The customer uploads an Excel file as an attachment to the account onboarding data import task.
2.  The data is loaded to the staging table and validated to ensure that only the correct data can be published and moved to the target table. Several pre-defined validations are available with the base system. You can create additional validations or use a custom script if required. See [Configure data validation using the Data Validation Assist table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/acct-lifecycle-events/account-lifecycle-data-valid-assist.md) for details.
3.  When the validation has been completed, the data is moved to one of the following categories:
4.  -   Ready to publish: The data meets all the validation conditions and can be published.
-   Needs attention: Review the records that are in the **Needs attention** state, resolve the errors, and select **Save**. These updated records are moved into the **Yet to validate** state.

