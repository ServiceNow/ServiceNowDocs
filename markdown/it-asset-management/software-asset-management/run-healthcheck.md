---
title: Run a health check scan for Software Asset Management
description: Run a health check scan on your Software Asset Management configurations and get recommendations on fixing any errors that may exist.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Run a health check scan for Software Asset Management

Run a health check scan on your Software Asset Management configurations and get recommendations on fixing any errors that may exist.

## Before you begin

Role required:

-   sam\_user
-   implementation partners
-   support analyst

## About this task

You can run a health check scan to know the health score for the complete configuration of the Software Asset Management application or for a specific part of the configuration.

## Procedure

1.  Navigate to **Software asset** &gt; **Software Asset Workspace** &gt; **Success portal** &gt; **Health check**.

2.  Select the **Suites check available** widget.

    The Suites page appears listing all available health checks per suite.

3.  Select the suite on which you want to run the health check scan.

    All checks for that particular suite appear in the page along with a short description and the category of each check.

4.  Select **Execute Suite scan** to begin the scan.

    The Execute Suite Scan dialog box appears and shows the progress of the scan. All the checks in that suite get executed across your environment.

5.  Select **Go to results** once the scan is complete.

    All issue records for the health checks are displayed under **Scan Findings** in the Scan Result page.

6.  Select on an issue record to get more details on an error such as detailed description of the error, resolution details.

    You can create tasks and assign the tasks to individuals to take action on the recommendations.

7.  Create tasks and assign the tasks to individuals to take action on the recommendations.

    Once the errors are fixed, you can run the scan again to see improved health scores.


**Parent Topic:**[Configuring Software Asset Workspace](../concept/Config-sam-workspace.md)

