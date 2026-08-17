---
title: Create an AI connection for Amazon \(v2.0.2\)
description: Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 2.0.2\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-an-ai-connection-for-amazon-v2-0-2.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-07-05"
reading_time_minutes: 2
breadcrumb: [AWS, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for Amazon \(v2.0.2\)

Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 2.0.2\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Select **AWS** from the available connectors and then select **Create connection**.

3.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

4.  Select Download basic scripts.

    **Note:** Download the basic scripts and select the check box.

5.  Select **Continue**.

    Setup page appears.

6.  Select Source systems.

7.  Choose the AWS services that you want to integrate with ServiceNow.

    -   Amazon Bedrock
    -   Amazon SageMaker
    -   Amazon Bedrock AgentCore
8.  Select **Submit**.

9.  Enter the details on Configure Amazon Bedrock:

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key ID**.

    3.  Enter the **Secret Access Key**.

    4.  Enter the **AWS Regions**

    5.  Enter the **Management Account ID**.

    6.  Enter the **Standalone Account ID**.

    7.  Enter the **STS Assume Role**.

    8.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    9.  Select **Continue**.

10. Configure Amazon Bedrock import schedule:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

11. Enter the details on Configure Amazon CloudWatch logs:

    1.  Enter the **Connection Name**.

    2.  Enter the **Secret Key**.

    3.  Enter the **Management Account ID**.

    4.  Enter the **STS Assume Role**.

    5.  Enter the **Access Key**.

    6.  Enter the **AWS Regions**.

    7.  Enter the **Standalone Account ID**.

    8.  Enter the **Log Group Names**.

    9.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    10. Select **Continue**.

12. Configure Amazon CloudWatch logs import schedules:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

13. Enter the details on Configure Amazon SageMaker:

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key ID**.

    3.  Enter the **Secret Access Key**.

    4.  Enter the **AWS Regions**.

    5.  Enter the **Management Account ID**.

    6.  Enter the**STS Assume Role**.

    7.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    8.  Select **Continue**.

14. Configure Amazon Sagemaker import schedule:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

15. Enter the details on Configure Amazon Bedrock AgentCore:

    1.  Enter the **Connection Name**.

    2.  Enter the **Secret Key**.

    3.  Enter the **Management Account ID**.

    4.  Enter the **STS Assume Role**.

    5.  Enter the **Access Key**.

    6.  Enter the **AWS Regions**.

    7.  Enter the **Standalone Account ID**.

    8.  Enter the **Log Group Names**.

    9.  Select **Create and test connection**.

        A banner appears displaying Connection verified.

    10. Select **Continue**.

16. Configure Amazon Bedrock AgentCore import schedule:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

17. Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

