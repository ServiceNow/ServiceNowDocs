---
title: Create a parent multi-store case in Retail Task Management Core
description: Create a parent multi-store case for your retail organization using Retail Task Management Core.
locale: en-US
release: australia
product: \[Legacy\] Retail Task Management
classification: legacy-retail-task-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create multi-store cases, Retail Task Management, Retail]
---

# Create a parent multi-store case in Retail Task Management Core

Create a parent multi-store case for your retail organization using Retail Task Management Core.

## Before you begin

Role required: sn\_retail.support\_agent

**Note:** If the child case creation fails due to platform or instance issues, there’s no retry mechanism in place. As a result, the parent case is marked as **Canceled with error\(s\)**. In this situation, create a parent case from the beginning.

## Procedure

1.  In **CSM/FSM Configurable Workspace**, navigate to **Retail Cases**.

2.  Select **New**.

3.  In the service selector, select the service definition with multi-store case creation capabilities then select **Create case**.

4.  In the multi-store retail case, fill in initial details as needed.

5.  Select **Save**.

    Once the initial case information is filled in and you save the case, the **Affected Retail Stores** tab appears. The **Affected Retail Stores** tab enables you to create child cases for the stores you select.

6.  In the multi-store retail case, navigate to **Affected Retail Stores**.

7.  Select **Add retail stores**.

8.  Select the stores that you want added as child cases using the check box column and select **Add**.

    Only retail stores are available for selection here as multi-store case creation doesn’t include areas, regions, districts, or divisions.

    You can also choose to select all.

9.  Select **Save**.

    **Note:**

    Selecting Save doesn't submit the cases for creation. You can still add, edit, or remove cases until you select the **Submit case.** Then, the parent retail case is submitted, and the child cases creation process begins.

10. Once all child cases are added and reviewed, select **Submit case** to submit the parent case.

    The child cases then begin to generate.

11. Once the case has been submitted, a new related list called **Child cases** appears which will display all child cases created for this parent case after the generation process has completed.

12. Use the Tasks related lists to add any tasks to this parent case.

13. Use the Escalate case or Report Knowledge Gap from the more menu as needed.

14. Once all child cases have been sufficiently closed, use **Close Case** to close the parent case.


