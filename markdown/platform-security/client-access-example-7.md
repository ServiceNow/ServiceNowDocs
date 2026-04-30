---
title: Test the end-to-end client-side encrypted secrets integration
description: Test your integration, and review the execution details to confirm your configuration is working.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring client accessible secrets, Secrets Management, Platform Security]
---

# Test the end-to-end client-side encrypted secrets integration

Test your integration, and review the execution details to confirm your configuration is working.

## Before you begin

Role required: admin, KMF\_admin, sn\_secrets.secret\_manager, and sn\_kmf.cryptographic\_manager

## Procedure

1.  In Workflow Studio select the **Test** button in the top-right corner of the screen.

    ![Test button in flow designer](../images/client-side-13.png)

2.  In the **Test Action** window, select **Run Test**.

3.  Select **Your test has finished running. View the Action execution details.**

4.  Refresh your screen until you see **Test Run – Completed** in the top-right side of the screen.

5.  Select the **Steps** arrow at the bottom left of the screen.

6.  Scroll down until you see a **Step Output Data** heading with the following success message:

    ```
    {"Step Status";{"code";0,"message";"Success"}}
    ```

7.  After seeing this message in Workflow Studio, verify that your text file has been created in your local system.


**Parent Topic:**[Configuring client accessible secrets](../concept/client-access-secret-landing.md)

