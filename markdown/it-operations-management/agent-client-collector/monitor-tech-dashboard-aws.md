---
title: Monitoring Technology Dashboard for AWS
description: With the AWS Monitoring Technology Dashboard, you can monitor the health and performance of your AWS infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs and servers.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Understanding the Monitoring Technology Dashboard, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Monitoring Technology Dashboard for AWS

With the AWS Monitoring Technology Dashboard, you can monitor the health and performance of your AWS infrastructure. By using the dashboard, you can identify the configuration items \(CIs\) and servers with the highest metric readouts, and view the most recent active alerts on those CIs and servers.

## Overview of the dashboard

The AWS Monitoring Technology Dashboard shows the five CIs and servers with the highest metric readouts during the past six hours. The dashboard also shows the 50 most recent active alerts in your AWS environment.

To view the dashboard, navigate to **All** &gt; **AIOps Dashboards** &gt; **Monitoring Technology Dashboards** and select **AWS Monitoring**.

## Using the Monitoring Technology Dashboard for AWS

Before using the Monitoring Technology Dashboard for AWS:

-   Create an AWS credential. For details on creating AWS credentials, see [Set up AWS service accounts](../../it-operations-management/concept/setup-aws-service-accounts.md).
-   Create a Discovery schedule, using the credential created in the previous step. For details on creating a Discovery schedule, see [Create discovery schedules for cloud resources](../../discovery/concept/discovery-manager.md#).
-   Ensure that you’re working in the Agent Client Collector Monitoring scope in your ServiceNow instance.
-   Ensure that the agent\_client\_collector\_admin and dashboard\_admin roles are enabled.
-   Enable Metric Intelligence on the MID Server.
-   Ensure that the **AWS Metrics**, **AWS EC2 Metrics**, and **AWS DynamoDB Metrics** policies are enabled.

    Enabling these policies activates metric to CI mapping.

-   Ensure that the clotho plugin version 1.19.0.10 or above is enabled.
-   After upgrading from a previous version, follow the procedure described in the [ACC-M Dashboard Filters are not working when upgraded from Tokyo/Utah to Vancouver \[KB1438042\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1438042) article in the NOW Support Knowledge Base.

The AWS Monitoring Technology Dashboard contains the tabs that are listed in the following table.

|Tab|Description|
|---|-----------|
|EC2|Displays the metric data from the EC2 \(virtual machines\) in the AWS environment.|
|EC2 Alerts|Displays the active EC2 \(virtual machine\) alerts in the AWS environment.|
|EBS|Displays the metric data from the EBS \(storage volume\) in the AWS environment.|
|S3|Displays the metric data from the S3 \(cloud object storage\) in the AWS environment.|
|RDS|Displays the metric data from the RDS \(cloud database\) in the AWS environment.|
|ELB|Displays the metric data from the ELB \(cloud load balancing\) in the AWS environment.|
|Dynamo DB|Displays the metric data from the Dynamo DB \(cloud database\) in the AWS environment.|
|ECS Cluster|Displays the metric data from the ECS cluster in the AWS environment.|
|ECS Service|Displays the metric data from the ECS service in the AWS environment.|

On the right side of widgets displaying a single metric, you can select the More options icon \(![More options icon](../image/three-vertical-icon.png)\) and select **Change group by**. Select the category you want to view the metric by: Host name, Class, Operating System, or OS Version.

Point to the relevant widget to view a specific datapoint and all of its details in a pop-up window. Select the **Alerts** tab to view the 50 most recent active alerts in your environment. Alerts help you to remediate your system by providing the information on problematic behavior.

Use the **Time range filter** to filter the time range for which you want metric data to display on the dashboard.

Use the **Metrics by selected CI filter** to select the CIs for which you want to view metrics.

You can customize the appearance of the individual widgets on the AWS Monitoring Technology Dashboard. For example, you could change the time that the EC2 metrics appear. You can also include the customized widgets when you are creating a custom dashboard. For more information, see [Customize the Monitoring Technology Dashboard](../task/customize-dashboard-widgets.md).

