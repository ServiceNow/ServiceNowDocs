---
title: Create an AI connection for Amazon
description: Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-ai-connection-for-amazon.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [AWS, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for Amazon

Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon.

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Click **Add**.

3.  Select **AWS** from all the available connectors.

4.  Click **Create connection**.

    **Note:** The Review the setup instructions page appears and verifies to follow all the prerequisites.

5.  Select Download basic scripts.

    **Note:** Download the basic scripts and select the check box.

6.  Select **Continue**.

    Setup page appears.

7.  Select Source systems.

8.  Choose the AWS services that you want to integrate with ServiceNow.

    -   Amazon Bedrock
    -   Amazon Bedrock AgentCore
    -   Amazon SageMaker
9.  Select **Submit**.

10. **Configure Amazon Bedrock**

    1.  Enter the **Connection Name**

    2.  Enter the **Access Key ID**

    3.  Enter the **Secret Access Key**

        The Access keys are long-term credentials for an IAM user or the AWS account root user. Access keys consist of two parts: an access key ID and a secret access key. For detailed information, see [how to get access and secret key](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

    4.  Enter the **AWS Region**.

        **Note:** The region information is available in the navigation bar of the AWS management console.

    5.  Enter the **Management Account ID**

        **Note:** The Management Account ID applies in two scenarios:

        -   Your IAM user is created in a Designated Member account.
        -   You need Organizational-level access.
    6.  Enter the **Standalone Account ID**

        **Note:** This step is optional. Provide a single account ID to test discovery against that account before enabling full Organization discovery.

    7.  Enter the STS Assume Role

        The role assumed for discovery.

    8.  Select **Update and test connection**

    9.  Select **Continue**

11. **Configure Bedrock import schedule**

    1.  Open a parent schedule import

    2.  Select the Active check box

    3.  Select Run according to your preference

        **Note:** This is an optional step as the schedule imports run according to the schedule.

12. **Configure CloudWatch logs forBedrock**

    1.  Enter the **Connection Name**.

    2.  Enter the **Access Key**.

    3.  Enter the **Secret Key**.

    4.  Enter the **AWS Region**.

    5.  Enter the **Log Group Names**.

    6.  Select **Create and test connection**.

    7.  Select **Continue**.

13. **Configure CloudWatch logs import schedule for Bedrock**

    1.  Open a parent schedule import.

    2.  Select the Active check box.

    3.  Select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    4.  Select **Continue**.

14. **Configure SageMaker**

    1.  Enter the **Connection Name**

    2.  Enter the **Access Key ID**

    3.  Enter the **Secret Access Key**

    4.  Enter the **AWS Region**

    5.  Select **Create and test connection**

    6.  Select **Continue**

15. **Configure SageMaker import schedule**

    1.  Open a parent schedule import

    2.  Select the Active check box

    3.  Select Run according to your preference

    4.  Select Execute Now

        **Note:** This is an optional step as the schedule imports run according to the schedule

    5.  Select **Continue**

16. **Configure CloudWatch monitoring for SageMaker**

    1.  Enter the **Connection Name**

    2.  Enter the **Access Key**

    3.  Enter the **Secret Key**

    4.  Enter the **AWS Region**

    5.  Select **Create and test connection**

    6.  Select **Continue**

17. **Configure CloudWatch monitoring import schedules for SageMake**r

    1.  Open a parent schedule import

    2.  Select Active check box

    3.  Select Run according to your preference

    4.  Select Execute Now

        **Note:** This is an optional step as the schedule imports run according to the schedule

    5.  Select **Continue**.


## Result

The AI connection for AWS is created and configured.

