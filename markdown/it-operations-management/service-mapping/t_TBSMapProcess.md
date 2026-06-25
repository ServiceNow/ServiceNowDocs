---
title: Resolve pattern-related mapping errors
description: You can troubleshoot mapping errors caused by patterns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/t\_TBSMapProcess.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Fix errors in individual application service maps, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Resolve pattern-related mapping errors

You can troubleshoot mapping errors caused by patterns.

This video provides an alternative way of troubleshooting pattern-related errors.

## Before you begin

Verify that the mapping error is caused by an inaccurate pattern by checking the discovery message. If the message says "Failed to recognize application", the error is pattern-related.

You need to be familiar with the Pattern Designer module of Service Mapping.

Role required: admin and service\_mapping\_admin

## About this task

If there are configuration items \(CIs\) that Service Mapping could not map correctly, they appear on your service instance map with warning icons \[Omitted image "MapWarningIcon.png"\] Alt text: The warning icon. Typically, mapping errors happen when Service Mapping fails to connect to a CI or fails to recognize it due to an inaccurate pattern.

You can identify problematic steps in your pattern and fix them without reviewing all steps and operations contained in the pattern. It allows you to troubleshoot pattern-related errors quickly and effectively.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Ensure that the map opens in Edit mode displaying discovery messages and errors.

    \[Omitted image "MapEditDiscoveryMessages.png"\] Alt text: Discovery Messages pane

3.  Right-click the CI with the warning icon \(\[Omitted image "MapWarningIcon.png"\] Alt text: The warning icon\) and select **Show discovery log**.

4.  Expand the failed pattern which appears above the result marked red.

    \[Omitted image "DiscLogExpandPattern.png"\] Alt text: A failed pattern appears

5.  Expand the failed section and click the failed step.

    \[Omitted image "DiscLogExpandPatternSection.png"\] Alt text: A pattern section inside the pattern in the Discovery Log window.

6.  Click **Debug**.

7.  Click the first step and wait for Pattern Designer to run it.

    Repeat this action for other steps following the order until you reach the faulty step that causes the error.

    In the example below the port number is 8081 instead of 8080 which causes the problem.

    \[Omitted image "PatDefDebugStepFailure.png"\] Alt text: The debug session fails when Pattern Designer tries to run a faulty step.

8.  Click **OK**.

9.  Fix the pattern attribute that causes the problem.

10. Click **Test**.

11. Verify that Pattern Designer returns a success message.

12. Click **Save**.

13. Click **Activate**.

14. Return to the service instance map which contained the mapping error.

15. Right-click the CI for which the pattern was fixed and select **Resume discovery**.

16. Verify that the CI is discovered and mapped correctly.


**Parent Topic:**[Fix errors in individual application service maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/fix-or-ignore-errors-business-service-map.md)

**Related topics**  


[Fix errors in individual application services using discovery messages]()

[Skip errors to continue discovering an application service]()

