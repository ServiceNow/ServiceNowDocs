---
title: Configure settings for estimated time to resolve values
description: After upgrading, configure some settings to view the Time to Resolve Numeric Value column in the case report for older cases and determine the information that is displayed.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Estimated time to resolve a case, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Configure settings for estimated time to resolve values

After upgrading, configure some settings to view the **Time to Resolve Numeric Value** column in the case report for older cases and determine the information that is displayed.

## Before you begin

You must have a trained default estimated time to resolve a case regression solution. For more information, see [Configure the default estimated resolution time](ettr_configure.md).

Role required: admin

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

