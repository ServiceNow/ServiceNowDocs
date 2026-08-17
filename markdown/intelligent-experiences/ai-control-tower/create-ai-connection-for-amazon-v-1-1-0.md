---
title: Create an AI connection for Amazon \(v1.1.0\)
description: Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 1.1.0\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-ai-connection-for-amazon-v-1-1-0.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [AWS, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Create an AI connection for Amazon \(v1.1.0\)

Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 1.1.0\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Select **AWS** from the available connectors and then select **Create connection**.

3.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

4.  Select **Continue**.

    Setup page appears.

5.  Select Source systems.

6.  Choose the AWS services that you want to integrate with ServiceNow.

    -   Amazon Bedrock
    -   Amazon Bedrock AgentCore
    -   Amazon SageMaker
7.  Select **Submit**.

8.  Enter the details on Configure Amazon Bedrock:

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key ID**.

    3.  Enter the **Secret Access Key**.

        The Access keys are long-term credentials for an IAM user or the AWS account root user. Access keys consist of two parts: an access key ID and a secret access key. For detailed information, see [how to get access and secret key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html).

    4.  Enter the **AWS Region**.

        **Note:** The region information is available in the navigation bar of the AWS management console and this can be a comma separated field. So, you can enter multiple regions.

    5.  Select **Update and test connection**.

    6.  Select **Continue**.

9.  Configure Bedrock import schedule:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

10. Enter the details on Configure CloudWatch logs for Bedrock:

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key**.

    3.  Enter the **Secret Key**.

    4.  Enter the **AWS Region**.

    5.  Enter the **Log Group Names**.

    6.  Select **Create and test connection**.

    7.  Select **Continue**.

11. Configure CloudWatch logs import schedule for Bedrock:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

12. Enter the details on Configure SageMaker:

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key ID**.

    3.  Enter the **Secret Access Key**.

    4.  Enter the **AWS Region**.

    5.  Select **Create and test connection**.

    6.  Select **Continue**.

13. Configure SageMaker import schedule:

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

14. Enter the details on Configure CloudWatch monitoring for SageMaker:

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key**.

    3.  Enter the **Secret Key**.

    4.  Enter the **AWS Region**.

    5.  Select **Create and test connection**.

    6.  Select **Continue**.

15. Configure CloudWatch monitoring import schedules for Sagemaker:

    1.  Open a parent schedule import.

    2.  Select Active check box.

    3.  Select Run according to your preference.

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Select **Continue**.

16. Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

