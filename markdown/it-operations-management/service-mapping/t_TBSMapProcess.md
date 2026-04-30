---
title: Resolve pattern-related mapping errors
description: You can troubleshoot mapping errors caused by patterns.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Fix errors in individual application service maps, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Resolve pattern-related mapping errors

You can troubleshoot mapping errors caused by patterns.

Service Mapping Part 2 \| Troubleshooting

This video provides an alternative way of troubleshooting pattern-related errors.

## Before you begin

Verify that the mapping error is caused by an inaccurate pattern by checking the discovery message. If the message says "Failed to recognize application", the error is pattern-related.

You need to be familiar with the Pattern Designer module of Service Mapping.

Role required: admin and service\_mapping\_admin

## About this task

If there are configuration items \(CIs\) that Service Mapping could not map correctly, they appear on your service instance map with warning icons ![The warning icon](../image/MapWarningIcon.png). Typically, mapping errors happen when Service Mapping fails to connect to a CI or fails to recognize it due to an inaccurate pattern.

You can identify problematic steps in your pattern and fix them without reviewing all steps and operations contained in the pattern. It allows you to troubleshoot pattern-related errors quickly and effectively.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technical Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Ensure that the map opens in Edit mode displaying discovery messages and errors.

    ![Discovery Messages pane](../image/MapEditDiscoveryMessages.png)

3.  Right-click the CI with the warning icon \(![The warning icon](../image/MapWarningIcon.png)\) and select **Show discovery log**.

4.  Expand the failed pattern which appears above the result marked red.

    ![A failed pattern appears](../image/DiscLogExpandPattern.png)

5.  Expand the failed section and click the failed step.

    ![A pattern section inside the pattern in the Discovery Log window.](../image/DiscLogExpandPatternSection.png)

6.  Click **Debug**.

7.  Click the first step and wait for Pattern Designer to run it.

    Repeat this action for other steps following the order until you reach the faulty step that causes the error.

    In the example below the port number is 8081 instead of 8080 which causes the problem.

    ![The debug session fails when Pattern Designer tries to run a faulty step.](../image/PatDefDebugStepFailure.png)

8.  Click **OK**.

9.  Fix the pattern attribute that causes the problem.

10. Click **Test**.

11. Verify that Pattern Designer returns a success message.

12. Click **Save**.

13. Click **Activate**.

14. Return to the service instance map which contained the mapping error.

15. Right-click the CI for which the pattern was fixed and select **Resume discovery**.

16. Verify that the CI is discovered and mapped correctly.


**Parent Topic:**[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

**Related topics**  


[Fix errors in individual application services using discovery messages](fix-errors-by-discovery-messages.md)

[Skip errors to continue discovering an application service](skip-errors-continue-discovery-individual-services.md)

