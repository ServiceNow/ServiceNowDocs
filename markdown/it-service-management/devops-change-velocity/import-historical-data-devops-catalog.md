---
title: Importing historical data for DevOps tools
description: Use the service catalog to onboard a new app and import historical DevOps data for that app. Enable polling to import data that is mapped to associated plans, repositories and pipelines on a scheduled frequency.Enable polling to import DevOps data on a scheduled frequency to apps that have imported historical data, and are mapped to associated plans, repositories, and pipelines.After you have integrated Azure DevOps with DevOps, you can import up to 90 days of existing Azure DevOps pipeline, repository, and plan data. You can then use DevOps dashboards to view and manage Azure DevOps data.After you have integrated GitLab with DevOps, you can import up to 90 days of existing GitLab pipeline and repository data. You can then use DevOps dashboards to view and manage GitLab data.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Onboarding tools and apps, Manage, DevOps Change Velocity, IT Service Management]
---

# Importing historical data for DevOps tools

Use the service catalog to onboard a new app and import historical DevOps data for that app. Enable polling to import data that is mapped to associated plans, repositories and pipelines on a scheduled frequency.

## Import historical DevOps data for existing tools

You can create an app onboarding request and import historical data for a DevOps tool that you have already on-boarded, using the app onboarding catalog form. Currently, you can import historical data for the last 90 days from current date, and enable polling on a scheduled frequency for the following tools:

-   Jira \(Plan\)
-   GitHub and GitHub Enterprise \(Coding\)
-   Jenkins \(Orchestration\)

**Note:**

-   Ensure that you have created, connected, and discovered the tool you are importing data for.
-   Import requests for Plan tool \(Jira\) are processed first, followed by repository and pipeline import requests.

## Import workflow and retries

On successfully submitting the catalog request from the Self-service catalog, the request is sent for approval following the designated approver flow that you have configured. When the request is approved, an inbound event is created for the app onboarding request. The **Processing details** field of the inbound event record displays the import request ID and status. A single import request creates multiple child import request pages that display in the related list. The import request pages are created based on the following logic for the supported tools:

-   Jira: a page is created for a range of 15 days.
-   GitHub : a page is created for every 100 commits.
-   Jenkins: pages are created per build.

. After import requests are complete processing, the associated Work items, Commits, Branches, Tags, Pipeline executions, Test summaries that you mapped are created and persisted in the system.

On successful import you can view all imported commits in the **DevOps** &gt; **Develop**:

-   Branches
-   Commits
-   Committers
-   Tags
-   Repositories
-   Work Items

for details to confirm successful import for the specified date range.

While processing an import request, if any page errors out, an inbuilt retry mechanism tries processing the page for a set number of times. After all automatic retries, if the page is still in error state, the subsequent or remaining pages in the import request are processed. The overall state of the import request remains in error.

For example, if the Plan import request failed \(after all retries\), we will proceed to process Repository and Pipeline imports. You can configure the retries for the import request from **DevOps** &gt; **Administration** &gt; **Properties** &gt; **Maximum retries per page, while importing**.

-   Specify the count of retries to auto-attempt, in case the import request page fails in the **Maximum retries per page, while importing** field. If after all the automatic retries, page does not succeed, the import request will process the remaining pages. The overall status of the import request reflects as errored.
-   You can manually retry attempting a failed import by clicking the **Retry import** button, on the failed import request page,

**Parent Topic:**[Additional information for onboarding DevOps tools and apps using the Service catalog](onboard-tools-self-service-catalog.md)

## Polling schedule and configuration

Enable polling to import DevOps data on a scheduled frequency to apps that have imported historical data, and are mapped to associated plans, repositories, and pipelines.

After you have onboarded an app and imported the associated DevOps data, you can enable the base system schedule for import requests to be created for the plans, repositories, and pipelines that are tracked and associated to an app. When the import requests complete processing, the associated data is persisted and display against the app. While the base system *DevOpsImportPolling* schedule job is active by default, you must enable polling from the DevOps properties to run the scheduled job.

To enable polling, navigate to **DevOps** &gt; **Administration** &gt; **Properties** &gt; **Enable Import Polling** and select the check box.

Turning this property flag on, enables the base system *DevOpsImportPolling* schedule job. The scheduled job for polling considers either the last successful import or 30 days, whichever is later as the ‘start date’, and the current day's date as the 'end date' for the data import, for all apps that are active and have tracked pipelines. The job looks up the time of the last successful import and creates the subsequent import request accordingly. This logic ensures that the scheduled polling job imports the delta of relevant DevOps data for that app, from the last successful import till date, to a maximum of thirty days.

**Note:** Do not configure a polling frequency that is less than a day or 24 hours.

The default frequency of the job is set to run daily at midnight using the system time zone. To change the frequency of scheduled job you need the ServiceNow ServiceNow AI Platform Administrator \(admin\) role.

Navigate to **System Definition** &gt; **Scheduled Jobs** &gt; **DevOpsImportPolling** and modify the **Run** frequency, **Time zone**, and **Time** field values, as needed. For more information, see [Schedule Jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

**Note:**

-   The scheduled job only applies to active apps. Ensure that the app you are configuring polling for is in active state and the **Track** field is enabled for the relevant pipelines.
-   Consider the following when you're modifying the schedule frequency:
    -   For JIRA the default time zone is based on the time zone of the JIRA server's location.
    -   For Jenkins the default time zone is UTC. For more information see Jenkins [documentation on System Time time zones](https://www.jenkins.io/doc/book/managing/change-system-timezone/).

The schedule jobs that polls to import DevOps data honours the default values for the following DevOps properties related to imports and import requests:

-   Maximum retries per page while importing
-   Maximum number of pages to process at a time for an import request
-   To save payloads as attachments on the Import Request Page record, set the "Value" field to "true". Anything else is considered false.

## Import existing Azure DevOps pipelines, repositories, and plans

After you have integrated Azure DevOps with DevOps, you can import up to 90 days of existing Azure DevOps pipeline, repository, and plan data. You can then use DevOps dashboards to view and manage Azure DevOps data.

### Before you begin

Role required: admin

### About this task

-   You will request the data from the service catalog as a predefined catalog item.
-   Imported test summaries, artifacts, and packages are linked to pipeline executions and not to step executions.
-   SonarQube scan results are not imported.
-   Azure DevOps imposes the following restrictions:
    -   Maximum 20,000 work items can be imported every 15 days.
    -   Maximum 200 run commits can be mapped to any pipeline execution.
    -   Test results for pipeline executions longer than 7 days are not returned.

**Note:** The import process can take some time, hours for very large data sets.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **My Catalogs** and then select **DevOps Onboarding**.

2.  In the **Catalog Items** related list, select **DevOps App Onboarding**.

3.  On the Catalog Item form, select **Try It** to request the data.

    The resulting DevOps App Onboarding form enables you to specify the catalog item to order. In this case, the "app" to order is your Azure DevOps instance.

    ![Specify the instance on the Onboarding form](../image/dev-ops-app-onboarding-form.png)

4.  Select the Select in list icon \(![Applications icon](../image/icon-view-list.png)\) on the **App** field and then select your instance of Azure DevOps.

    Now that you have specified the instance, you will specify date range and sources of data to import.

5.  Repeat the following procedure for each pipeline, repository, and plan that you want to import:

    1.  Select the Select in list icon \(![Applications icon](../image/icon-view-list.png)\) on the appropriate **Onboarding** field to select the item to import.

        You can select multiple items.

    2.  Specify the range of dates for the data in the **Import From** and **Import To** fields.

6.  Select **Order Now**.

    Your request appears on the Order Status page.

7.  Select the request number so you or another user with the admin role can approve the request.

    ![Select the request so you can approve it](../image/dev-ops-request-number-select.png)

8.  Approve the request: On the Request form, set **Approval** and **Request state**to **Approved**.

    The import process begins immediately on approval.


## Import existing GitLab pipelines and repositories

After you have integrated GitLab with DevOps, you can import up to 90 days of existing GitLab pipeline and repository data. You can then use DevOps dashboards to view and manage GitLab data.

### Before you begin

Role required: admin

### About this task

-   You will request the data from the service catalog as a predefined catalog item.
-   Imported test summaries are linked to pipeline executions and not to step executions.
-   Only artifacts published using the artifacts keyword are imported.
-   Test results are not displayed for artifacts that have expired. You can set the expiration date of an artifact by configuring the **expire\_in** property in the pipeline. For more information on artifact expiration policies, see [Artifact and job meta data expiration](https://about.gitlab.com/blog/2020/06/18/job-artifact-meta-data-expiration-change/).
-   SonarQube scan results are not imported.
-   Only 6400 commits per branch can be imported in a single import.
-   GitLab imposes the following restriction: While associating run commits to a pipeline execution, GitLab doesn't provide the starting part of the commit details in some scenarios. It provides only the part before the SHA as '0000000000000000'. In such scenarios, the latest commit will be associated as the run commit. For example, when a new branch is created or when a pipeline is run manually.

    **Note:** The import process can take some time, hours for very large data sets.


### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **My Catalogs** and then select **DevOps Onboarding**.

2.  In the **Catalog Items** related list, select **DevOps App Onboarding**.

3.  On the Catalog Item form, select **Try It** to request the data.

    The resulting DevOps App Onboarding form enables you to specify the catalog item to order. In this case, the "app" to order is your GitLab instance.

    ![Specify the instance on the Onboarding form](../image/dev-ops-app-onboarding-form.png)

4.  Select the Select in list icon \(![Applications icon](../image/icon-view-list.png)\) on the **App** field and then select your instance of GitLab.

    Now that you have specified the instance, you will specify date range and sources of data to import.

5.  Repeat the following procedure for each repository that you want to import:

    1.  Select the Select in list icon \(![Applications icon](../image/icon-view-list.png)\) on the **Onboarding Repositories** field and then select the item to import.

        You can select multiple items.

    2.  Specify the range of dates for the data in the **Import From** and **Import To** fields.

    **Note:** The pipelines mapped to the repositories are automatically selected when you select the repository in the **Onboarding Repositories** field. You do not have to select the pipelines separately.

6.  Select **Order Now**.

    Your request appears on the Order Status page.

7.  Select the request number so you or another user with the admin role can approve the request.

    ![Select the request so you can approve it](../image/dev-ops-request-number-select.png)

8.  Approve the request: On the Request form, set **Approval** and **Request state** to **Approved**.

    The import process begins immediately upon approval.


