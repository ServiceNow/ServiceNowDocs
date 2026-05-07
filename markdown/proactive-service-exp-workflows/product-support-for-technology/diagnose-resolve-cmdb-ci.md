---
title: Run diagnostics tests for a CI or a service
description: As a customer service agent, review, diagnose, resolve, and close a service case for the service-related issue experienced by the customer.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Proactive Service Experience Workflow, Use, Product Support for Technology]
---

# Run diagnostics tests for a CI or a service

As a customer service agent, review, diagnose, resolve, and close a service case for the service-related issue experienced by the customer.

## Before you begin

Role required: admin

## About this task

This task helps you to understand how to execute relevant preconfigured diagnostics tests for a specific CI or a service, without any incident or case. This helps the agents to test a CI or Service standalone. If any issues are found, resolution shall follow the standard process like incident or case as applicable. This task doesn't enable the agent to create any repair or diagnostic task, but only help to run the required test on the fly without any case or incident.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the List icon.

3.  Navigate to **CMDB** &gt; **Services**.

4.  Open a service that is in the New or Open state.

    ![CMDB services.](../../tmt-spmc/image/diagnose-cmdb-case.png)

5.  Diagnose the service to identify the root-cause of the problem.

    The decision table can be configured to control the visibility of the Diagnose and Run Diagnostics contextual panel tabs. For more information about decision tables, see [Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=australia&pubname=australia-application-development&ft:locale=en-US).

    1.  To generate the test results, select **Run diagnostics** from the contextual panel.

    2.  In the run diagnostics panel, select **CI/Service** from the drop-down list.

        The drop-down list shows the current product inventory and all the child inventories.

        To set up test definitions, see [Setting up test definitions](https://www.servicenow.com/docs/access?context=settingup-test-specifications&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).

    3.  Expand the cards in **Available test suite**.

        To set up test group, see [Setting up a test group](https://www.servicenow.com/docs/access?context=setting-test-group&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).

    4.  In the manual test, select single/multiple tests.

        In the automated test, selection of test isn’t available. The subflow that is configured for the test group would be invoked.

    5.  Select **Configure**.

    6.  In the Configure tests, fill the test required characteristics form to activate the **Run test** button.

    7.  In the test, select an option either to **Run test** now or to **Schedule test** for later.

    8.  Select **Run test**.

    9.  In the diagnose tab, expand the **Test results** and review the results of the tests conducted in the previous step, checking whether each test is passed or failed.

        The maximum number of rows to the group is limited to 20 rows. To configure the maximum number of rows more than 20 rows to the group, see [Presentational List Usage](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-list/usage).

    10. Select the **View Details** ![](../../../reuse/icons/product-icons/open-link-right-fill-24.svg) icon for a specific test result to review its details.

    11. Select the **Rerun test** ![](../../../reuse/icons/product-icons/arrow-clockwise-outline-24.svg) icon for a specific test result to run it again.

    12. Select **Continue**.

6.  Review the details of the service in the **Details** tab.

7.  View the service-related records in the **Related records** tab.


**Parent Topic:**[Using Proactive Service Experience Workflows](../concept/use-assurance-workflows.md)

