---
title: Allow client errors from step results
description: Allow client errors as you review step results.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Allowed client errors, Building and running automated tests with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Allow client errors from step results

Allow client errors as you review step results.

## Before you begin

Role required: atf\_test\_admin, atf\_test\_designer, or admin

## About this task

You can allow multiple or individual client errors. For each client error, you must decide how to report future instances of the client error. Report level options include:

-   Warning: Test steps containing the allowed client error report a status of `Success with warning(s)`. The error message appears in the test result output, and is recorded in the test logs with the status `Warning`.
-   Ignored: Test steps containing the allowed client error report a status of `Success`. The error is recorded in the test logs with an `Ignored` status.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Test Results**.

2.  Select the test result for a specific test.

    The system displays the Test Result record.

3.  Select the client errors to be allowed.

<table id="choicetable_pd5_3d2_1db"><tbody><tr><td id="d99728e112">

**Specific step result from Step Results related list**

</td><td>

1.  In the Step Results related list, right-click the step result containing client errors you want to allow.
2.  From the context menu, select one of the following options:
    -   **Add all client errors to warning list**: Allow all client errors in this step with a report level of Warning.
    -   **Add all client errors to ignored list**: Allow all client errors in this step with a report level of Ignored.


</td></tr><tr><td id="d99728e142">

**Multiple step results from Step Results related list**

</td><td>

1.  In the Step Results related list, select the check box in the first column for each step result containing client errors you want to allow.
2.  From the **Actions on selected rows** list, select one of the following options.
    -   **Add all client errors to warning list**: Allow all client errors in this step with a report level of Warning.
    -   **Add all client errors to ignored list**: Allow all client errors in this step with a report level of Ignored.


</td></tr><tr><td id="d99728e175">

**Specific step result from Step Result record**

</td><td>

1.  In the Step Results related list, select the Step Result record containing a client error you want to allow.
2.  From the Related links, select one of the following options:
    -   **Add all client errors to warning list**: Allow all client errors in this step with a report level of Warning.
    -   **Add all client errors to ignored list**: Allow all client errors in this step with a report level of Ignored.


</td></tr></tbody>
</table>    The Automated Test Framework allows the selected client errors and displays a status message at the top of the form.


**Parent Topic:**[Allowed client errors](../concept/whitelisted-client-errors.md)

**Related topics**  


[Allowed client errors](../concept/whitelisted-client-errors.md)

