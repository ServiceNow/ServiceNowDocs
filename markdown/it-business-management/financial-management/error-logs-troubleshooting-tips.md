---
title: Missing money logs factoring tips - Legacy
description: The error type and the possible causes and resolution tips help you to troubleshoot the errors easily.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 28
breadcrumb: [Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Missing money logs factoring tips - Legacy

The error type and the possible causes and resolution tips help you to troubleshoot the errors easily.

**Note:** Missing money analysis is an extended and improved version of the allocation log functionality available prior to Madrid.

<table id="table_i4g_m1p_kx"><thead><tr><th>

Category

</th><th>

Condition

</th><th>

Cause

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Bucket Allocation

</td><td>

Bucket Data Validation: '\{0\}' is excluded: \{1\} but one of its sub-buckets is not: \{2\}

</td><td>

Either parent or child buckets \(\{Test Parent Bucket\}/\{Test Child Bucket\}\) are excluded from allocation

</td><td>

Contact [Customer Service and Support](https://www.servicenow.com/support/contact-support.html)

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is allocated to an invalid segment

</td><td>

Bucket \{Test Parent Bucket\} is with corrupted target segment

</td><td>

Revert and reassign the bucket.1.  Click the error message to highlight the bucket.
2.  To revert the bucket assignment, click the revert bucket assignment \(![Revert bucket assignment icon](../image/RevertBucketAssignmentIcon.png)\) icon.
3.  [Assign a bucket to a segment or an account](../task/t_AssignABucketToASegmentOrAnAccount.md).

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is allocated to a segment \{1\} that is not associated with the current cost model

</td><td>

Bucket \{Test Parent Bucket\} is allocated to a segment that is NOT associated with the current cost model

</td><td>

Revert and reassign the bucket.1.  Click the error message to highlight the bucket.
2.  To revert the bucket assignment, click the revert bucket assignment \(![Revert bucket assignment icon](../image/RevertBucketAssignmentIcon.png)\) icon.
3.  [Assign a bucket to a segment or an account](../task/t_AssignABucketToASegmentOrAnAccount.md).

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is using a weighted allocation method, but no metric is specified

</td><td>

\{Test Bucket\} is using weighted allocation method, but metric is not specified

</td><td>

Revert and reassign the bucket.1.  Click the error message to highlight the bucket.
2.  To revert the bucket assignment, click the revert bucket assignment \(![Revert bucket assignment icon](../image/RevertBucketAssignmentIcon.png)\) icon.
3.  [Assign a bucket to a segment or an account](../task/t_AssignABucketToASegmentOrAnAccount.md).

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is allocated using an invalid allocation metric

</td><td>

\{Test Bucket\} is using weighted allocation method, but an invalid metric is used

</td><td>

Revert and reassign the bucket.1.  Click the error message to highlight the bucket.
2.  To revert the bucket assignment, click the revert bucket assignment \(![Revert bucket assignment icon](../image/RevertBucketAssignmentIcon.png)\) icon.
3.  [Assign a bucket to a segment or an account](../task/t_AssignABucketToASegmentOrAnAccount.md).

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is allocated to an unspecified account

</td><td>

\{Test Bucket\} is allocated to an unspecified account

</td><td>

Revert and reassign the bucket.1.  Click the error message to highlight the bucket.
2.  To revert the bucket assignment, click the revert bucket assignment \(![Revert bucket assignment icon](../image/RevertBucketAssignmentIcon.png)\) icon.
3.  [Assign a bucket to a segment or an account](../task/t_AssignABucketToASegmentOrAnAccount.md).

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is allocated to an invalid account

</td><td>

\{Test Bucket\} is allocated to an invalid account

</td><td>

Revert and reassign the bucket.1.  Click the error message to highlight the bucket.
2.  To revert the bucket assignment, click the revert bucket assignment \(![Revert bucket assignment icon](../image/RevertBucketAssignmentIcon.png)\) icon.
3.  [Assign a bucket to a segment or an account](../task/t_AssignABucketToASegmentOrAnAccount.md).

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is missing mandatory manual allocation information

</td><td>

In the \{Test Bucket\} allocation, one of the manually allocated lines has missing information \(Transaction Account or Transaction Segment or Percentage allocation\)

</td><td>

Fill in the missing mandatory information such as the transaction account, transaction segment, percentage allocation.1.  Click the link to navigate to the Bucket Allocation Account form.
2.  Enter the missing mandatory information such as the transaction **Segment**, transaction **Account**, and the **Percentage** in the respective fields.
3.  Click **Update**.

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is manually allocated to an invalid segment: '\{1\}'

</td><td>

\{Test Bucket\} is manually allocated and one of the allocated lines has an invalid segment \{Test Segment\}

</td><td>

Correct the segment information in the bucket allocation account.1.  Click the link to navigate to the Bucket Allocation Account form.
2.  Select the segment from the **Segment** choice list.
3.  Click **Update**.

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is manually allocated to an invalid account \{1\} in the segment \{2\}. \{3\}% of amount is lost

</td><td>

\{Test Bucket\} is manually allocated to an invalid account \{Test Account\} in the segment \{Test Segment\}. \{Amount\}% of amount may be lost

</td><td>

Correct the account information in the bucket allocation account.1.  Click the link to navigate to the Bucket Allocation Account page.
2.  Select the account from the **Account** choice list.
3.  Click **Update**.

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' is manually allocated with a missing or invalid percentage value

</td><td>

\{Test Bucket\} is manually allocated with a missing or invalid percentage value

</td><td>

Correct the percentage in the bucket allocation account.1.  Click the link to navigate to the Bucket Allocation Account page.
2.  Enter correct percentage in the **Percentage** field.
3.  Click **Update**.

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}':- sum of the manual percentages is \{1\}% which is more than 100%

</td><td>

In the \{Test Bucket\} manual allocation, sum of the allocation percentages is 120%

</td><td>

Correct the allocation percentages in the bucket allocation accounts.1.  Click the link to navigate to the Bucket Allocation Accounts list.
2.  Enter correct percentages in the **Percentage** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}':- sum of the manual percentages is \{1\}% which is less than 100%

</td><td>

In the \{Test Bucket\} manual allocation, sum of the allocation percentages is 70%

</td><td>

Correct the allocation percentages in the bucket allocation accounts.1.  Click the link to navigate to the Bucket Allocation Accounts list.
2.  Enter correct percentages in the **Percentage** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Allocation: '\{0\}' manual allocation was chosen, but no accounts were specified

</td><td>

In the \{Test Bucket\} manual allocation, accounts have not been specified.

</td><td>

Revert and reassign the bucket. 1.  Click the error message to highlight the bucket.
2.  To revert the bucket assignment, click the revert bucket assignment \(![Revert bucket assignment icon](../image/RevertBucketAssignmentIcon.png)\) icon
3.  [Assign a bucket to a segment or an account](../task/t_AssignABucketToASegmentOrAnAccount.md).

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Split for '\{0\}': sum of the split percentages is \{1\} which is less than 100

</td><td>

Bucket Split for \{Test Bucket\}: Sum of the split percentages is 70%

</td><td>

Contact [Customer Service and Support](https://www.servicenow.com/support/contact-support.html)

</td></tr><tr><td>

Bucket Allocation

</td><td>

Bucket Split for '\{0\}': sum of the split percentages is \{1\} which is more than 100

</td><td>

Bucket split for \{Test Bucket\}: Sum of the split percentages is 120%

</td><td>

Contact [Customer Service and Support](https://www.servicenow.com/support/contact-support.html)

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': target segment is not in Hierarchy: \{1\}

</td><td>

The rollup of \{Test Segment\} segment has a corrupted target segment, which is not in the hierarchy.

</td><td>

Redefine the rollup for the segment.1.  Click the error message to highlight the segment.
2.  Click the segment name.
3.  Select the right segment from the choice list in the segment rollup pop-up.
4.  Select the **Rollup Method** from the choice list.
5.  Click **Save Changes**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': target segment has not been specified: \{1\}

</td><td>

The rollup of \{Test Segment\} segment has a corrupted target segment.

</td><td>

Redefine the rollup for the segment.1.  Click the error message to highlight the segment.
2.  Click the segment name.
3.  Select the right segment from the choice list in the segment rollup pop-up.
4.  Select the **Rollup Method** from the choice list.
5.  Click **Save Changes**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': target segment has not been specified: \{1\}

</td><td>

The rollup of \{Test Segment\} segment has a corrupted target segment.

</td><td>

Redefine the rollup for the segment.1.  Click the error message to highlight the segment.
2.  Click the segment name.
3.  Select the right segment from the choice list in the segment rollup pop-up.
4.  Select the **Rollup Method** from the choice list.
5.  Click **Save Changes**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': target segment is not valid: \{1\}

</td><td>

The rollup of \{Test Segment\} segment has a corrupted target segment.

</td><td>

Redefine the rollup for the segment.1.  Click the error message to highlight the segment.
2.  Click the segment name.
3.  Select the right segment from the choice list in the segment rollup pop-up.
4.  Select the **Rollup Method** from the choice list.
5.  Click **Save Changes**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': weighted rollup is chosen, but no metric is specified

</td><td>

The rollup of \{Test Segment\} segment has a corrupted metric.

</td><td>

Redefine the rollup for the segment.1.  Click the error message to highlight the segment.
2.  Click the segment name.
3.  Select the right segment from the choice list in the segment rollup pop-up.
4.  Select **Weighted** from the **Rollup Method** choice list.
5.  Click **Save Changes**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}' rollup is using an invalid metric: \{1\}

</td><td>

The rollup of \{Test Segment\} segment has a corrupted metric.

</td><td>

Redefine the rollup for the segment.1.  Click the error message to highlight the segment.
2.  Click the segment name.
3.  Select the right segment from the choice list in the segment rollup pop-up.
4.  Select **Weighted** from the **Rollup Method** choice list.
5.  Click **Save Changes**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': rollup script contains syntax errors

</td><td>

The rollup script defined for \{Test Segment\} segment has syntax errors.

</td><td>

The rollup script must be syntactically corrected on the Segment Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': \{1\} argument is missing in rollup of script for target Account \{2\}

</td><td>

\{Test Segment\}: \{Test Argument\} is missing in the rollup script for target account \{Test Account\}

</td><td>

The rollup script must be syntactically corrected.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': To transaction Segment is given empty/null for Scripted Rollup for to Account \{1\}

</td><td>

The rollup script defined for \{Test Segment\} segment has an invalid JSON return. One of the rollup values in JSON is Null.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script in the Cost Allocation Rollup form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': To transaction Segment: \{1\} is invalid for Scripted Rollup for to Account \{1\}

</td><td>

The rollup script defined for \{Test Segment\} segment has an invalid JSON return. One of the rollup values in JSON is invalid.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script in the Cost Allocation Rollup form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': To transaction Segment: \{1\} is not in hierarchy for Scripted Rollup for to Account \{2\}

</td><td>

The rollup script defined for \{Test Segment\} segment has an invalid JSON return. One of the rollup values in JSON is not in the hierarchy.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script in the Cost Allocation Rollup form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': To transaction Account \(\{1\}\) of Segment \(\{2\}\) does not exist for Scripted Rollup

</td><td>

The rollup script defined for \{Test Segment\} segment has an invalid JSON return. One of the rollup values \(Account\) in JSON does not exist.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script in the Cost Allocation Rollup form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': To transaction Account is null for Segment \(\{1\}\) does not exist for Scripted Rollup

</td><td>

The rollup script defined for \{Test Segment\} segment has an invalid JSON return. One of the rollup values \(Account\) in JSON is Null.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script in the Cost Allocation Rollup form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}': To transaction Account: \{1\} \(\{2\}\) is invalid for Scripted Rollup for to Account \{3\}

</td><td>

The rollup script defined for \{Test Segment\} segment has an invalid JSON return. One of the rollup values \(Account\) in JSON is invalid.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script in the Cost Allocation Rollup form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}' rollup is divided by no/invalid percent value for Scripted Rollup for to Account \{1\}

</td><td>

The rollup script defined for \{Test Segment\} segment has an invalid JSON return. One of the rollup percentage values is invalid.

</td><td>

The rollup script returns a JSON variable that must be corrected to sum up to 100%. Correct the script in the Cost Allocation Rollup form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}' scripted rollup is divided by percent \{1\}% which is more than 100%

</td><td>

The rollup script defined for \{Test Segment\} segment has an invalid JSON return. The sum of the rollup amount is 120%

</td><td>

The rollup script returns a JSON variable that must be corrected to sum up to 100%. Correct the script in the Cost Allocation Rollup form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Segment Rollup

</td><td>

Segment Rollup: '\{0\}' scripted rollup is divided by percent \{1\}% which is less than 100%

</td><td>

The rollup script defined for \{Test Segment\} segment has an invalid JSON return. The sum of the rollup amount is 70%

</td><td>

The rollup script returns a JSON variable that must be corrected to sum up to 100%. Correct the script in the Cost Allocation Rollup form.1.  Click the link to navigate to the Cost Allocation Rollup form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': target segment has not been specified: \{1\}

</td><td>

The rollup of '100 South Charles Street, Baltimore, MD' account has a corrupted target segment.

</td><td>

Redefine the rollup for the account.1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Delete the existing corrupt target segment by clicking the actions \(![Delete icon](../image/Delete_icon.png)\) icon in the account rollup pop-up.
4.  Click **Add Rollup** button and select the target segment in the **To Segment** choice list.
5.  Select the **Rollup Method** from the choice list.
6.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': target segment is not valid: \{1\}

</td><td>

The rollup of '100 South Charles Street, Baltimore, MD' account has a corrupted target segment.

</td><td>

Redefine the rollup for the account.1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Delete the existing corrupt target segment by clicking the actions \(![Delete icon](../image/Delete_icon.png)\) icon in the account rollup pop-up.
4.  Click **Add Rollup** button and select the target segment in the **To Segment** choice list
5.  Select the **Rollup Method** from the choice list.
6.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': target segment is not in Hierarchy: \{1\}

</td><td>

The rollup of '100 South Charles Street, Baltimore, MD' account has a target segment that is not in the hierarchy.

</td><td>

Redefine the rollup for the account.1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Delete the existing corrupt target segment by clicking the actions \(![Delete icon](../image/Delete_icon.png)\) icon in the account rollup pop-up.
4.  Click **Add Rollup** button and select the target segment that is in the hierarchy in the **To Segment** choice list.
5.  Select the **Rollup Method** from the choice list.
6.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': target segment is not in Hierarchy: \{1\}

</td><td>

The rollup of '100 South Charles Street, Baltimore, MD' account has a corrupted target account

</td><td>

Redefine the rollup for the account.1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Delete the existing corrupt target segment by clicking the actions \(![Delete icon](../image/Delete_icon.png)\) icon in the account rollup pop-up.
4.  Click **Add Rollup** button and select the target segment in the **To Segment** choice list.
5.  Select the target account in the **To Account** choice list.
6.  Select the **Rollup Method** from the choice list.
7.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': To transaction Account: \{1\} \(\{2\}\) is invalid

</td><td>

The rollup of '101 Broadway East, Seattle, WA' account rolls up to an invalid account.

</td><td>

Redefine the rollup for the account.1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Delete the existing corrupt target segment by clicking the actions \(![Delete icon](../image/Delete_icon.png)\) icon in the account rollup pop-up.
4.  Click **Add Rollup** button and select the target segment in the **To Segment** choice list.
5.  Select a valid account in the **To Account** choice list.
6.  Select the **Rollup Method** from the choice list.
7.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': weighted rollup is chosen, but no metric is specified

</td><td>

The rollup of 'Development' account has a corrupt metric.

</td><td>

Redefine the rollup for the account.1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Delete the existing target segment by clicking the actions \(![Delete icon](../image/Delete_icon.png)\) icon in the account rollup pop-up.
4.  Click **Add Rollup** button and select the target segment in the **To Segment** choice list.
5.  Select a valid account in the **To Account** choice list.
6.  Select the **Weighted** metric in the **Rollup Method** choice list.
7.  Select a valid metric in the **Select Metric** choice list.
8.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': weighted rollup is chosen, but no metric is specified

</td><td>

Account Rollup: The rollup of 'Development' account has a corrupt metric.

</td><td>

Redefine the rollup for the account.1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Delete the existing target segment by clicking the actions \(![Delete icon](../image/Delete_icon.png)\) icon in the account rollup pop-up.
4.  Click **Add Rollup** button and select the target segment in the **To Segment** choice list.
5.  Select a valid account in the **To Account** choice list.
6.  Select the **Weighted** metric in the **Rollup Method** choice list.
7.  Select a valid metric in the **Select Metric** choice list.
8.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' is manually divided by a missing or invalid percentage value

</td><td>

The sum rollup percentage of 'HR' is 70%.

</td><td>

Redefine the rollup to sum up to 100%1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' - sum of the manual percentage is \{1\}% which is more than 100%

</td><td>

The sum rollup percentage of 'HR' is 70%.

</td><td>

Redefine the rollup to sum up to 100%1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' - sum of the manual percentage is \{1\}% which is less than 100%

</td><td>

The sum rollup percentage of 'HR' is 70%.

</td><td>

Redefine the rollup to sum up to 100%1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' is equally divided by a missing or invalid percentage value

</td><td>

'\{0\}' rollup override is equally divided by no/invalid percent value.

</td><td>

Redefine the rollup to sum up to 100%1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' is equally divided by percent \{1\}%, which is more than 100%

</td><td>

The rollup of '125 West South Street, Indianapolis, IN' account is more than 100% and may lead to unaccountable amounts.

</td><td>

Redefine the rollup to sum up to 100% on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' is equally divided by percent \{1\}% which is less than 100%

</td><td>

The rollup of '125 West South Street, Indianapolis, IN' account is more than 100% and may lead to unaccountable amounts.

</td><td>

Redefine the rollup to sum up to 100% on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': rollup script contains syntax errors

</td><td>

The rollup script defined for the Facilitate Connectivity account has syntax errors. 

</td><td>

The rollup script must be syntactically corrected on the account rollup override form.1.  Click the link to navigate to the Cost Allocation Rollup Override form.
2.  Correct the syntax of the script in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': To transaction Segment \{1\} is given empty/null for Scripted Rollup Override for to Account \{2\}

</td><td>

The rollup script defined for the Facilitate Connectivity account has an invalid JSON return. One of the rollup values in JSON is null.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Override form.
2.  Correct the rollup value in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': To transaction Segment: \{1\} is invalid for Scripted Rollup Override for to Account \{2\}

</td><td>

The rollup script defined for the Facilitate Connectivity account has an invalid JSON return. One of the rollup values is Test Account, which is not a valid Business Unit. 

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Override form.
2.  Enter a valid rollupValue in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': To transaction Segment: \{1\} is not in the hierarchy for Scripted Rollup Override for to Account \{2\}

</td><td>

The rollup script defined for the Facilitate Connectivity account has an invalid JSON return. One of the rollupToSegment is Test Segment, which is not in the hierarchy.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollupToSegment. Correct the script on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Override form.
2.  Enter a valid rollupToSegment in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': To transaction Account \(\{1\}\) of Segment \(\{2\}\) is given empty/null for Scripted Rollup Override

</td><td>

The rollup script defined for the Facilitate Connectivity' account has an invalid JSON return. One of the rollup values is given empty/Null.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Override form.
2.  Enter a valid rollupValue in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': To transaction Account is null for Segment \(\{1\}\) for Scripted Rollup Override

</td><td>

The rollup script defined for the Facilitate Connectivity account has an invalid JSON return. One of the rollup values is given empty/Null.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Override form.
2.  Enter a valid rollupValue in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}': To transaction Account: \{1\} \(\{2\}\) is invalid for Scripted Rollup Override

</td><td>

Script returns invalid JSON. One of the rollup values is BlackBerry, which is not a valid Business Unit.

</td><td>

The rollup script returns a JSON variable that must be corrected for a valid rollup value. Correct the script on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Override form.
2.  Enter a valid rollupValue in the **Script** field.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' rollup override is divided with no/invalid percent value for Scripted Rollup Override for to Account \{1\}

</td><td>

One of the percentage values, rollup amount, is given Null or invalid value for rollup value 'test account'.

</td><td>

Correct the rollup amount in the script on the Account Rollup Override form.Correct the script on the Account Rollup Override form.

 1.  Click the link to navigate to the Cost Allocation Rollup Override form.
2.  Correct the rollupAmount in the script.
3.  Enter a valid percentage value in the **Script** field.
4.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' rollup override is divided with no/invalid percent value for Scripted Rollup Override for to Account \{1\}

</td><td>

One of the percentage values is given Null or invalid for a missing rollup argument or rollup value.

</td><td>

Correct the rollup amount in the script on the Account Rollup Override form.Correct the script on the Account Rollup Override form.

 1.  Click the link to navigate to the Cost Allocation Rollup Override form.
2.  Correct the rollupAmount in the script.
3.  Enter a valid percentage value in the **Script** field.
4.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' scripted rollup is divided by percent \{1\}% which is more than 100%

</td><td>

The rollup script defined for the Facilitate Connectivity account has an invalid JSON return. The sum of the rollupAmount is 120%.

</td><td>

The rollup script returns a JSON variable that must be corrected to sum up to 100%. Correct the script on the Account Rollup Override list.1.  Click the link to navigate to the Cost Allocation Rollup list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' scripted rollup is divided by percent \{1\}% which is less than 100%

</td><td>

The rollup script defined for the Facilitate Connectivity account has an invalid JSON return. The sum of the rollupAmount is 70%

</td><td>

The rollup script returns a JSON variable that must be corrected to sum up to 100%. Correct the script on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click **Update**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup with invalid bucket

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup with invalid bucket

</td><td>

Redefine the bucket rollup for the account.1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Click the **Bucket Rollups** tab.
4.  Delete the existing invalid bucket record by clicking the delete \(![Delete icon](../image/Delete_icon.png)\) icon.
5.  Click **Add Bucket Rollup**.
6.  Select the bucket from the **Bucket** choice list in the bucket rollup pop-up.
7.  Select the **Rollup Method** from the choice list.

See [View accounts that roll up to an account](../task/t_ViewAccountsThatRollUp.md) for more information.

8.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup where bucket has no parent

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup where the bucket has no parent

</td><td>

Contact [Customer Service and Support](https://www.servicenow.com/support/contact-support.html).

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup where bucket is not in the current cost model

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup where the bucket is not in the current cost model

</td><td>

Redefine the bucket rollup for the account.1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Click the **Bucket Rollups** tab.
4.  Delete the existing bucket record by clicking the delete \(![Delete icon](../image/Delete_icon.png)\) icon.
5.  Click **Add Bucket Rollup**.
6.  Select a bucket that is in the current cost model from the **Bucket** choice list in the bucket rollup pop-up.
7.  Select the **Rollup Method** from the choice list.

See [View accounts that roll up to an account](../task/t_ViewAccountsThatRollUp.md) for more information.

8.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup where bucket is not at the lowest split level

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup where the bucket is not at the lowest split level

</td><td>

Redefine the bucket rollup for the account1.  Click the error message to highlight the account.
2.  Click the account name.
3.  Click the **Bucket Rollups** tab.
4.  Delete the existing bucket record by clicking the delete \(![Delete icon](../image/Delete_icon.png)\) icon.
5.  Click **Add Bucket Rollup**.
6.  Select a bucket that is at the lowest split level from the **Bucket** choice list in the bucket rollup pop-up.
7.  Select the **Rollup Method** from the choice list.

See [View accounts that roll up to an account](../task/t_ViewAccountsThatRollUp.md) for more information.

8.  Click **Save Changes**.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup divided manually for bucket '\{1\}' has a missing or invalid percentage value

</td><td>

Account '\{0\}' rollup override is manually divided with no/invalid percent value.

</td><td>

Redefine the rollup to sum up to 100%.1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup divided manually for bucket '\{1\}' with percent \{2\}% which is more than 100%

</td><td>

The sum rollup percentage of 'HR' is 70%.

</td><td>

Redefine the rollup to sum up to 100%.1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup divided manually for bucket '\{1\}' with percent \{2\}% which is less than 100%

</td><td>

The sum rollup percentage of 'HR' is 70%.

</td><td>

Redefine the rollup to sum up to 100%.1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup divided equally for bucket '\{1\}' with a missing or invalid percentage value

</td><td>

'\{0\}' rollup override is equally divided with no/invalid percent value

</td><td>

Redefine the rollup to sum up to 100%.1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup divided equally for bucket '\{1\}' with percent \{2\}% which is more than 100%

</td><td>

The rollup of '125 West South Street, Indianapolis, IN' account is more than 100% and may lead to unaccountable amounts.

</td><td>

Redefine the rollup to sum up to 100% on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr><tr><td>

Account Rollup

</td><td>

Account Rollup: '\{0\}' has bucket-based rollup divided equally for bucket '\{1\}' with percent \{2\}% which is less than 100%

</td><td>

The rollup of '125 West South Street, Indianapolis, IN' account is less than 100% and may lead to unaccountable amounts.

</td><td>

Redefine the rollup to sum up to 100% on the Account Rollup Override form.1.  Click the link to navigate to the Cost Allocation Rollup Overrides list.
2.  Enter percentage for each record so that the percentages of all records sum up to 100% in the **Percent** column.
3.  Click the save \(![Save icon](../../application-portfolio-management/image/SaveIcon.png)\) icon or press Enter after each entry.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Management workbench - Legacy](../concept/c_TheITFinanceWorkbench.md)

**Related topics**  


[The Data Definition stage - Legacy](../concept/c_TheDataDefinitionStage.md)

[The Data Cleansing stage - Legacy](../concept/c_TheDataCleansingStage.md)

[The Bucketing stage - Legacy](../concept/c_TheDataBucketingStage.md)

[Allocation Setup stage - Legacy](../concept/c_TheAllocationSetupStage.md)

[The Allocation Review stage - Legacy](../concept/c_TheAllocationReviewStage.md)

[The Cost Models tab - Legacy](../concept/c_TheCostModelsTab.md)

[The Configuration tab - Legacy](../concept/c_TheConfigurationTab.md)

