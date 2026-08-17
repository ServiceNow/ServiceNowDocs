---
title: Configure settings for estimated time to resolve values
description: After upgrading, configure some settings to view the Time to Resolve Numeric Value column in the case report for older cases and determine the information that is displayed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ettr-upgrade.html
release: australia
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 1
breadcrumb: [Estimated time to resolve a case, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Configure settings for estimated time to resolve values

After upgrading, configure some settings to view the **Time to Resolve Numeric Value** column in the case report for older cases and determine the information that is displayed.

## Before you begin

You must have a trained default estimated time to resolve a case regression solution. For more information, see [Configure the default estimated resolution time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ettr_configure.md).

Role required: admin

## About this task

**Note:** Support for creating new regression solutions was deprecated in the Washington DC release. You can train and edit any existing solutions, but you can't initiate new ones. The following information is provided for legacy context. For more information see [Create and train a regression solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-regression-solution.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Script**.

2.  Select the **Populate Numeric TTR values** fix script.

3.  Modify the default parameter values.

    -   **LookBackPeriodInMonths**: The number of past months of cases to examine. The default value is 15 months.
    -   **report.setLimit**: The maximum number of records to examine. The default value is 150,000.
4.  Click **Run Fix Script** to populate the estimated time values taken to resolve older cases.

5.  Either run the script on screen or run it in the background.

    -   To display the script running on the screen, click **Proceed**.
    -   To run the script in the background, click **Proceed in Background**.

