---
title: Create an AI connection for Amazon \(v1.3\)
description: Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 1.3\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/create-an-ai-connection-for-amazon-v1-3.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-07-05"
reading_time_minutes: 1
breadcrumb: [AWS, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for Amazon \(v1.3\)

Create an AI connection for Amazon in AI Control Tower using the AI Service Graph Connector for Amazon \(version 1.3\).

## Before you begin

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## Procedure

1.  Navigate to **Al Control Tower** &gt; **Configurations** &gt; **AI connections**.

2.  Click **Add**.

3.  Select **AWS** from the available connectors.

4.  Click **Create connection**.

5.  Review setup instructions page displays.

    **Note:** Verify to follow all the prerequisite steps.

6.  Select Download basic scripts.

    **Note:** Download the basic scripts and select the check box.

7.  Select **Continue**.

    Setup page appears.

8.  Select Source systems.

9.  Choose the AWS services that you want to integrate with ServiceNow.

    -   Amazon Bedrock
    -   Amazon Bedrock AgentCore
    -   Amazon SageMaker
10. Select **Submit**.

11. **Configure Amazon Bedrock**

    1.  Select **Create and test connection**

    2.  Enter the **Connection Name**

    3.  Enter the **Access Key ID**

    4.  Enter the **Secret Access Key**

    5.  Enter the **AWS Regions**

    6.  Enter the **Management Account ID**

    7.  Enter the **Standalone Account ID**

    8.  Enter the **STS Assume Role**

    9.  Click **Create and test connection**

        A banner appears displaying Connection verified.

    10. Click **Continue**

12. **Configure Amazon Bedrock import schedule**

    1.  Open a parent schedule import

    2.  Select the Active check box

    3.  Select Run according to your preference

    4.  To run frequency by demand, select **Execute now**

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Click **Continue**

13. **Configure Amazon CloudWatch logs**

    1.  Enter the **Connection Name**

    2.  Enter the **Secret Key**

    3.  Enter the **Management Account ID**

    4.  Enter the **STS Assume Role**

    5.  Enter the **Access Key**

    6.  Enter the **AWS Regions**

    7.  Enter the **Standalone Account ID**

    8.  Enter the **Log Group Names**

    9.  Click **Create and test connection**

        A banner appears displaying Connection verified.

    10. Click **Continue**

14. **Configure Amazon CloudWatch logs import schedules**

    1.  Open a parent schedule import

    2.  Select the Active check box

    3.  Select Run according to your preference

    4.  To run frequency by demand, select **Execute Now**.

        **Note:** This is an optional step as the schedule imports run according to the schedule.

    5.  Click **Continue**

15. Select the **Confirm connection setup** activity to verify whether the connection was configured.


## Result

Click **View all connections** to view the newly created connection.

AI connection for AWS is created and configured.

