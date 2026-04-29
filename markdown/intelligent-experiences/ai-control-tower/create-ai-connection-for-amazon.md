---
title: Create AI connection for Amazon
description: Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [AWS, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Create AI connection for Amazon

Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and n\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Select **Add**.

3.  Select **AWS** from all the available connectors.

4.  Click **Create connection**.

    **Note:** The Review the setup instructions page appears and verifies to follow all the prerequisites.

5.  Click **Continue**.

    Setup page appears.

6.  Select Source systems.

7.  Choose the AWS services that you want to integrate with ServiceNow.

    -   Amazon Bedrock
    -   Amazon Bedrock AgentCore
    -   Amazon SageMaker
8.  Click **Submit**.

9.  **Configure Bedrock**

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key ID**.

    3.  Enter the **Secret Access Key**.

        Access keys are long-term credentials for an IAM user or the AWS account root user. Access keys consist of two parts: an access key ID and a secret access key. For detailed information, see [how to get access and secret key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

    4.  Enter the **AWS Region**.

        **Note:** The region information is available in the navigation bar of the AWS management console.

    5.  Click **Update and test connection**.

    6.  Click **Continue**.

10. **Configure Bedrock import schedule**

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

11. **Configure CloudWatch logs forBedrock**

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key**.

    3.  Enter the **Secret Key**.

    4.  Enter the **AWS Region**.

    5.  Enter the **Log Group Names**.

    6.  Click **Create and test connection**.

    7.  Click **Continue**.

12. **Configure CloudWatch logs import schedule for Bedrock**

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Click **Continue**.

13. **Configure SageMaker**

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key ID**.

    3.  Enter the **Secret Access Key**.

    4.  Enter the **AWS Region**.

    5.  Click **Create and test connection**.

    6.  Click **Continue**.

14. **Configure SageMaker import schedule**

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select Run according to your preference.

    4.  Select Execute Now.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Click **Continue**.

15. **Configure CloudWatch monitoring for SageMaker**

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key**.

    3.  Enter the **Secret Key**.

    4.  Enter the **AWS Region**.

    5.  Click **Create and test connection**.

    6.  Click **Continue**.

16. **Configure CloudWatch monitoring import schedules for SageMake**

    1.  Open a parent schedule import.

    2.  Select Active check box.

    3.  Select Run according to your preference.

    4.  Select Execute Now.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Click **Continue**.


## Result

AI connection is created for AWS.

